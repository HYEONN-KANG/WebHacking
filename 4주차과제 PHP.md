��ó : https://opentutorials.org/index.php/course/62

<h1>PHP ���� ���</h1>
<h3>PHP�� �����ΰ�?</h3>

![](https://grm-project-template-bucket.s3.ap-northeast-2.amazonaws.com/lesson/les_ZVCZS_1533200934311/39b799024e850d787d9eb469f4e7a8c5f892fa1b4425b937dc242dc4757dfbc9.png)

Client�� Server�� ��û, Server�� Client�� ��û�� �����ϴ� ������ �Ѵ�.

�츮�� ���� ���̹��� ���۰� ���� ����Ʈ�� ������ ��, �� ������(Web Browser)�� ����Ѵ�. �̰��� *Web Client*��� �θ���. �ݴ�� ���� �ʿ��� *Web Server*�� �����Ѵ�.

*Web Client*�� �������� ���̾�����, ���ͳ� �ͽ��÷ξ�, ũ��, ���ĸ� ���� �ִ�. *Web Server*�� �������� Apache, IIS, nginx ���� �ִ�.

���� ��� �����ο� o2.org/topic.php ��� ���� Enter Ű�� ������ Web  Server���� Ȯ���ڰ� php��� ���� Ȯ���ϰ�, �̰��� PHP engine ���� ������. PHP engine ���κ��� ������� Web Server�� ���� ������, �̰��� Web Client�� �����Ѵ�. �̷��� Web Server�� PHP engine ������ ��� �Ծ�, ����� CGI(Common Gateway Interface) ��� �Ѵ�.

PHP(Hypertext Preprocessor)�� �����ʿ��� ���� �Ǵ� ���α׷��� ���

PHP�� ����
1. ���� ����ȭ�� ���
2. �����߿� �ʿ��� ������ �������� �Լ��� ���·� �̸� ������
3. ���� ��� �����ͺ��̽��� ����
4. �������� �ʿ���� interpreter����� ���
----------------------------------------------------------------------------
<h3>ù��° PHP ���ø����̼�</h3>

Ȯ���ڸ��� .php�� ������ ������ �����غ���.

```php
<?php
echo "Hello world";
?>
```
echo�� �ڿ� ������� �����͸� ������ִ� ������ �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/79328251-ae80a880-7f50-11ea-8804-e0eb62b9db17.png)<br><br>

```php
<html>
<body>
echo "Hello world";
<?php
echo "Hello world";
?>
</body>
</html>
```
echo ������ php ���� ���̿� ���� ���� body �±� �ȿ� ���� �� ��� ����� �޶�����? 

