## SQL复制表时的UNIQUE constraint failed问题

以在同一个数据库里复制表为例

数据库中有  Note , DeletedNote 两张表，它们的结构相同

```sql
sqlite> .schema
CREATE TABLE Note (_id integer primary key autoincrement,words text,time text);
CREATE TABLE DeletedNote (_id integer primary key autoincrement,words text,time text);
```

有时候**复制表**会出现以下问题

```sql
sqlite> .insert into DeletedNote select * from NoteTime;
Error: UNIQUE constraint failed: DeletedNote._id
```

因为复制表的时候主键也会一起复制过去，所以当两个表有主键相同的数据时，就无法复制



### 解决

复制语句换成

```sql
sqlite> insert into DeletedNote (words,time) select words,time from Note;
```

就不会把主键也复制过去了