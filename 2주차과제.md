��ó : ��Ȱ�ڵ�

```html
<h1>������ ����</h1>
�츮 ��δ� <strong>�ڽ��� ��</strong>���� �߰��� ������ ���� ���� ������.(���ε� Ŀ����)
```
<h1\> �̶�� �±׸� ���� �� �������� ������ ������ �������� ó���Ѵ�. <h1\>�� ���������� ���� ū ���ڷ� �ٸ��ְ� �ٹٲ��� �ѹ� �Ѵ�. (<h1\>�� <h2\>�� �ٲٸ� �۾��� ���� �۾�����.)

<strong\> �̶�� �±״� �ܾ ����, ���ϰ� ǥ���Ѵ�.

���⼭ <strong\>�� �����±�, </strong\>�� ������ �±��̴�.

<a\> �±׸� �ɾ� ���ڰ� ��ũ��� ����� �˷��ְ� �� �������� �̵��� �� �ֵ��� �Ѵ�.

```html
<a href="https://www.google.co.kr/" target="_blank" title="����Ȩ������">����</a>
```
target�� '����'�� Ŭ������ �� �ش� �� ���������� �ٷ� ��ũ�� ���� �ʰ� ���� �ǿ��� ��ũ�� ���� �������� �Ѵ�.

title�� ���콺 �����͸� '����'���� �÷� ������ ����Ȩ������ ���尡 �ߵ��� �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/82145108-75a35e80-9883-11ea-9f7f-c98e1bca55ff.png)


<li\> �±׸� ����ϸ� ������� ǥ��<br>
<ul\> �±׷� ���� ������ �±׸� ���� grouping �� �� �ִ�.<br>
<ol\>�� ���ڰ� �ٰ� <ul\>�� ���ڰ� ���� �ʴ´�.

�±׿� �±״� ��ø�ؼ� ��� �����ϴ�.

```html
<ol>
    <li>����Ұ�</li>
    <li>�⺻����</li>
    <li>�������ؽ�Ʈ�� �Ӽ�</li>
    <li>����Ʈ�� �±��� ��ø</li>
</ol>
<ul>
    <li>������</li>
    <li>������</li>
    <li>���̶�</li>
    <li>������</li>
</ul>
```

