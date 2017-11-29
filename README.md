# mobiscroll
基于mobiscroll的demo（年月日、选项）


最近做一个模仿ios滚动选择，从网上找了mobiscroll这个插件，但是是付费版的，不过在天朝想收费是不存在的。。。<br>
这是mobiscroll的api：https://demo.mobiscroll.com <br><br><br>
# 示例1
html：
```
<select name="sex" id="sex" class="am-text-center">
      <option value="1">男</option>
      <option value="2">女</option>
 </select>
 ```
 js:
 ```
 $('#sex').mobiscroll().select({
    theme: 'ios',// 主题
    lang: 'zh',
    cancelText:'取消',// 取消按钮的text
    setText:'确定',// 确认按钮的text
    display: 'bottom',
    minWidth: 200// 每个选择条的宽度
  });
   ```
# 示例2 年月日
html：
```
<input id="times" name="times" />
 ```
 js:
 ```
var now = new Date(),
    max = new Date(now.getFullYear() + 100, now.getMonth(), now.getDate());

    $('#times').mobiscroll().date({
      theme: 'ios',
      lang: 'zh',
      display: 'bottom',
      max: max,
      dateFormat: 'yy.mm.dd', // 日期格式
      setText: '确定', //确认按钮名称
      cancelText: '取消',//取消按钮名籍我
      dateOrder: 'yymmdd' //面板中日期排列格式
    });
   ```
