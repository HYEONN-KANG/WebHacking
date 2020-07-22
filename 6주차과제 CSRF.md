<h1>CSRF ���� ���</h1>

CSRF(Cross Site Request Forgery)�� Ư�� ������� ������ Ż���ϴ� ������ �����Ͽ����� ��ũ���� ������ ���� �� ����� �� �ִ� ��ŷ ����̴�. �����ڰ� ��ũ��Ʈ�� ���� �Ͱ� ���ÿ� �ڱ⵵ �𸣰� Ư���� ����Ʈ�� ��� HTTP ��û(Request) �����͸� �����ٴ� ���� Ư¡�̴�.

![image](https://user-images.githubusercontent.com/62539341/82747656-41c1bf00-9dd6-11ea-8c47-d19d898d82ec.png)

�� ���� ���� ���� �ڱ⵵ �𸣰� �ٸ� ���� �ۼ� �ϰ� �ϴ� CSRF �����̴�.

![image](https://user-images.githubusercontent.com/62539341/82747664-5b630680-9dd6-11ea-95d2-5b3c34b66d3a.png)

<h3>CSRF ������ �ϱ� ���� ����</h3>
1. �ش� �� ����Ʈ�� ��Ű�� �̿��� ���� ����� ����ؾ� �Ѵ�.
2. �����ڰ� ������ �� �� ���� �Ķ���Ͱ� �����ϸ� �ȵȴ�.
  - �ڵ��Է� ���� ���ڸ� �־�� �ϴ� ��û�� �����ڰ� �̸� �� �� ����.
  - �н����� ���� ��ɿ��� ���� �н����带 �Է� �޴´ٸ�? �� ���� �����ڰ� �̸� �� �� ����.

<h3>Mitigation</h3>
CSRF ������ ���� ���� ���
1. ���� ��Ű ��� Ŀ���� ����� ����Ͽ� ����� ����
  - ����� �������� ���� ����� �߰��Ѵ�.(e.g. Authorization)
2. �����ڰ� ������ �� ���� �Ķ���� �߰� �� ����
  - Same Origin������ ���� ������ �����͸� ����
  - CAPTCHA
  - �������� ����ڸ� �ƴ� ������ ���� ����(��: ���� ��й�ȣ)

<h3>SameSite Cookie</h3>
CSRF ������ ������ ������ �� �������� ũ�ν� ����Ʈ, �� �ٸ� ����Ʈ�κ��� ���۵� ��û�� ��Ű�� �Բ� �����Ѵٴ� ���� �ִ�. �� �������� ��Ű�� �ٸ� ����Ʈ�� ���� ���۵� ��û�� ���������� SameSite ��Ű ������ ���� ����

ũ�ν� ����Ʈ���� ����� ��û�� ���������� ��Ű�� ���Խ�Ű�� �ϴ� �ɼ��̴�. �� 3����(Strict, Lax, Normal) ���� ������ �� �ִ�. �⺻������ Strict�� ��� ũ�ν� ����Ʈ���� ����� ��û�� �ش� ��Ű�� �������� �ʴ´�. Lax�� Link, Prerender, Form GET�� ������ ��û���� �������� �ʰ� Normal�� ������ ���� ��� ��û�� �����Ѵ�.

<h1>Wirte-up</h1>

<h3> 1. Root-me : CSRF- 0 protection</h3>
https://www.root-me.org/en/Challenges/Web-Client/CSRF-0-protection

�ϴ� ȸ�������ϰ� �α����ؼ� �����ʿ� �����Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82747947-e47b3d00-9dd8-11ea-9258-ef28aedf1897.png)

���� Status �� ��Ȱ��ȭ �Ǿ��ִ�. �ƹ����� Status�� Ȱ��ȭ ���Ѿ� ���ͳݿ� ���ᰡ���� �� ����.

![image](https://user-images.githubusercontent.com/62539341/82747965-0e346400-9dd9-11ea-8c6b-2bf800251ea8.png)

checkbox�� disabled�� abled�� �����غ��Ҵ�.

checkbox�� üũ�� �ϰ� submit�� �غ��Ҵ���

![image](https://user-images.githubusercontent.com/62539341/82747985-3de36c00-9dd9-11ea-8fc2-0ce9ec922a7a.png)

admin�� �ƴ϶�� �źδ��ߴ�.

```html
<form id="hello" action=��http://challeng01.root-me.org/web-client/ch22/index.php?action=profile�� method=��post�� enctype=��multipart/form-data��>                    
<input type="text" name="username" value="hello">
<input type="checkbox" name="status" checked>
</form> <script>document.getElementById("hello").submit();</script>
```

�̷��� contact�� �Է��ϰ� submit�� �����ôµ��� �ٲ� ���� ����.. �� �𸣰ڴ�.

<h3>2. xss challenge : #1 ~ #5</h3>
http://xss-quiz.int21h.jp/

![image](https://user-images.githubusercontent.com/62539341/82748952-db8e6980-9de0-11ea-84e4-d72d6340e276.png)

alert(document.domain) ���â�� ����� �����ΰ� ����. script �±׸� ����ؼ� �ٷ� ������Ѻ��Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82748985-1db7ab00-9de1-11ea-8f11-e48ab1cd1090.png)

![image](https://user-images.githubusercontent.com/62539341/82748996-2d36f400-9de1-11ea-950f-e63a0b58332b.png)

���â�� �� ���� �Ǿ���.

![image](https://user-images.githubusercontent.com/62539341/82749011-42138780-9de1-11ea-83f3-f07e697839e8.png)

�̹����� alert(document.domain) ���â�� ���� �����̴�.

![image](https://user-images.githubusercontent.com/62539341/82749029-5fe0ec80-9de1-11ea-97a5-95d33f6cb146.png)

�Ʊ�� ���� �Է��غ������� �����ߴ�.

![image](https://user-images.githubusercontent.com/62539341/82749067-acc4c300-9de1-11ea-9168-ee914d12fbc4.png)

��Ʈ�� Ȯ���غ��� ���� �±׸� �ݰ� ��ũ��Ʈ�� �߰��϶�� �Ǿ� �ִ�.

![image](https://user-images.githubusercontent.com/62539341/82749285-10032500-9de3-11ea-8c05-0f6856bb1ccd.png)

�̷��� �Է��� ���־���.

![image](https://user-images.githubusercontent.com/62539341/82749294-1beee700-9de3-11ea-9ee7-029607e35cd4.png)

![image](https://user-images.githubusercontent.com/62539341/82749318-5062a300-9de3-11ea-9207-c5bf04286ebf.png)

�̹����� ���â�� ���� ������ �� ������ ���� ������ �� �� �ִ�.

�ؽ�Ʈ â�� �ƹ��� �ص� ������ ������ �ʴ´�. ���� ���� �� �� �ִ� ĭ�� ���� �ִ°� �ƴ϶�� ������ �����. ���ö��� alert�� �����Ű�� ���� ������ ���� ������

![image](https://user-images.githubusercontent.com/62539341/82749385-e8608c80-9de3-11ea-9cb8-34fbc164bef5.png)

�ܼ�â�� �̷��� �־��־���.

![image](https://user-images.githubusercontent.com/62539341/82749407-029a6a80-9de4-11ea-8244-590653102493.png)

���� ���� ���ϴ� ��� �ɼǿ� alert�� ����! alert ������ �������ְ� �ƹ��ų� �Է��ѵ� search�� �������Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749428-2362c000-9de4-11ea-94c7-551cbafeeddd.png)

���!

![image](https://user-images.githubusercontent.com/62539341/82749439-39708080-9de4-11ea-95fe-4a696ca20dda.png)

3�� ������ ���� ������ ����� �ϰ� �ִ�. 3���� �Ȱ��� ����� �õ��غ��Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749459-5ad16c80-9de4-11ea-9b46-7800bb57a448.png)

![image](https://user-images.githubusercontent.com/62539341/82749471-7472b400-9de4-11ea-9188-d463f39faae1.png)

search Ŭ��!

![image](https://user-images.githubusercontent.com/62539341/82749492-89e7de00-9de4-11ea-83d3-fc1427a809ef.png)

�̹��� �� ����� �� ������ �ʴ� �� ����. 

������ �ҽ��� �ѹ� ���캸�Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749558-e945ee00-9de4-11ea-9adc-b9b206bee98d.png)

�ҽ� �߿� ���� ������ ������ �߰��ߴ�. type�� hidden�ε��ٰ�, value�� hackme�� �Ǿ� �ִ� �� ���� �� ���� �����غ��� �ڴ�. �켱 type�� hidden�� ���� text�� �ٲ㼭 �츮 ���� ���̰� ��������.

![image](https://user-images.githubusercontent.com/62539341/82749594-26aa7b80-9de5-11ea-9526-a74f6433f5ea.png)

�������ִ� p3�� �����ߴ�. �� ���� alert ������ �ְ� search�� �������Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749619-5194cf80-9de5-11ea-8535-1be851e6d98a.png)

����...

�Ʊ� 2�� Ǯ���� ������� �ٽ� �ѹ� �õ��غ��Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749695-eef00380-9de5-11ea-9b7d-2232e9defee0.png)

![image](https://user-images.githubusercontent.com/62539341/82749700-fb745c00-9de5-11ea-8917-a4e82ed32f91.png)

���...

![image](https://user-images.githubusercontent.com/62539341/82749732-32e30880-9de6-11ea-81b0-0de7ebb86b00.png)

������ �����ϱ� ��ư��� �����ϸ鼭 �⺻ script ������ �־�ô��� �ڿ� �ִ� ���ڵ��� �ƿ� ���󰡹��ȴ�.

![image](https://user-images.githubusercontent.com/62539341/82749754-5f972000-9de6-11ea-8a0b-d04b8a947e05.png)

maxlength�� 15�ۿ� �ȵǼ� �� ���ڵ��� �Է��� �ȵ� �� ����. �˳��� 60���� �÷��� �ٽ� �õ��غ��Ҵ�.

![image](https://user-images.githubusercontent.com/62539341/82749831-e3e9a300-9de6-11ea-9e72-3434dd725b7c.png)

![image](https://user-images.githubusercontent.com/62539341/82749836-eea43800-9de6-11ea-860f-785cab760344.png)