![image](https://user-images.githubusercontent.com/62539341/82145202-12fe9280-9884-11ea-8fbf-6455759a38cc.png)

<title\> �±׸� �̿��ؼ� �� ������ ������ ���ְ� ������ �� �ִ�.

�۾��� �̻��ϰ� ������ ��찡 ���� ���� <meta charset="utf-8"> �±׸� �߰����ָ� �� ������ ���� �� �ִ�.

html�� �ΰ����� ������ ������ ���� �ٸ� �±׿� �㵵�� ����ߴ�.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>HTML - ����</title>
        <meta charset="utf-8">
    </head>
    <body>
        <h1>HTML</h1>
        <ol>
            <li>����Ұ�</li>
            <li>�⺻����</li>
            <li>�������ؽ�Ʈ�� �Ӽ�</li>
            <li>����Ʈ�� �±��� ��ø</li>
        </ol>
        <ul>
            <li>������</li>
            <li>������</li>
            <li>���̶�</li>
            <li>������</li>
        </ul>
        HTML�� �����մϴ�.
    </body>
</html>
```

������ �ƴ� ���� <head\>�±� �ȿ�, ������ <body\>�±� �ȿ� ���´�. 

�׸��� <head\>�� <body\>�� <html\>�±׷� �����ش�.

<\!DOCTYPE html\>�� document type declaration �� ����

�ڽ��� �ۼ��� html �ڵ尡 � ����� html �ڵ�� �ۼ�������� �����ϴ� ���̴�.

![image](https://user-images.githubusercontent.com/62539341/82145298-c9627780-9884-11ea-9152-ab5927305cf1.png)

<p\> �±״� paragraph �� ���Ӹ��� �ܶ��̶� ���̴�. <p\> �±׸� �̿��Ͽ� �ܶ��� ������ �� �ִ�.<br>
<br\> �±׸� �̿��ϸ� �ٹٲ��� �� �� �ִ�.

```html
<html>
    <body>
        <meta charset="utf-8">
        <p>
            Hypertext Markup Language (HTML) is the standard markup language for documents designed to be displayed in a web browser. 
            hnologies such as Cascading Style Sheets (CSS) and scripting languages such as JavaScript.
        </p>
        <p>
            Web browsers receive HTML documents from a web server or from local storage and render the documents into multimedia web pages. 
            HTML describes the structure of a web page semantically and originally included cues for the appearance of the document.
        </p>
        <p>
            HTML elements are the building blocks of HTML pages. With HTML constructs, images and other objects such as interactive forms 
            may be embedded into the rendered page. HTML provides a means to create structured documents 
            by denoting structural semantics for text such as headings, paragraphs, lists, links, quotes and other items. <br>
            HTML elements are delineated by tags, written using angle brackets. Tags such as <img\> and <input\> directly introduce content into the page. 
            Other tags such as <p\> surround and provide information about document text and may include other tags as sub-elements. 
            Browsers do not display the HTML tags, but use them to interpret the content of the page.
        </p>
        <img src="img.jpg" height="300" alt="�̹���" title="image">
    </body>
</html>
```

<img\>�� ���� �̹����� �� �������� ��Ÿ�� �� �ִ�. height�� ����, width�� ���� �����ؼ� ������ ũ�⸦ ������ �� �ִ�. alt��� �Ӽ��� ����ϸ� �̹����� ������ �� �ؽ�Ʈ�� ǥ�����ش�. title�� ���콺 �����͸� ���� ���� �÷��� �� �ؽ�Ʈ�� ǥ�����ش�.

![image](https://user-images.githubusercontent.com/62539341/82179911-66232480-991a-11ea-9a37-73b3e5acc8fa.png)

form�� ����ڰ� �Է��� ������ ������ ������ �� ����ϴ� ���̴�.

<input\>���� ������� �Է��� �޾ƿ� �� �ִ�.

text�� ������ �����ϸ� ����ڰ� �Է��ϴ� text�� �޾ƿ� �� �ִ�.

password�� type�� �ϸ� ����ڰ� �Է��ϴ� ���ڴ� ������ �ʴ´�.

submit�� ���� ��ư�� �������ش�.

����ڰ� �Է��� ������ ���� ���� ���ΰ��� form �±� �ȿ� ���ָ� �ȴ�.

-----------------------------------------------------------------
<h2>write-up</h2>

<h3>HTML- source code</h3>

![image](https://user-images.githubusercontent.com/62539341/98460098-97532200-21e4-11eb-94d5-b0b9a9c0644e.png)

출처:https://www.root-me.org/en/Challenges/Web-Server/HTML-source-code

![image](https://user-images.githubusercontent.com/62539341/98460145-f6189b80-21e4-11eb-8379-be96e5d25172.png)

주석 부분에 password가 nZ^&@q5&sjJHev0라고 적혀있다.

<h3>Webhacking.kr old-1번</h3>

![image](https://user-images.githubusercontent.com/62539341/98460172-47c12600-21e5-11eb-937a-bc76d9fedab2.png)

출처:https://webhacking.kr/challenge/web-01/

view-source를 눌러 코드를 확인해보았다.

![image](https://user-images.githubusercontent.com/62539341/98460268-2f9dd680-21e6-11eb-83d6-f82e18d694ec.png)

user_lv 쿠키값이 6보다 크거나 같으면 쿠키값은 1이 되고, 쿠키값이 5보다 크면 solve(1) 이 실행되는 것을 보아 해결이 되는 것 같다. 그럼 5보다는 크고 6보다는 작은 수를 쿠키에 넣으면 된다.

![image](https://user-images.githubusercontent.com/62539341/98460284-6bd13700-21e6-11eb-90f6-a38a00b2574b.png)

<h3>HTML disabled</h3>

![image](https://user-images.githubusercontent.com/62539341/98460329-d5514580-21e6-11eb-85c7-26082dae59c0.png)

지금 저 텍스트상자를 눌러보니 제대로 작동하지 않는다. 버튼도 마찬가지다.
이번에도 페이지 소스를 확인한다.

![image](https://user-images.githubusercontent.com/62539341/98460356-0c275b80-21e7-11eb-8e12-c1af48972a71.png)

disabled 라는 키워드 때문에 현재 접근이 불가능한 것 같다. disabled를 없애보았다.

![image](https://user-images.githubusercontent.com/62539341/98460384-57da0500-21e7-11eb-9146-5ee5291e9865.png)

텍스트박스와 버튼이 활성화되었고, 아무 글자를 입력해보니 문제가 해결되었다.