![image](https://user-images.githubusercontent.com/62539341/79328008-5a75c400-7f50-11ea-803a-0e6f1d36f3cf.png)


----------------------------------------------------------------------------
<h3>������ �� ����ϴ� ����</h3>
�� �츮�� server side script�� ���°�?

Web Browser�� Web Server�� ��û�ϰ� �����ϴ� ������ ��ġ�� ���� ��â���� ����̾���. PHP�� Java, Python, perl ���� �����ʿ��� ����Ǵ� ������ ������.

�� �������� Web Browser�� ����ڿ��� ������ ������ ��, ������ ����ִ� �޼����� HTML �̴�. �׸��� HTML�� Server�� Client�� �ְ� �ޱ� ���� �Ծ��� HTTP�̴�.
URI, URL�� �츮�� �������� �ּ�â�� �Է��ϸ� �̿� �ش�Ǵ� HTML ������ ã�Ƽ� Ŭ���̾�Ʈ�� �� ������ �ٿ�ε� �� �� �ְ� �ȴ�.

�׷��� ���ͳ��� ���������� �����ϱ� �����ϸ鼭 ������ �߻��ϱ� �����ߴ�.
������Ʈ�� �����ϸ鼭 ���� ������� �̿��ϰ� �ǰ� Web Server �����δ� ��� ���� ó���ϱ⿡ ���ſ�����. �̶� ����� ���� �ٷ� CGI �̴�.

Web Server�� PHP, Java, Python, perl ���� ���α׷��� ��� ���̿� ���� Ŀ�´����̼��ϱ� ���� ��űԾ��� CGI�̴�.

PHP, Java, Python, perl ���� Web Browser�� ��û�� ���� HTML�� �ƴϸ� Web Server�� �� ������ ó���� �� ���� �ش� �� ȣ���ؼ� ����ڰ� ��û�� ������ �����Ѵ�. ���� ����� Web Server�� �Ű��� Web Browser���� ��ġ HTML�� ��ó�� �����ϴ� ���̴�.

DB�� �ش�Ǵ� ���� MySQL, ORACLE ���� �ִµ� �̰��� �����͸� �����ϴ� �Ϳ� Ưȭ�Ǿ� �ִ�. �����̳� �������� ���� �����Ͱ� �ʿ��ϸ� ���α׷��־� DB���� �ش� �����͸� �̾Ƽ� ����.
��������� �����ڰ� PHP������ �ϳ� �����, �����̳� ��������, ������ ���� ��������� ��� ����Ǵ� ���̴�.

----------------------------------------------------------------------------
<h3>���ڿ� ����</h3>

```php
<?php
echo 1;
?>
```
echo 1 �̶�� �ϸ� 1�̶�� ���ڸ� ȭ�鿡 ����Ѵ�
```php
<?php
var_dump(6);
?>
```
var_dump(������)�� �����Ͱ� ��� ���������� �����ش�.

![image](https://user-images.githubusercontent.com/62539341/79335610-43899e80-7f5d-11ea-89be-24b379d107b3.png)

```php
<?php
echo var_dump(1234);
echo var_dump("1234");
?>
```
php���� ���ڿ��� �ǹ��� ���� "" �Ǵ� ''�� ǥ���Ѵ�. 

![image](https://user-images.githubusercontent.com/62539341/79336240-551f7600-7f5e-11ea-8a56-728ba0b8cdd8.png)

```php
<?php
echo "hello"." "."world";
?>
```
���ڿ� ���ڸ� �����ϰ� �ʹٸ� �̷��� php������ ��Ư�ϰ� +��� .�� ����Ѵ�.

----------------------------------------------------------------------------
<h3>����</h3>

```php
<html>
<body>
<?php
$a=1;
echo $a+1; #2
echo "<br />";
$a=2;
print $a+1; #3
?>
</body>
</html>
```
php������ ������ ������ �� '$����'�� ���� �տ� $�� ���δ�. �ּ��� �� ���� #�� ���δ�. �ּ��� ������ �ް� ������ /**/�� ����ϸ� �ȴ�.
```php
<html>
<body>
<?php
$first = "coding";
echo $first." everybody";
?>
</body>
</html>
```
�̷��� ���� �ȿ��� ���� �Ӹ� �ƴ϶� ���ڿ��� �� �� �ִ�.<br><br>

�츮�� ������ �� ���� �ɱ�?
```php
<html>
<body>
<?php
echo 100+10;
echo '<br />';
echo (100+10)/10;
echo '<br />';
echo ((100+10)/10)-10;
echo '<br />';
echo (((100+10)/10)-10)*10;
echo '<br />';
?>
</body>
</html>
```
�� �ڵ忡�� 100�� 1000���� �ٲ�� �Ѵٸ�?
���� ���ŷӰ� ������. ������ ������ ����Ѵٸ� ������ ���� �������ָ� �ǹǷ� ���ϴ�.
```php
<html>
<body>
<?php
$a = 100;
$a = $a + 10;
print $a.'<br />';
$a = $a / 10;
print $a.'<br />';
$a = $a - 10;
print $a.'<br />';
$a = $a * 10 ;    
print $a.'<br />';
?>
</body>
</html>
```
```php
<html>
<body>
<?php
define('TITLE', 'PHP Tutorial');
echo TITLE;
define('TITLE', 'JAVA Tutorial');
?>
</body>
</html>
```
����� ������ �ٸ��� ���� ������ �� ����. ù��° define���� ��� TITLE�� PHP Tutorial �̶�� ���� �����ߴ�. �׷��� �� �ؿ� �ٽ� ��� TITLE�� �ٸ� ���� ������ �����Ƿ� ���⼭ error�� �߻��Ѵ�.

������ ��� ������ ���� �˻��ϰ� �����ϱ�
```html
<html>
<body>
<?php
$a = 100;
echo gettype($a);
settype($a, 'double');
echo '<br />';
echo gettype($a);
?>
</body>
</html>
```
------------------------------------------------------------------
<h3>��</h3>
���α׷��ֿ��� �񱳶� �־��� ������ ������, �ٸ���, ū��, �������� �����ϴ� ���� �ǹ��Ѵ�. �� �� �� �����ڸ� ����ϴµ� �� �������� ����� true�� false ���� �ϳ���. -> ���������� Boolean !

1. "=="  : ���װ� ������ ���� ���ٸ� true, �ٸ��� false
2. "!="  : ==�� ����� ���ݴ�
3. ">"   : ������ ���� ������ ������ ũ�ٸ� true, �ƴϸ� false
4. ">="  : ������ ���� ������ ������ ũ�ų� ���ٸ� true, �ƴϸ� false
5. "<"   : ������ ���� ������ ������ ������ true, �ƴϸ� false
6. "<="  : ������ ���� ������ ������ �۰ų� ���ٸ� true, �ƴϸ� false
7. "===" : ���װ� ������ ���� '��Ȯ�ϰ�' ���ٸ� true, �ƴϸ� false

------------------------------------------------------------------
<h3>����� �׸��� ���� HTTP</h3>
���α׷��� �Է� ���� ���� �� �ִ�. �׸��� �Է� ���� ���� ���� ����� �޶����ų� �Էµ� ���� ����/����/��� �� �� �ִ�. �̹� �ð����� PHP�� ������ ���� ���뿡�� ��� �������ͼ� PHP ���ø����̼��� �����͸� �Է� �޴� ����� ���ؼ� �˾ƺ���.

```php
<?php
echo $_GET['id'];
?>
```
ó�� ���� $_GET[]�� �����ϴ� �� ������ �̰��� �迭(array)�̶�� �͸� �˰� �Ѿ��. �� �ڵ带 �����غ���

![image](https://user-images.githubusercontent.com/62539341/79403993-6783c900-7fcb-11ea-8f3a-d7b57df3971d.png)

�̷��� URL�� �̻��ϴ�. ���⼭ egoing�� k8805�� �ٲٸ� ȭ�鿡 egoing ��� k8805�� ��µȴ�. ��, �Է��� ���� ���� �ٸ� ��°��� �������� User�� ��ȣ�ۿ��ϴ� ���ø����̼��� �Ǿ��ٶ�� ���̴�.<br>

URL�� �ִ� *localhost/�����.php?id=egoing*�� �ѹ� ���캸��.<br>
�����.php��� php ���ø����̼��� ã�Ƴ��� �ּҰ� *localhost/�����.php*��� ?�� �������� �ڿ� �ִ� *id=egoing* �� �ּҰ� ����Ű�� php ���ø����̼����� ���޵Ǵ� ���� ������ �����̴�.<br>
���⼭ �ٽ�, *id=egoing*�� ���캸��, =�� �������� �տ� �ִ� id �� ���� ���� �̸��̰�, = �ڿ� �ִ� egoing�� ���̴�.

���� �� �����ϰ�, �̹��� password���� �Է¹޾ƺ���.
```php
<?php
echo $_GET['id'].','.$_GET['password'];
?>
```

![image](https://user-images.githubusercontent.com/62539341/79404830-bfbbca80-7fcd-11ea-8275-39a90efd9565.png)

 &�� ���� ���� �����ϴ� �������̴�.

�׷��� �Ź� �̷��� ����ڰ� id�� password���� ������ URL�� ��� �����ϴ� ���� �ſ� �����ϴ�. �׷��� ����ϴ� ���� �ٷ� ��(form)�̴�.

```html
<html>
<body>
    <form method="get" action="2.php">
        id :  <input type="text" name="id" />
        password :  <input type="text" name="password" />
        <input type="submit" />
    </form>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/62539341/79405358-25f51d00-7fcf-11ea-974e-6185e38f25ad.png)

![image](https://user-images.githubusercontent.com/62539341/79406374-e11eb580-7fd1-11ea-85ac-450268f092ab.png)
<br><br>

�̹��� Get ��İ� Post ����� �������� ���� ���캸��. ���ݱ��� �츮�� ����� ���� Get ����̴�.

get ������� �����͸� ������ �� URL�� �����͸� ���Խ�Ű�� ���� ���ؼ� POST ������� �����͸� ������ ���� �����ϴ� �����͸� URL�� ���Խ�Ű�� �ʰ� ���� �� �� �ִ�. �̷��� ���̷� ���ؼ� GET ����� ������ ���� ��ũ�� ���� ���ǰ�, POST ����� ������� ���̵� ��й�ȣ�� ���� �����͸� �����ϴ� ������� �ַ� ����Ѵ�.

```html
<html>
<body>
    <form method="POST" action="4.php">
        id :  <input type="text" name="id" />
        password :  <input type="text" name="password" />
        <input type="submit" />
    </form>
</body>
</html>
```
```php
<?php
echo $_POST['id'].','.$_POST['password'];
?>
```

![image](https://user-images.githubusercontent.com/62539341/79406460-1c20e900-7fd2-11ea-9121-14af3c0ae040.png)
�̷��� �Ʊ�ʹ� �ٸ��� URL�� �����Ͱ� �巯���� �ʰ� �ȴ�.

------------------------------------------------------------------
<h3>���ǹ�</h3>

php���� ���ǹ��� �⺻ ������ �ٸ� ���α׷��� ���� �����ϴ�.
```php
<?php
if(����){
    ������ true��� ������ ���
}
?>
```

<br>
���ǹ��� �����غ���.

```html
<html>
<body>
    <form method="post" action="13.php">
        id :  <input type="text" name="id" />
        password : <input type="password" name="password" />
        <input type="submit" />
    </form>
</body>
</html>
```
```php
<?php
if($_POST['id'] === 'egoing'){
    if($_POST['password'] === '111111'){
        echo 'right';
    } else {
        echo 'password wrong';
    }   
} else {
    echo 'id wrong';
}
?>
?>
```
id�� password�� ���� �Է¹޾� ���ǹ��� �̿��ϸ�, ���� �´��� Ȯ���� �� �ִ�. <br>���ǹ��� ��ø ����!

���ǹ��� ����� �� �ִ� �� ������

1. and : and�� ���װ� ������ ��� ��(true)�� �� ���̵ȴ�. &&�� ����ص� �ȴ�.
2. or  : or�� or�� �¿��� �߿� �ϳ��� true��� true�� �Ǵ� �� �����ڴ�.
3. !   : !(not)�� ������ �ǹ̷�, true�� false�� false�� true�� �����.

------------------------------------------------------------------
<h3>�ݺ���</h3>

�ݺ������� ���� ���� ���Ǵ� ���� while�� for�� �ִ�.

while���� ������ ������ ����.
```php
while(����){
    �ڵ�
    �ڵ�
}
```
(��)
```php
<?php
# i�� ������ 0�� �Ҵ��Ѵ�. 
$i = 0;
# ������������ i�� ���� 5���� �۴ٸ� true, ���ų� ũ�ٸ� false
while($i < 5){
    echo 'coding everybody';
    # �ݺ����� ����� ������ i�� ���� 1�� ������Ų��. �� ��� i�� ���� 5�� �Ǹ� ���������� false�� �Ǹ鼭 �ݺ����� ����ȴ�.
    $i += 1;
}
?>
```

![image](https://user-images.githubusercontent.com/62539341/79409512-1e3a7600-7fd9-11ea-8ca4-231f1c0dd7cb.png)

for���� ������ ������ ����.
```php
for(�ʱ�ȭ; �ݺ� ���� ����; �ݺ� ����){
    �ڵ�;
}
```
(��)
```php
<?php
for($i = 0; $i < 10; $i++){
    echo 'coding everybody'.$i."<br />";
}
?>
```

![image](https://user-images.githubusercontent.com/62539341/79409578-43c77f80-7fd9-11ea-8a4a-7a68145c2f4a.png)<br><br>

�ݺ��۾��� �߰��� �ߴܽ�Ű�� �ʹٸ� ��� �ؾ��ұ�?  break�� ����ϸ� �ȴ�. �Ʒ��� ������ ������ ���캻 ������ �Ϻ� ������ ���̴�.
```php
<?php
for($i = 0; $i < 10; $i++){
    if($i === 5){
        break;
    }
    echo "coding everybody{$i}<br />";
}
?>
```

![image](https://user-images.githubusercontent.com/62539341/79409746-a6208000-7fd9-11ea-959a-62f087a11e02.png)

�׷� ������ ��� �ߴ� �ϸ鼭 �ݺ��� ���ӵŰ� �Ϸ��� ��� �ؾ� �ұ�? continue�� ����ϸ� �ȴ�.
```php
<?php
for($i = 0; $i < 10; $i++){
    if($i === 5){
        continue;
    }
    echo "coding everybody{$i}<br />";
}
?>
```

![image](https://user-images.githubusercontent.com/62539341/79409945-19c28d00-7fda-11ea-917c-7ef2edcd8722.png)

------------------------------------------------------------------
<h3>�Լ�</h3>
�Լ�(function)�� �ϳ��� ������ ����� �� �� �ֵ��� �ϴ� ������ �ڵ��� ���뼺�� �����ش�. �� ���ĺ��� �����ϴ� �Լ��� ��ü����� ���� ������� �װ� ��ü�� ���α׷����� �����̳� ���� ���������� �����ϴ� ���̶�� ���ٴ� ����� ���� �ڵ带 �ٿ��ְ�, ���������� �����ϰ�, ���װ� �߻��� ������ �ٿ��ִ� �͵��̶�� �� �� �ִ�. 

�Լ��� ����
```php
function �Լ���( [����...[,����]] ){
   �ڵ�
   return ��ȯ��;
}
```
(��)
```php
<?php
function get_member1(){
    return 'egoing';
}
 
 
function get_member2(){
    return 'k8805';
}
 
echo get_member1();
echo ',';
echo get_member2();
?>
```

![image](https://user-images.githubusercontent.com/62539341/79410253-d3216280-7fda-11ea-9e9a-3094800ce6f3.png)

<br>
�̷��� �Լ��� ���ڰ��� �޾Ƽ� �����ų ���� �ִ�.

```php
<?php
function get_arguments($arg1, $arg2){
    return $arg1 + $arg2;
}
echo get_arguments(10, 20);
echo get_arguments(20, 30);
?>
```
------------------------------------------------------------------
<h3>�迭</h3>
�迭�̶� ������ �����͸� ��Ƽ� �����ϱ� ���ؼ� ����ϴ� ������ Ÿ���̴�. ������ �ϳ��� �����͸� �ӽ÷� �����ϱ� ���� ���̶�� �迭�� ���� ���� �����͸� �����ϱ� ���� ���̶�� �� �� �ִ�.

```php
<?php
$member = ['egoing', 'k8805', 'sorialgi'];
?>
```
```php
<?php
$member = array('egoing', 'k8805', 'sorialgi');
?>
```
�ϳ��� ������ 3���� �����͸� ��Ҵ�. ������ �����͸� ���(element)��� �θ���. 

�迭�� �ݺ����� ����ϸ� ���� ���ϴ�!
```php
<?php
function get_members(){
    return ['egoing', 'k8805', 'sorialgi'];
}
 
$members = get_members();
 
for($i = 0; $i < count($members); $i++){
    echo ucfirst($members[$i]).'<br />';
}
 
?>
```
<br>
�迭�� ������ �����͸� ȿ�������� ����, �����ϱ� ���� �������� ��ȵ� ������ Ÿ���̴�. ���� �������� �߰�/����/������ ���� ���� ���ϰ� �� �� �ֵ��� ���� �پ��� ����� ������ �ִ�. ��� �߿��� ��ɵ鸸 ���캸��.

1. �迭�� ũ��
```php
<?php
$l = [1, 2, 3, 4, 5];
echo count($l);
?>
```
2. �迭�� �߰�
```php
<?php
$arr = ['a', 'b', 'c', 'd', 'e'];
array_push($arr, 'f');
var_dump($arr);
?>
```
������ �����͸� �߰��Ϸ���
```php
<?php
$li = ['a', 'b', 'c', 'd', 'e'];
$li = array_merge($li, ['f','g']);
var_dump($li);
?>
```
������ �迭�� �������� �������� �߰��ϴ� ����̴�. �迭 li�� z, a, b, c, d, e�� �ƴ�. insert�� ù��° ���ڴ� �߰��� �������� ��ġ�� �ǹ��ϰ� �ι�° ���ڴ� �߰��� ���� �ǹ��Ѵ�.
```php
<?php
$li = ['a', 'b', 'c', 'd', 'e'];
array_unshift($li,'z');
var_dump($li);
?>
```
���� �ι�° �ε��� �ڿ� �빮�� B�� �ְ� �ʹٸ� �Ʒ��� �����Ѵ�.
```php
<?php
$li = ['a', 'b', 'c', 'd', 'e', 'z'];
array_splice($li, 2, 0, 'B');
var_dump($li);
?>
```
3. �迭�� ����

������ �迭�� ù��° ��Ҹ� �����ϴ� ����̴�. 
```php
<?php
$li = ['a', 'b', 'c', 'd', 'e', 'z'];
array_shift($li);
var_dump($li);
?>
```
������ �迭�� ������ ��Ҹ� �����ϴ� ����̴�. 
```php
<?php
$li = ['a', 'b', 'c', 'd', 'e', 'z'];
array_pop($li);
var_dump($li);
```
4. �迭�� ����

������ �����ϴ� ����̴�. ����� a, b, c, d, e ��.
```php
<?php
$li = ['c','e','a','b','d'];
sort($li);
var_dump($li);
?>
```
�������� �����ϰ� ������
```php
<?php
$li = ['c','e','a','b','d'];
rsort($li);
var_dump($li);
?>
```
<br>
���ݱ��� ���캻 �迭�� �����ۿ� ���� �ĺ��ڷ� ���ڸ� ����ߴ�. �����Ͱ� �߰��Ǹ� �迭 ��ü���� �ߺ����� �ʴ� �ε����� �ڵ����� ��������� �� �����Ϳ� ���� �ĺ��ڰ� �Ǵ� ���̴�. PHP������ �ε����� ���ڸ� ����ϴ� �͵� �����ϴ�. �Ϲ������� �ٸ� ������ ���ڸ� �ε����� ����ϴ� ���� �Ϲ������� �迭, Ȥ�� indexed array��� �ϰ�, ���ڸ� �ε����� ����ϴ� ���� �����迭(associative array, hash, dictionary)��� �θ����� PHP������ �̸� Ư���� �������� �ʰ� �ֱ� ������ �ϳ��� �迭�� Ű ������ ���ڿ� ���� ��θ� ����� �� �ִ�.

```php
<?php
$grades = array('egoing'=>10, 'k8805'=>6, 'sorialgi'=>80);
?>
```
���� �������� egoing�� key�� �ǰ�, 10�� value�� �ȴ�.
```php
<?php
$grades = [];
$grades['egoing'] = 10;
$grades['k8805'] = 6;
$grades['sorialgi'] = 80;
var_dump($grades);
?>
```
�� ������ε� �����迭�� ���� �� �ִ�.
```php
<?php
$grades = array('egoing'=>10, 'k8805'=>6, 'sorialgi'=>80);
echo $grades['sorialgi'];
?>
```
�̷��� key ���� ���� �� �� �ִ�. �� ����� 80�̴�.

�ݺ����� �Բ� ����� ���� �ִ�.
```php
<?php
$grades = array('egoing'=>10, 'k8805'=>6, 'sorialgi'=>80);
foreach($grades as $key => $value){
    echo "key: {$key} value:{$value}<br />";
}
?>
```
����� �Ʒ��� ����.

![image](https://user-images.githubusercontent.com/62539341/79411674-64de9f00-7fde-11ea-8f9d-806dbad91769.png)

-----------------------------------------------------------------

<h1>Write-up</h1>

1. webhacking.kr old 6

![image](https://user-images.githubusercontent.com/62539341/79440002-7771cc00-8010-11ea-99f6-8150dfa13f9f.png)

view-sourc�� Ŭ��!

![image](https://user-images.githubusercontent.com/62539341/79440499-0aab0180-8011-11ea-81da-302c09323402.png)

���� id�� guest, pw�� 123qwe�� ����Ǿ��ִ�. �׸��� for���� ���캸��, id�� pw�� base64_encode�� 20�� �ݺ��Ѵ�...

![image](https://user-images.githubusercontent.com/62539341/79441594-65912880-8012-11ea-8768-3117cf678746.png)

�� �κ��� ���ϱ� decode_id�� admin �̰� decode_pw�� nimda�̸� ������ �ذ�Ǵ� �� ����.

�켱 encode�� decode�� �������� �� �𸣰ھ ã�ƺ��� encode�� ��ȣȭ, decode�� ��ȣȭ��� ���� �˰� ���.

�ٽ� �ι�° ������ ���� ��, ��ȣȭ�� �� ���ڵ��� ���� ���� admin, nimda �̾�� �Ѵ�. �׷����� ���ڵ��ϱ� ��, ���ڵ��� ���� admin, nimda�� �ٲ��... ���� ������?

php online compiler ����
```php
 $val_id="guest";
  $val_pw="123qwe";
  for($i=0;$i<20;$i++){
    $val_id=base64_encode($val_id);
    $val_pw=base64_encode($val_pw);
  }
```
�� �κ��� ��¦ �ٲ㼭 admin�� nimda�� 20�� ���ڵ��� ���� ��Ű user�� password�� ���� �ְ� ���ΰ�ħ�ߴµ� 

![image](https://user-images.githubusercontent.com/62539341/79446600-69747900-8019-11ea-8df8-71bd66f722e1.png)

������ ���� ������ Ǯ�� ���ߴ�.. �������� ���Ϸ� �ؼ� �׷��� �����ϰ� ũ������ �����ؼ� �ٽ� �õ��غôµ� �Ȱ��� ������ ����...

2.webhacking.kr old-33

view-source Ŭ��!

![image](https://user-images.githubusercontent.com/62539341/79446940-0d5e2480-801a-11ea-8972-11c021adb043.png)

�̹��� ��û �ڵ尡 �����غ��̴µ�..

php ���θ� ���캸�� GET ������� ���� get�� hehe�� ���� �Է¹�����
echo�� ����?�� ����ϴ� �� ����.

![image](https://user-images.githubusercontent.com/62539341/79447450-d2a8bc00-801a-11ea-8f5a-6464bb3f07fa.png)

�̷��� get�� hehe�� �Է��ϴϱ� Next ��ư�� �����! Next Ŭ��!<br><Br>

![image](https://user-images.githubusercontent.com/62539341/79447641-20bdbf80-801b-11ea-8592-bb5d5f0e1707.png)

�̹��� POST ������� post�� hehe, post2�� hehe2�� �Է��ϸ� ���� �ܰ�� �Ѿ�°�����.

![image](https://user-images.githubusercontent.com/62539341/79452530-3cc55f00-8023-11ea-97e5-476d726797ea.png)

�̷��� ���� html �ڵ忡 �� �ڵ带 �߰��ؼ� post�� submit �� �� �ְ� �Է�ĭ �ΰ��� submit ��ư�� �������.

![image](https://user-images.githubusercontent.com/62539341/79452630-65e5ef80-8023-11ea-9210-49ee152b706d.png)
Next!<br><br>

![image](https://user-images.githubusercontent.com/62539341/79452725-92017080-8023-11ea-99f1-36f591736580.png)

GET������� myip�� REMOTE_ADDR�� �Է��ϸ� ������ Ǯ���� �� ����.
�Ȱ��� �Է��ߴµ�... ���� �ƴ϶�� ���Դ�.

ã�ƺ��� REMOTE_ADDR�� �� ip �ּҸ� �Է��϶�� ���� �˰� �Ǿ���.
�ٽ� ip �ּҸ� �Է��ϴϱ� ���� �ذ�!

![image](https://user-images.githubusercontent.com/62539341/79453363-9417ff00-8024-11ea-8677-10f80619932f.png)

<br>���� 4��° ������.
![image](https://user-images.githubusercontent.com/62539341/79453408-a2feb180-8024-11ea-8d17-c9bc8c593ea9.png)

hint�� �����ִ�.. ���� ��� ������ �𸣴� �ϴ� view-source

![image](https://user-images.githubusercontent.com/62539341/79453487-bc9ff900-8024-11ea-9547-413ee749b8be.png)

�̹����� GET ������� password �� ���� �Է��ϴ� ������
�׷��� md5�� ó�� ���� ���̴�. 

![image](https://user-images.githubusercontent.com/62539341/79453926-55cf0f80-8025-11ea-8d4c-05327208cfdf.png)

���ۿ� �˻��ؼ� hint�� ���ڸ� �����ϱ� ������ ������ ģ������ ����. �� ģ������ password�� �־���. �ٵ� �ð��� ������ ���ڰ� �ٲ� ���ڸ� �˳��ϰ� �����ߴ�. Ÿ�ֿ̹� ���缭 ���ΰ�ħ�ϴϱ� ������ Ǯ�ȴ�!

![image](https://user-images.githubusercontent.com/62539341/79454324-f7566100-8025-11ea-911f-1d98b853965e.png)<br><br>

![image](https://user-images.githubusercontent.com/62539341/79454361-0d642180-8026-11ea-9b13-d3b5e8c93d90.png)

�̹��� GET�̶� POST�� COOKIE�� �ٰ��� �ִ� ������.

�ϴ� GET�� imget�� URL�� �߰��ϸ� �ǰ� POST �κ��� �ذ��ؾ� �Ǵϱ� ������ �ҽ��� ���� ������ �ʿ䰡 �ִ�.

![image](https://user-images.githubusercontent.com/62539341/79455843-751b6c00-8028-11ea-925a-c1e2e70a1b70.png)


�̷��� post �� �� �ְ� �ڵ带 �߰��ߴ�.

���� imcookie�� �̸����� ��Ű�� ������� ����!

![image](https://user-images.githubusercontent.com/62539341/79455272-962f8d00-8027-11ea-9402-a533cabe345e.png)

![image](https://user-images.githubusercontent.com/62539341/79455918-9419fe00-8028-11ea-8ce1-e85c1c95bdd9.png)

submit�� �ϴ� ���!<br><br>

![image](https://user-images.githubusercontent.com/62539341/79455991-b27ff980-8028-11ea-84fe-e637e4599948.png)

�̹� �������� hint�� �����ִ�. ���������� Ư�� ���ڸ� �����س����ǰ�?

![image](https://user-images.githubusercontent.com/62539341/79456103-dfcca780-8028-11ea-87bf-45b2458e5d5b.png)

��Ű�� ����Ʈ ����� �̿��ؼ� ������ Ǯ��� �ǰڴ�.

�� ip�ּҸ� ���� ��Ű 'test'�� ����,
�׸��� ���� post ������� hint�� ���� ���ڸ� �־�� �ڴ�.

![image](https://user-images.githubusercontent.com/62539341/79457473-3b983000-802b-11ea-98f6-26b2c5ef709b.png)

���� �ƴ϶�� ����� ����. ��� Ǯ��� �Ǵ� ���� �� �𸣰ڴ�...
