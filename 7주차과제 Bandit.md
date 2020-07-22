��ó : https://overthewire.org/wargames/bandit/

![image](https://user-images.githubusercontent.com/62539341/83342096-0703dd80-a326-11ea-8f68-d1f1ff33baee.png)

<h3>Level 0</h3>

SSH�� ����ؼ� bandit0�� �α����ؾ� �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/83342176-fd2eaa00-a326-11ea-937a-b03632cf4571.png)

> ssh bandit0@bandit.labs.overthewire.org -p2220 

(ssh������ ��Ʈ2220�� ����ؼ� �����ϰڴ�) 

![image](https://user-images.githubusercontent.com/62539341/83342301-c78ac080-a328-11ea-887b-08a8eb863162.png)

�׷��� ��й�ȣ�� �Է��϶�� �ߴµ� ������ �����ִ´�� badit0�� �Է����ָ� �ȴ�. ��й�ȣ�� �Է��� �� ȭ�鿡 ��й�ȣ�� �ԷµǴ��� ������ �ʾ� �ԷµǴ°ǰ� �򰥷ȴµ� ������ ���ȱ���ΰ�����. ��й�ȣ�� �Է��ϸ� ������ ���� badit0�� �α��εȴ�.

![image](https://user-images.githubusercontent.com/62539341/83342318-015bc700-a329-11ea-86fd-e981bb91c4b6.png)


<h3>Level 0 -> Level 1</h3>

SSH�� badit1�� �α����� �ؾ� �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/83342145-9c9f6d00-a326-11ea-8c59-28bba9e3c45f.png)

���� ������ ���� ���� �н������ readme�� �ִٰ� �Ѵ�. �ؿ� �� ������ Ǯ�� ���� ls, cd, cat, file, du, find ��ɾ ����ؾ� �Ѵٰ� �����ִ�.

- ls : ���� ���丮�� �ִ� ����(���丮, ����)���� Ȯ��
  - ls - a : ������ ���丮�� ���� ��� Ȯ��
  - ls - l : �ڼ��� ���� Ȯ��
- cd : ���丮�� �̵�
  - cd . : ���� ���丮
  - cd .. : �� �ܰ� ���� ���丮
  - cd / :�ֻ��� ���丮
- cat :  ���� ������ ���
- file : ������ ����(type)�� Ȯ��
- du : disk usage�� ���ڷν� ���� ���丮 Ȥ�� ������ ���丮�� ��뷮�� Ȯ��
- find : ���� �� ���丮�� �˻�

![image](https://user-images.githubusercontent.com/62539341/83342646-c65b9280-a32c-11ea-9a77-4af7512ae81d.png)

��й�ȣ�� �ٷ� ����. ���!

<h3>Level 1 -> Level 2</h3>

![image](https://user-images.githubusercontent.com/62539341/83342832-d5434480-a32e-11ea-9219-3a4b20428484.png)

password�� ���� �ȿ� �����Ѵٰ� �Ѵ�.

�ϴ� ls�� ������ Ȯ���غ��� -�� �̸��� ���� ������ Ȯ���Ͽ��� cat���� ������ ������ Ȯ���Ϸ������� ���� ���������� ������ ������ �ʴ´�.

ã�ƺ��� �����̸��� �հ��� �ٸ��� Ư�����ڿ��� ~/ �����η� ������ �νĽ����ָ� �ȴٰ� �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/83342836-e2f8ca00-a32e-11ea-8578-fde642274a35.png)

<h3>Level 2 -> Level 3</h3>

![image](https://user-images.githubusercontent.com/62539341/83343004-4c2d0d00-a330-11ea-9c61-4eb9d69d75f4.png)

�̹��� ��й�ȣ�� ����ִ� ���� �̸��� spaces in this filename��� �����ִ�.

���� �̸��ȿ� ������ ������ �Ʊ�ó�� �����η� ������ �νĽ�ų �� ���� ������?

![image](https://user-images.githubusercontent.com/62539341/83343008-551dde80-a330-11ea-860a-0cd7cc26f35a.png)

���۸��� �غ��� ���� �̸��� ������ ū ����ǥ("")�� �����ָ� �ȴٰ� �Ѵ�.

![image](https://user-images.githubusercontent.com/62539341/83343028-6bc43580-a330-11ea-93fb-808ae71851c9.png)

<h3>Level 3 -> Level 4</h3>

![image](https://user-images.githubusercontent.com/62539341/83343074-0e7cb400-a331-11ea-8e5c-4437a0de12d0.png)

inhere ���丮 �ȿ� ������ ������ �����Ѵٰ� �Ѵ�.

�Ʊ� ls ��ɾ ���� �˾ƺ� �� ��� ������ ������ �ɼ� -a�� ���ٰ� �ߴ�. ������ �����̶�� ������ ls�� ���� ���� ������ ������ �ʰ� �ɼ� -a�� �߰��ϸ� ������ ���� ���̴�.

![image](https://user-images.githubusercontent.com/62539341/83343077-176d8580-a331-11ea-9494-8d44f0e4c26d.png)

<h3>Level 4 -> Level 5</h3>

![image](https://user-images.githubusercontent.com/62539341/83343253-b777de80-a332-11ea-8bc4-a24194351b66.png)

inhere ���丮 �ȿ� ����� ���� �� �ִ� ������ �����Ѵٰ� �����ִ�.

���� ������ Ȯ���غ��� ���ڰ� �̻��ϰ� �����. ����� ���� �� �ִٰ� �ߴµ�... ����..?

![image](https://user-images.githubusercontent.com/62539341/83343256-c2327380-a332-11ea-82cb-b02f1a3ad16d.png)

![image](https://user-images.githubusercontent.com/62539341/83343263-d0808f80-a332-11ea-8d8b-075a7b6652fc.png)

��..! -file07���� ����� ���� �� �ִ� �����̴�! �̰� ��й�ȣ�ΰ�����!

![image](https://user-images.githubusercontent.com/62539341/83343269-de361500-a332-11ea-9ad1-253c04487abd.png)

<h3>Level 5 -> Level 6</h3>

![image](https://user-images.githubusercontent.com/62539341/83343427-10487680-a335-11ea-9de4-97df819d953d.png)

inhere ���丮 �ȿ� ��𰣿� ��й�ȣ�� ����ִ� ������ �����Ѵ�. �׸��� ������ ����� ���� �� �ְ�, ���� �Ұ��ϰ�, 1033 ����Ʈ ����� ������.

���丮�� 19���� �ִ�... �ƹ����� �̰� �ϳ��ϳ� �� Ȯ���غ��ƾ� �ڴ�.

![image](https://user-images.githubusercontent.com/62539341/83343430-176f8480-a335-11ea-990f-43f6076c2080.png)

���丮 �ȿ� ������ Ȯ���غ��� ���� �Ұ����� ���ϵ鸸 ���캸�� �ǰڴ�.

![image](https://user-images.githubusercontent.com/62539341/83343433-21918300-a335-11ea-91df-5f0f2ed9744e.png)

�ϳ� �����غ��� �̰� �밡���ؼ� �� �� �ƴ϶�� ������ �����.

��Ʈ�� 1033 ����Ʈ��� ������ du ��ɾ ���� �ȴٰ� ������ ���ߴ�! �ϸ��͸� ����� �� �� �ߴ�. �� ���� �͵��� �ϳ��ϳ� �� ������ �ߴٴ�... ����

![image](https://user-images.githubusercontent.com/62539341/83343446-4128ab80-a335-11ea-8b31-c7c112bb4f65.png)

���⼭ 1033 ����Ʈ ����� ���� ���� ã���� �ȴ�. ���� ��ġ Ȯ��!

![image](https://user-images.githubusercontent.com/62539341/83343453-5e5d7a00-a335-11ea-8efb-66a17494ce68.png)

![image](https://user-images.githubusercontent.com/62539341/83343462-7e8d3900-a335-11ea-93b4-e6ce3ddf8ba3.png)

<h3>Level 6 -> Level 7</h3>

![image](https://user-images.githubusercontent.com/62539341/83343574-438c0500-a337-11ea-9549-b8cef3875711.png)

�̹��� ���Ӱ� grep �̶�� ��ɾ �����ߴ�.

- grep : �Է����� ���޵� ������ ���뿡�� Ư�� ���ڿ��� ã������ �� ���

![image](https://user-images.githubusercontent.com/62539341/83343577-4d156d00-a337-11ea-8c7c-db8e24701490.png)

�̹��� ���� ��Ŵٰ� find �ɼ� �� �����ؼ� �̷��� ã�ƺô�.
size 33����Ʈ��, bandit7�� �����̰�, �׷��� badit6

![image](https://user-images.githubusercontent.com/62539341/83343586-661e1e00-a337-11ea-8a34-ab872ec6c603.png)
 
���� ���� �̰��� ��й�ȣ�� �ִ� �����̴�!

![image](https://user-images.githubusercontent.com/62539341/83343599-7afab180-a337-11ea-96d6-97c185a8c98b.png)

<h3>Level 7 -> Level 8</h3>

![image](https://user-images.githubusercontent.com/62539341/83343926-91a30780-a33b-11ea-843d-4d1d25687294.png)

�̹����� ��ɾ � �� �߰����.

- sort : ��ɾ� ��� Ȥ�� ���� ������ ����
- uniq : �ߺ��� ������ ���� ���������� �ִٸ� �ϳ��� ����� �����Ѵ�. ��ü������ �л�� �ߺ��� ã�� ���� sort�� ���� ���̱� ����.
- strings : ���α׷� �ȿ��� ���� ���ڿ��� ���
- base64 : ���ڿ��� base64�� ���ڵ�
- tr : translate �� ���μ�, Ư���� ���ڸ� �ٸ� ���ڷ� �ٲٰų� �Ǵ� Ư�� ���ڸ� ����
- tar : ���� ���� ������ �ϳ��� ���Ϸ� ���ų� Ǯ �� ���
- gzip : ������ ���� �� ����, tar�� �Բ� �� ���ȴ�.
- bzip2 : ������ ���� �� ����
- xxd : ���̳ʸ� �����͸� 16������, 16���� �����͸� ���̳ʸ� �����ͷ� ��ȯ

ls�� Ȯ���غ��� data.txt�� �����Ѵ�. �̸� cat�� Ȯ���غ��� ��~�� ���� �����͵��� ��µȴ�.

![image](https://user-images.githubusercontent.com/62539341/83343928-9962ac00-a33b-11ea-84be-eb87f4ad62c2.png)

�ϴ� �� ��ɾ���� ��� ����ؾ� ���� �� �𸣰ڰ� �Ʊ� ���Դ� grep ���� millionth�� �˻��غô�.

![image](https://user-images.githubusercontent.com/62539341/83343933-ac757c00-a33b-11ea-86c2-71476952bc05.png)

<h3>Level 8 -> Level 9</h3>

![image](https://user-images.githubusercontent.com/62539341/83344070-48ec4e00-a33d-11ea-8acd-eead7b8d14c1.png)

data.txt�� Ȯ���غ��� �� ��û ���� �����͵��� ����� ���´�.

�ؽ�Ʈ�� �ϳ��� ���´ٰ� ������ �Ʊ� ã�ƺ� uniq�� ����غ��ƾ� �ڴ�.

![image](https://user-images.githubusercontent.com/62539341/83344079-51448900-a33d-11ea-8760-705bce0dbfbd.png)

<h3>Level 9 -> Level 10</h3>

![image](https://user-images.githubusercontent.com/62539341/83344200-78e82100-a33e-11ea-97b9-13aa858d22ef.png)

�̹��� strings�� ����ؼ� ���ڿ��� ã�ƺ��� �ǰڴ�!

![image](https://user-images.githubusercontent.com/62539341/83344209-8ef5e180-a33e-11ea-96e2-ffa116c9cc9d.png)

<h3>Level 10 -> Level 11</h3>

![image](https://user-images.githubusercontent.com/62539341/83344286-923d9d00-a33f-11ea-9e10-10c375045064.png)

�̹��� base64�� ���ڵ��ϸ� �� �� ����!

![image](https://user-images.githubusercontent.com/62539341/83344289-9d90c880-a33f-11ea-98e6-02b6e0fe8fa7.png)

�� �ȵ���..? base64�� base64�� ���ڵ��Ѵٰ� �ߴµ� �� �Ǵ� ������ �𸣰ڴ�.

![image](https://user-images.githubusercontent.com/62539341/83344293-ab464e00-a33f-11ea-8271-092367039d96.png)
