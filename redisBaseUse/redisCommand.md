### 1.Զ�����ӵ�������
redis-cli -h 127.0.0.1-p 6379
### 2.��ȡ����keys 
keys *
### 3.һ����������
keys *abcd*
### 5�� ����������ݿ������ key
   flushall
### 6������������յ�ǰ���ݿ��е����� key��
   FLUSHDB
### 7�����ҿ�
    select 1  
### 8������key ����ɾ��
    DEL KEY_NAME