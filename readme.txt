ѧϰgit��
git��һ���汾����ϵͳ��
git�ǿ�Դ�ġ�

1.pwd���� ������ʾ��ǰĿ¼
2.windowsϵͳ ȷ��Ŀ¼��������Ŀ¼  ����������

3.git init ��Ŀ¼���git���Թ���Ĳֿ� ��������.gitĿ¼�����ٹ���汾�⣩
.git Ŀ¼Ĭ�������ص� ������ ls -ah ������ʾ

ѧϰgit status

git diff  

git log �鿴�ύ��־

git log --pretty=oneline ʹ�������־��Ϣ���

HEAD^ ��һ�汾
HEAD^^ �������汾
HEAD~100  ����100�汾

�汾����  git reset --hard HEAD^

���汾����֮����Ҫ�ٸĻ���  ����git log �ṩ��commit id �����ٴλ���  git reset --hard  19sa23---- ָ��Ҫ���˵İ汾��commit id��
( Git ���ڲ���һ��ָ��ǰ�汾��HEAD ָ�룬������˰汾��ʱ�򣬽����Ǹı�HEAD��ָ��)


cat readme.txt  (���������ڲ鿴readme.txt�ļ�������)

git reflog (��¼ÿһ�ε�����)
git log (�ύ��ʷ)


git diff (���������ݴ����ıȽ� �����Կ������������޸�����Щ����)

���Կ�git add ���ǲ����� git commit

�]���ύ���������һ���ύ���״̬  git checkout -- readme.txt

����Ϊ����git checkout -- file ���� ���ı䲢����ӵ��ݴ��� ��Ҫ�Ȼ��˰汾  ֻ�ǻ�����ӵ��ݴ����� ֱ�� git reset HEAD --readme.txt ���ɣ�Ȼ�󱾵��ļ���ʹ�� git checkout -- readme.txt��


1,�������˹������ļ������ݣ���ֱ�Ӷ������������޸�ʱ�������� git checkout -- file
2,�������˹������ļ������ݲ�����ӵ����ݴ�����ʱ����ʹ������ git reset HEAD file��Ȼ����ʹ������ git checkout -- �ļ���


ɾ���ļ� rm file

1����ɾ�� ʹ�� git checkout -- file  (�Ӱ汾������ȡ�ļ�)
2��ȷʵ��ɾ��  git rm file Ȼ��  git commit -m "";


cd ~  �����û�����Ŀ¼�ļ�


�ñ��ص�git�ֿ��github�����git�ֿ�Զ��ͬ��  -��github�ϴ���һ���ֿ⣬Ȼ���ڱ��زֿ�ִ������
1���ñ��زֿ��github����Ĳֿ����  git remote add origin git@github.com:YUECHUNYING/learngit.git
2,  �ѱ��ص��������͵�Զ��github����  git push -u origin master


������Կ��ssh-keygen -t rsa -C "���Լ�������" (shell ������ git bash����)


��github���½�һ���ֿ⣬�ڱ���ִ�� git clone ���ɲֿ��ĵ�ַ


git branch dev  (git�����һ����֧)
git checkout dev(��֧������) ���л���dev�����֧��
git checkout -b dev (����dev��֧�����л���dev��֧��)

git branch ���鿴��֧�б�


git merge dev  (�ϲ�ָ���ķ�֧����ǰ��֧�£�)

git branch -d dev ��ɾ��dev��֧��

�����ͻ ��git�ϲ�ʧ�ܵ��ļ��ֶ��༭Ϊϣ��������


git merge --no-ff -m "�ϲ������ύ�ļ�" dev  
���ϲ���֧ʱ���� --no-ff �����Ϳ�������ͨģʽ�ϲ����ϲ������ʷ�з�֧���ܿ��������������ϲ�,��fast-forward�ϲ��Ϳ����������������ϲ���

git stash ���������ع���
git stash list �鿴�����ֳ�

�ָ� ���������ݣ�1��git stash apply �ָ���stash�����ݲ���ɾ������Ҫʹ�� git stash drop��ɾ��
                           2��git stash pop �ָ���ͬʱ��stash������Ҳɾ����
1��git stash  2,ȥ�������������޸���bug  3��git stash pop �ָ������ֳ�



�½���һ����֧����û�кϲ� ���ɾ�����ͻᶪʧ���޸� �����Ҫǿ��ɾ������Ҫһ������ -D��
git branch -D dev ��ǿ��ɾ����


�鿴Զ�̿����Ϣ  git remote  --> origin
                            git remote -v ����ϸ����Ϣ

���ͷ�֧  ���ǰѸ÷�֧�ϵ����б����ύ���͵�Զ�̿⣬����ʱ��Ҫָ�����ط�֧��
������git�ͰѸ÷�֧���͵�Զ�̿��Ӧ��Զ�̷�֧�ϡ�

����Զ��origin��dev��֧������   git checkout -b dev origin/dev
Ȼ��� ���ص� dev��֧ push ��Զ��  git push origin dev

����ʧ�ܣ���ʹ��git pull �����µ��ύ��Զ�ֿ̲��֧ dev��ץ������Ȼ���ڱ��غϲ��������ͻ��������

���û��ָ������dev��֧��Զ��origin/dev��֧�����ӣ�����dev��origin/dev������
git branch --set-upstream-to=origin/dev dev

�ٴ�ִ�� git pull �ϲ��г�ͻ ��Ҫ�ֶ������Ȼ�����ύ����git push origin dev

git tag v1.0 �����½�һ����ǩ Ĭ����HEAD Ҳ����ָ��һ��commit id   ��git tag v0.9  f52c633��
git tag -a v1.1 -m "���ǩ"  ָ����ǩ��Ϣ
git tag ���Բ鿴���б�ǩ
