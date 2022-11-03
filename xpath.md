# XPATH

XPath(XML Path Language) 通过“路径表达式” 在 XML/HTML 文本中选择节点。

公式表示为: /nodes[predicates], 即 /node1[predicate1][predicate2]//node2/node3[predicate3] | /node4[predicate4]

## Nodes(节点)

- Element /, //, table, span, ...
- Attribute @class, @id, @href, @src, ...
- Text text()
- Comment comment()
- Axes preceding-sibling::, following-sibling::, ancestor, ...

## Predicates(谓语条件)

- 索引 1, last(), position(), count(), ...
- 算术运算 =, !=, >, <, ...
- 逻辑运算 and, or, not, ...
- 字符串判断 starts-with(), ends-with(), contains(), normalize-space(), ...
- 字符串处理 substring-before(), substring-after(), concat(), ...

## 其它

- 连接多个 Xpath |

## Notes!!!

在浏览器中能执行的 xpath 为什么在 expression 提取不到结果， 这个要对比浏览器中的 html 跟显示网页源代码中的 html 有什么不一样，一般有这几种情况

1. **浏览器给 html 加标签了，比如 table 的子节点的会加一层 tbody 标签**
2. 原来的 html 标签开合不匹配或者标签 id 重复，xpath 库解析 html 报错（调试时会有日志），但是浏览器自动修复了或者忽略错误了，这种情况可以通过 regex_replace 对 email.body 进行修复
3. 如果是 follow link 获取到的 html，可能有某些 header 缺失或者 cookie 问题导致获取到的 html 结构不一样，要对比一下获取到的 html 和浏览器的 html 是否一样
4. 在 chrome 浏览器里调试 xpath 可以用 `$x(xpath_pattern)` 的方式，比如 `$x("//strong[contains(text(), 'Order #')]/parent::td/text()[re:match(., 'W\\d{14}')]")`
5. 我们在 expression 里支持了拓展正则表达式，可以用 `re:match(text, pattern)` 的方式来做正则匹配，但是这个运算不能在浏览器里面执行

## XPATH 案例分析

```html
see wsgggws.html
```

```bash
# 获取 element
//table/tbody/tr/td

# 获取 attribute, text, comment,
//div/div/img/@src

# 获取 text, comment,
//div/div/span/text()

# 获取 comment,
//div/comment()

# Axe 的使用
//div/div/img/following-sibling::span/text()
```

```bash
# 使用谓语 [@id], [1]
//div[@id='node']/table/tbody/tr[1]/td

# 使用谓语 [last()]
//table/tbody/tr[last()]/td

# 使用谓语 [postition()]
//table/tbody/tr[position()=1]/td

# 使用谓语并条件判断 = <
//table/tbody[count(tr)=7]/tr/td
//table/tbody[count(tr)<7]/tr/td

# 使用谓语并逻辑判断 and not
//table/tbody[count(tr)=7 and tr/td]/tr/td
//table/tbody[count(tr)=7]/tr[not(td)]

# 使用谓语 [count()] [starts-with] 函数判断
//table/tbody[count(tr)=7]/tr/td[starts-with(., 'starts-with')]

# 使用谓语 [contains(node, ...)] 函数判断
//div[contains(@class, 'predicate')]/table/tbody[count(tr)=7]/tr/td[contains(., '()')]
//table/tbody[count(tr)=7]/tr/td[contains(., '()')]

# 使用 concat 拼接，但得使用 console 里的 $x
$x("concat(//table/tbody[count(tr)=7]/tr/td[starts-with(., 'starts-with')]/preceding-sibling::th/text(), //table/tbody[count(tr)=7]/tr/td[starts-with(., 'starts-with')])")


# 取两个注释中间的 tr, node 为 ’preceding-sibling::commnet()‘
//div/table/tbody/tr[contains(preceding-sibling::comment(), 'special tr start') and contains(following-sibling::comment(), 'special tr end')]
```

## exam 1

```html
<!--  如何得到  merchandise Total 的价格， 当 merchandise Total 并不总是出现在第一列! -->
<td>
  <table>
    <tbody>
      <tr>
        <td class="left">*Merchandise Total:</td>
      </tr>
      <tr>
        <td class="left">Discount:</td>
      </tr>
      <tr>
        <td class="left">*Processing &amp; Delivery:</td>
      </tr>
      <tr>
        <td class="left">*Tax:</td>
      </tr>
      <tr>
        <td class="left"><strong>*Total:</strong></td>
      </tr>
    </tbody>
  </table>
  <table>
    <tbody>
      <tr>
        <td>$29.95</td>
      </tr>
      <tr>
        <td>$0.00</td>
      </tr>
      <tr>
        <td>$8.99</td>
      </tr>
      <tr>
        <td>$0.00</td>
      </tr>
      <tr>
        <td>$38.94</td>
      </tr>
    </tbody>
  </table>
</td>
```

```bash

# 这时候我们可以用上边 table 的文案去定位下边的 price，例如：

/td/table[2]//tr[ position() = count(/td/table[1]//tr[.//text()[contains(.,
'Merchandise')]]/preceding-sibling::tr)+1 ]/td/text()

# 1. 我们先找到左边的 table 和对应的文案，也就是 /td/table[1]//tr[.//text()[contains(., 'Merchandise')]]
# 2. 然后我们根据这个文案找出他在当前上下文的位置，也就是 count(/td/table[1]//tr[.//text()[contains(., 'Merchandise')]]/preceding-sibling::tr)+1。这里 +1 是因为 xpath 的 position 是从 1 开始计算，而 count 的最小值是 0（表示没有同级的前文节点）
# 3. 然后我们在右边的 table 里找出位置相同的节点，也就是 /td/table[2]//tr[ position() = 第二步得出的结论]，最终的 xpath 为 `/td/table[2]//tr[ position() = count(/td/table[1]//tr[.//text()[contains(., 'Merchandise')]]/preceding-sibling::tr)+1 ]`
# 4. 然后根据第三步的节点，找出我们想要的文案，也就是 /td/table[2]//tr[ position() = count(/td/table[1]//tr[.//text()[contains(., 'Merchandise')]]/preceding-sibling::tr)+1 ]/td/text()
```

### exam 2:

```html
<!--  如何获得所有地址? `ABCDABCD` `ABCDABCD` `ABCDABCD` 为地址 -->
<html>
  <div>
    Hello!
    <br />
    <b>Shipment Address</b>
    <br />
    ABCDABCD
    <br />
    ABCDABCD
    <br />
    ABCDABCD
    <br />
    <b>Tracking Your Order</b>
    <br />
    you tracking number: xxxx
  </div>
</html>
```

```bash
# 可以通过 position 定位 `Shipment Address` 与 `Tracking Your Order` 之间的位置

//div/text()[contains(preceding-sibling::b, 'Shipment Address') and contains(following-sibling::b, 'Tracking Your Order')]
```
