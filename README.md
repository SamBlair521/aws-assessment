# aws-assessment

1. EBS is not a standalone storage service like s3
EBS is specifically meant ec2 instances
EBS can’t be used for multiple instances at once. S3 can be used by many different instances at once.

2.	Highlight few differences between NoSQL & SQL databases
SQL is relational databases and noSql is non-relational.
noSql has a dynamic schema whereas SQL has pre-defined schema.
SQL databases are vertically scalable and NoSQL databases are horizontally scalable

3. 3.	Highlight few differences between ssh & http protocol
Ssh has a built in username/pw authentication and http protocol authentication does not as opposed to https
http is an underlying protocol used by the web to define how messages are formatted and transmitted.
SSH uses port 22 to define authentication for connection instead over the world wide web


Task 3. (3) Winget https://testtt125.s3.us-east-2.amazonaws.com/mysqlsampledatabase.sql.txt

Task 4:
1.	On ec2 instance Count number of lines of the mysqldump file ( downloaded from s3) 4065
2.	Create a new file from the file mysqlsampledatabase.sql where every word “mysql” is replaced with “yoursql”  sed -i 's/mysql/yoursql/g' mysqlsampledatabase.sql.txt
3.	( bonus ) Count how many times word NULL appeared on mysqlsampledatabase.sql file.
grep -o 'NULL' mysqlsampledatabase.sql.txt | wc -l         538 times

Task 5:
1.	Create an RDS MariaDB instance on AWS Ohio region.
2.	Import the mysql dump file mysqlsampledatabase.sql into the RDS database

Task 6:
1.	Write an SQL query on the database created on step 5 : Select all customer names, and product names from the database in single query. Select c.customername, p.productname from customers c join products p on c.customerid = p.customerid


