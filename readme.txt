ѧϰgit��
git��һ���汾����ϵͳ��
git�ǿ�Դ�ġ�

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

