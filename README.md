#  PHP入门到放弃
# 我要学PHP #
## 我要学PHP ##
### 我要学PHP ###
#### 我要学PHP ####
##### 我要学PHP #####
###### 我要学PHP #######

-------

学习PHP 方法变通学习起来就很快了。请仔细阅读以下内容：

-------

# 入门 ##
PHP 是开源的，并且完全免费的。 PHP 是一种通用的脚本语言，可以运行在多种平台上。

-------
# 安装 ##
因为懒，直接使用一键环境安装，例如 [宝塔（点击访问）](https://www.bt.cn/)，配置好环境后，就可以开始使用 PHP 了。

-------
## 基础语法 ##
PHP 脚本以 <?php 开头，以 ?> 结尾：
```php
<?php
// 此处是 PHP 代码，以下内容少儿不宜
?>
```

## 变量 ##
变量以 $ 开头，变量名只能包含字母、数字和下划线，并且不能以数字开头。
```php
<?php
//$可以理解为开始标记，$后面是变量名，也就是你想存储的名称
$王总 = "我叫王总";
?>
```

## 输出变量 ##
输出变量echo 和 print 语句
```php
<?php
// 定义一个字符串
$王总 = "王总是个字符串";

// 使用 echo 输出字符串，相当于直接把东西输出到浏览器或者命令行（装逼装早了，命令行后面在学）
echo $王总;

// 注意: echo 和 print 的主要区别在于 echo 可以输出多个参数，而 print 只能输出一个参数
// echo 通常被认为比 print 快，因为它不返回任何值
// 示例: echo 可以输出多个字符串
echo "Hello", " ", "world!"; // 输出 "Hello world!"

// print 只能输出一个字符串，并始终返回 1
// 下面的代码演示了 print 的用法
// print $txt; // 已经在上面演示过
?>
```
## 数据类型 ##
PHP 支持多种数据类型，包括字符串、整数、浮点数、布尔值、数组和对象。
```php
<?php
$string = "Hello world!"; // 字符串
$integer = 10; // 整数
$float = 10.5; // 浮点数
$boolean = true; // 布尔值
$array = array("apple", "banana", "orange"); // 数组
$object = new stdClass(); // 对象
$null = null; // 空值
?>
```

## 字符串函数 ##
strlen()，str_word_count()，strrev()，strpos()，str_replace()，strtoupper()，strtolower()，substr()，trim()，ltrim()，rtrim()，explode()，implode()，str_split()，str_shuffle()，str_repeat()，str_pad()，str_ireplace()，str_word_count()
```php
<?php
$string = "Hello world!"; // 字符串
$length = strlen($string); // 获取字符串长度
echo "字符串长度为 ".$length; // 输出 "字符串长度为 12",这里讲下这个. 就是拼接的意思，就是把后面的字符串拼接到前面

$wordCount = str_word_count($string); // 获取字符串中的单词数量
echo "字符串中的单词数量为 $wordCount"; // 输出 "字符串中的单词数量为 2"

$reversedString = strrev($string); // 反转字符串
echo "反转后的字符串为 ".$reversedString; // 输出 "dlrow olleH"

$position = strpos($string, "world"); // 查找字符串中 "world" 的位置
echo "字符串中 \"world\" 的位置为 ".$position; // 输出 "字符串中 "world" 的位置为 6"

$newString = str_replace("world", "PHP", $string); // 替换字符串中的 "world" 为 "PHP"
echo "替换后的字符串为 ".$newString; // 输出 "Hello PHP!"

$uppercaseString = strtoupper($string); // 将字符串转换为大写
echo "大写字符串为 ".$uppercaseString; // 输出 "HELLO WORLD!"

$lowercaseString = strtolower($string); // 将字符串转换为小写
echo "小写字符串为 ".$lowercaseString; // 输出 "hello world!"

$substring = substr($string, 6, 5); // 获取字符串中从索引 6 开始的 5 个字符
echo "子字符串为 ".$substring; // 输出 "world"

$trimmedString = trim($string); // 去除字符串中的空格
echo "去除空格后的字符串为 ".$trimmedString; // 输出 "Helloworld!"

$leftTrimmedString = ltrim($string); // 去除字符串中的左侧空格
echo "去除左侧空格后的字符串为 ".$leftTrimmedString;

$rightTrimmedString = rtrim($string); // 去除字符串中的右侧空格
echo "去除右侧空格后的字符串为 ".$rightTrimmedString; 

$explodedArray = explode(" ", $string); // 将字符串拆分为数组
echo "拆分后的数组为 " . implode(", ", $explodedArray); // 输出 "Hello, world!"

$joinedString = implode(" ", $explodedArray); // 将数组合并为字符串
echo "合并后的字符串为 ".$joinedString; // 输出 "Hello world!"

$splitString = str_split($string); // 将字符串拆分为字符数组
echo "拆分后的字符数组为 " . implode(", ", $splitString); // 输出 "H, e, l, l, o,  , w, o, r, l, d, !"

$shuffledString = str_shuffle($string); // 将字符串打乱
echo "打乱后的字符串为 ".$shuffledString; // 输出 "Hellodlrow !"

$repeatedString = str_repeat($string, 3); // 重复字符串
echo "重复后的字符串为 ".$repeatedString; // 输出 "Hello world!Hello world!Hello world!"

$paddedString = str_pad($string, 20, "*", STR_PAD_LEFT); // 在字符串左侧填充字符
echo "填充后的字符串为 ".$paddedString; // 输出 "*****Hello world!"

$replacedString = str_ireplace("world", "PHP", $string); // 忽略大小写替换字符串中的 "world" 为 "PHP"
echo "忽略大小写替换后的字符串为 ".$replacedString; // 输出 "Hello PHP!"

$wordCount = str_word_count($string); // 获取字符串中的单词数量
echo "字符串中的单词数量为 ".$wordCount; // 输出 "字符串中的单词数量为 2"

?>
```

## 常量 ##
常量类似变量，但是常量一旦被定义就无法更改或撤销定义。 在 PHP 中，常量使用 define() 函数定义。
```php
<?php
// 定义常量，大小写敏感，也就是调用是必须大小写一致
define("GREETING", "Hello world!");
// 输出常量，常量不同于变量，不需要使用 $ 符号
echo GREETING;
// 定义常量，大小写不敏感，调用时大小写可以不同
define("GREETING", "Hello world!", true);
echo greeting;
?>
```

## 运算符 ##
也就是小学学到的算法，PHP 支持以下运算符：

| 运算符  |   描述    |         示例 |
|:-----|:-------:|-----------:|
| +    |   加法	   |    $x + $y |
| -    |   减法	   |    $x - $y |
| *    |   乘法	   |    $x * $y |
| /    |   除法	   |    $x / $y |
| %    |   取余	   |    $x % $y |
| **   |   指数	   |   $x ** $y |
| +=   |  加法赋值   |   $x += $y |
| -=   |  减法赋值   |   $x -= $y |
| *=   |  乘法赋值   |   $x *= $y |
| /=   |  除法赋值   |  	$x /= $y |
| %=   |  取余赋值	  |   $x %= $y |
| ++   |   自增	   |       $x++ |
| --   |   自减	   |       $x-- |
| ==   |   等于	   |   $x == $y |
| !=   |  不等于	   |   $x != $y |
| ===  |  完全等于	  |  $x === $y |
| !==  | 完全不等于	  |  $x !== $y |
| >    |   大于	   |    $x > $y |
| <    |   小于	   |    $x < $y |
| >=   |  大于等于	  |   $x >= $y |
| <=   |  小于等于	  |   $x <= $y |
| &&   | 逻辑 AND	 |   $x && $y |
| \|\| | 逻辑 OR	  | $x \|\| $y |
| !    | 逻辑 NOT  |       	!$x |

## 运算符优先级 ##
小学毕业的时候，我们知道数学运算符的优先级，在 PHP 中，运算符的优先级与数学运算符的优先级相同。
```php

<?php 
$x=17; 
$y=8;
echo ($x + $y); // 输出 25
echo ($x - $y); // 输出 9
echo ($x * $y); // 输出 136
echo ($x / $y); // 输出 2.125
echo ($x % $y); // 输出 1
?>
```

## 条件语句 ##
单条件，多条件，嵌套条件，条件语句在 PHP 中使用 if、else、elseif 等关键字来定义。
```php
<?php
// 单条件
$王总 = 10;
if ($王总 > 5) { //判断王总是否大于 5
    echo "王总 是大于 5 ";
}else { // else是否定，也就是不是上面的条件
    echo "王总 是小于 5";
}
// 多条件
if ($王总 > 5 && $王总 < 15) { //判断王总是不是大于 5 小于 15
    echo "王总 是大于 5 小于 15";
}elseif ($王总 > 15) { //王总大于 5 小于 15，那我们在判断王总是大于 15
    echo "王总 是大于 15";
}else { //都不是
    echo "王总 都不符合上面的条件";
}
// 嵌套条件
if ($王总 > 5) { //判断王总是否大于 5
    //王总 大于 5那我们在判断王总是不是小于 15
    if ($王总 < 15) {
        echo "王总 是大于 5 小于 15 的";//那为什么我们知道他是大于 5 小于 15？，因为上面的条件是判断王总大于 5
    }else {
        //王总条件不符合，
        echo "王总 都不符合上面的条件";
    }
}else {
    echo "王总 是小于等于 5 的";
}
```
Switch 语句跟if 语句一样，用于判断一个变量的值。但是 switch 语句比 if 语句更简单，更易读。
```php
<?php
$王总 = "红色";
switch ($王总) {
case "红色":
    echo "王总穿的颜色是红色!";
    break;
case "蓝色":
    echo "王总穿的颜色是蓝色!";
    break;
case "绿色":
    echo "王总穿的颜色是绿色!";
default:
    echo "王总穿的颜色不是红色、蓝色、绿色!";
}
?>
```
## 循环语句 ##
在 PHP 中，循环语句用于重复执行代码块。 可以使用 for、while、do…while 等关键字来定义循环。
PHP 支持以下循环语句：
```php
<?php
// for 循环
$王总 = 0;
for ($王总 = 0; $王总 <= 10; $王总++) {
    echo "for 是 ".$王总." <br>";
}
// while 循环
while ($王总 <= 10) {
    echo "while 是 ".$王总." <br>";
}
// do…while 循环
do {
    echo "do…while 是 ".$王总." <br>";
    $王总++;
}while ($王总 <= 10);
```

## 函数 ##
在 PHP 中，函数是用于执行特定任务的代码块。 可以使用函数来提高代码的复用性和可读性。可以比喻成一个函数是一段可以重复使用的代码。
```php
<?php
// 函数定义，function 关键字后跟函数名,也就是你想取名的函数
function 王总() {
    // 函数体
    echo "Hello World!";
}
// 函数调用，调用函数时，需要使用函数名，加括号
王总();

// 函数参数，函数可以接受参数，参数是函数调用时传递给函数的值
function 装总($秘书) { // $秘书 是参数，也是你可以自己取的名字
    echo "Hello ".$秘书;
}
装总("苏秘书");

// 函数返回值，函数可以返回值，返回值是函数执行结束后返回给调用者的值
function 逼总($秘书) {
    return "Hello ".$秘书;
}
$逼总说的话 = 逼总("高秘书");
echo $逼总说的话;

// 多个参数传递
function 杂总($秘书, $秘书2) {
    return "Hello ".$秘书."，".$秘书2;
}
$杂总说的话 = 杂总("李秘书", "张秘书");
echo $杂总说的话;

// 匿名函数，匿名函数是一种没有名字的函数，匿名函数可以作为参数传递给另一个函数，也可以作为返回值返回。
$王总 = function ($秘书) {
    echo "Hello ".$秘书;
}
$王总("装秘书");

```

## 数组 ##
数组是一种用于存储多个值的数据结构。在 PHP 中，数组可以包含字符串、数字、布尔值等数据类型。 数组在 PHP 中使用数组关键字来定义。数组可以包含多个值，每个值都有一个索引，索引是从 0 开始的。
```php
<?php
$牛总 = array("王总", "装总", "逼总", "杂总");// 数组定义，牛总是老板, 王总,装总,逼总,杂总,是牛总手里的
echo $王总[0]; // 牛总叫王总的代号0，王总就出来了，以此类推

// 我们可以使用 count() 函数来获取数组的长度，看看我们牛总一共有多少个员工
echo count($牛总);

// 数组的键值对，键是字符串，值是字符串，吊总知道他们的外号，键是王总，值是王小儿
$吊总 = array("王总" => "王小儿", "装总" => "装不下去", "逼总" => "逼你上天", "杂总" => "杂乱无章");
echo $吊总["装总"];// 我们问吊总，装总叫什么，吊总叫装不下去
```

## 超全局变量 ##
超全局变量是 PHP 中的特殊变量，可以在任何地方访问。 超全局变量包括 $_GET、$_POST、$_COOKIE、$_SESSION、$_SERVER、$_ENV、$_FILES 等。 超全局变量在 PHP 中使用 $ 符号来引用。
```php
<?php
// 超全局变量 $_GET
$王总听到 = $_GET["李秘书"]; // 获取 $_GET["李秘书"] 的值
// 如何使用呢？
//我们访问：http://localhost/index.php?李秘书=你在狗叫什么
echo "李秘书跟王总说：".$王总听到;

// 超全局变量 $_POST
$李总听到 = $_POST["张秘书"]; // 获取 $_POST["张秘书"] 的值
// 如何使用呢？
// 我们这就要用到 form 表单了，我们访问：http://localhost/index.php
//<form method="post" action="index.php">
//<input type="text" name="张秘书">
//</input>
//<input type="submit" value="提交">
//</form>
echo "张秘书跟王总说：".$李总听到;

// 超全局变量 $_COOKIE
setcookie("C秘书", "杂乱无章", time() + 3600); // 设置一个名为 "C秘书" 的 cookie，值为 "杂乱无章"，有效期 3600 秒

$杂总听到 = $_COOKIE["C秘书"]; // 获取 $_COOKIE["王总"] 的值
echo "C秘书跟王总说：".$杂总听到; 

// 超全局变量 $_SESSION
session_start();// 开启 session
$_SESSION["D秘书"] = "装不下去"; // 设置一个名为 "D秘书" 的 session，值为 "装不下去"
$装总听到 = $_SESSION["D秘书"];
echo "D秘书跟王总说：".$装总听到;

// 超全局变量 $_SERVER ，一般不会用到，所以就不写了
$server = $_SERVER;
foreach ($server as $key => $value) {
    echo "$key: $value<br>";
}

// 超全局变量 $_ENV ，一般不会用到，所以就不写了
$env = getenv();
foreach ($env as $key => $value) {
    echo "$key: $value<br>";
}

// 超全局变量 $_FILES，一般不会用到，所以就不写了
$files = $_FILES;
foreach ($files as $key => $value) {
    echo "$key: $value<br>";
}

```
## 类 ##
类是一种用于创建对象的模板。 类可以包含属性和方法。 类在 PHP 中使用 class 关键字来定义。 类可以包含多个属性和方法。
```php
<?php
// 类定义，class 关键字后跟类名,也就是你想取名的类
class 隔壁老王有限公司 {
    public $王总;
    // 构造函数，构造函数是类创建时自动调用的函数，也就是类创建时自动调用的函数
    public function __construct($王总) {
        $this->王总 = $王总;
    }
    // 方法，方法可以执行任务，方法可以返回值
    public function 老板() {
        echo "隔壁老王有限公司老板是：".$this->王总;
    }
    static 
    // 析构函数，析构函数是类销毁时自动调用的函数，也就是类销毁时自动调用的函数
    public function __destruct() {
        echo "删库跑路"
    }
}
// 使用
$隔壁老王有限公司 = new 隔壁老王有限公司("王总");
$隔壁老王有限公司->老板();
```
## 表单 ##
表单是一种用于收集用户输入的数据的 HTML 元素。 表单在 PHP 中使用 form 元素来定义。 表单可以包含多个输入元素。
```html
<!-- 创建一个文件 index.html -->
<html>
<body>
<form action="隔壁老王有限公司.php" method="post">
李秘书要说的话: <input type="text" name="李秘书"><br>
<input type="submit">
</form>

</body>
</html>
```
```php
<?php
// 创建一个文件 隔壁老王有限公司.php
$老板听到 = $_POST["李秘书"]; // 获取 $_POST["李秘书"] 的值，也就是李秘书说啥，切记做好安全性，不然李秘书会被拐走
echo "李秘书跟隔壁老王有限公司老板说：".$老板听到;
?>
```
安全校验：
```html
<html>
<body>
<form action="隔壁老王有限公司.php" method="post">
    <input type="text" name="李秘书" value="<script>location.href('http://www.hacked.com')</script> 真的是我，不要走！">
    <input type="submit">
</form>
</body>
</html>

```
```php
<?php
// 定义变量并设置为空值
$老板 = "";

if ($_SERVER["REQUEST_METHOD"] == "POST") { // 判断表单是否被提交
  $老板 = test_input($_POST["李秘书"]);
}
// 防止李秘书胡说八道，也就是XSS攻击
function test_input($data) {
  $data = trim($data); // 去除字符串中的空格
  $data = stripslashes($data); // 去除字符串中的反斜杠
  $data = htmlspecialchars($data); // 将 HTML 标签转换为实体
  return $data;
}
echo "李秘书跟隔壁老王有限公司老板说：".$老板;
?>
```

## include 和 require ##
include 和 require 是 PHP 中的内置函数，用于包含外部文件。 include 和 require 的区别在于，如果文件不存在，include 会继续执行，而 require 会中断执行。
```php
<?php
// 文件名：index.php
echo "隔壁老王有限公司老板是：王总";
// 引入文件
require "隔壁老李有限公司.php";
?>
```
```php
<?php
// 文件名：隔壁老李有限公司.php
echo "隔壁老李有限公司老板是：李总";
```

# 其他深入的内容 #
摆烂了不写了，自己去看 [PHP 教程](https://www.w3school.com.cn/php/index.asp) ，[交个喷友(点这里)](http://6764.cn/)