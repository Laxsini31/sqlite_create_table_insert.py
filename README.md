import sqlite3
conn=sqlite3.connect("students.db")
cursor=conn.cursor()
cursor.execute("create table if not exists student(id int,name text)")
cursor.execute("insert into student values(1,'Achu')")
conn.commit()
cursor.execute("select * from student")
print(cursor.fetchall())
conn.close()
Output
[(1, 'Achu')]
