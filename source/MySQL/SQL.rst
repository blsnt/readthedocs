SQL语句
=======

1. 基础查询
-----------

::

   # 查询员工表的单个字段
   mysql> select last_name from employees;

   # 查询员工表的多个字段
   mysql> select last_name,salary,email from employees;

   # 查询员工表的所有字段
   mysql> select * from employees;

   # 查询常量值
   mysql> select 100;

   # 查询表达式
   mysql> select 100%98;

   # 取别名
   mysql> select last_name as 姓,first_name as 名 from employees;
   +-------------+-------------+
   | 姓          | 名          |
   +-------------+-------------+
   | K_ing       | Steven      |
   | Kochhar     | Neena       |
   +---------------------------+

   mysql> select last_name 姓,first_name 名 from employees;

   # 案例,out是关键字需要加双引号
   mysql> select salary as "out put" from employees;

   # 案例: 去重 查询员工表卓弄个涉及到的所有的部门编号
   mysql> select distinct department_id from employees;
   +---------------+
   | department_id |
   +---------------+
   |          NULL |
   |            10 |
   |            20 |
   |            30 |
   |            40 |
   |            50 |
   |            60 |
   |            70 |
   |            80 |
   |            90 |
   |           100 |
   |           110 |
   +---------------+
   12 rows in set (0.00 sec)

   # +号的作用
   # 案例：查询员工和姓连接成一个字段，并显示为姓名
   mysql> select concat(last_name,first_name) as 姓名 from employees;
   +------------------+
   | 姓名             |
   +------------------+
   | K_ingSteven      |
   | KochharNeena     |
   | De HaanLex       |
   | HunoldAlexander  |
   | ErnstBruce       |
   | AustinDavid      |
   +------------------+

2. 条件查询
-----------

::

   # 分类
   条件运算符：> < = != <> >= <=
   逻辑运算法：and or not && || ！
   模糊查询：like 
                   between 
                   and 
                   in 
                   is null
                   
   # 按条件表达式筛选
   # 查询 工资> 12000的员工信息
   mysql> select * from employees where salary > 12000;
   +------------+-----------+----------+
   | first_name | last_name | salary   |
   +------------+-----------+----------+
   | Steven     | K_ing     | 24000.00 |
   | Neena      | Kochhar   | 17000.00 |
   | Lex        | De Haan   | 17000.00 |
   | John       | Russell   | 14000.00 |
   | Karen      | Partners  | 13500.00 |
   | Michael    | Hartstein | 13000.00 |
   +------------+-----------+----------+
   6 rows in set (0.00 sec)

.. _条件查询-1:

2. 条件查询
-----------

3. 排序查询
-----------
