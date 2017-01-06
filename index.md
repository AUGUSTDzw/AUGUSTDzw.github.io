让mysql支持插入中文

第一种，每次创建 table 时都加上 character set = utf8：
CREATE TABLE `runoob_posts`(
  cid INT(11) PRIMARY KEY AUTO_INCREMENT,
  username VARCHAR(20),
  title VARCHAR(200),
  content TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
) CHARACTER SET utf8;

第二种，修改已创建的 table 的编码：
alter table table_name convert to character set utf8;
