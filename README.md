# 支持人大金仓的V009R003C011 版本
# Kdbndp 驱动 来源于 https://gitee.com/dotnetchina/SqlSugar
# 修改aop的支持
# 修改内容
 where b.nspname || '.' || a.tablename =' 表名'   // 这个语句会查询出其它的数据 ， 修改成了 where b.nspname ='{{0}}' && a.tablename = '{{1}}

 and upper(text(b.nspname || '.' || a.relname))  报 function upper(boolean) is not unique 错误的问题  修改为 //and upper(text(b.nspname || '.' || a.relname))

 # 配置支持默认的模式
 在链接字符串中配置SearchPath= 类配置
 
 

 
