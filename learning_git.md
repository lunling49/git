gitʹ�ã�
���أ�
1��mkdir <file>������һ����Ŀ¼
2��git init�������Ŀ¼��� git �ɹ���ı��زֿ�
3��vi/vim <file>�����ļ����±�д�����������ļ�
4��git add <file>��ʵ���Ͼ��ǰ�Ҫ�ύ�������޸ķŵ��ݴ�����Stage��
5��git commit -m "�Ķ�˵��"�����ݴ����������޸��ύ����֧

�汾���ˣ�
git log -- �鿴�Ķ���־�����ύ��ʷ���Ա�ȷ��Ҫ���˵��ĸ��汾
git reflog -- �鿴������ʷ���Ա�ȷ��Ҫ�ص�δ�����ĸ��汾
HEAD -- ָ��İ汾���ǵ�ǰ�汾
git reset --hard commid_id(�汾��) -- ���˻�ص�δ���İ汾
��һ���汾HEAD^������һ���汾HEAD^^���Ϻܶ�汾ʱ����д��~���֣�����20��HEAD~20

�����޸ģ�
git diff HEAD -- <file>  �鿴�������Ͱ汾�������°������
git checkout -- <file> -- ���ļ��ڹ��������޸�ȫ������
����޸ĺ��������ӵ����ݴ������붪���޸�
	1��git reset HEAD <file>���ص�������
	2��git checkout -- <file>�������������޸�
���commit�ˣ��붪���޸�
	git reset --hare HEAD^ ���� git reset --hard +�汾��

ɾ���ļ���
1��rm <file>���൱��ֻɾ���˹��������ļ��������Ҫ�ָ���ֱ����git checkout -- <file>
2��git rm <file>���൱�ڲ���ɾ�����ļ������һ���ӵ����ݴ�������Ҫ��git reset HEAD <file>��Ȼ����git checkout -- <file>
3�����Ҫ���װѰ汾��ɾ������git rm����git commit