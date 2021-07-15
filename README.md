# docker-images

沃趣科技Docker image开源项目,持续分享我们在数据库容器化进程中的实践与经验,欢迎关注并提交issue与我们互动.



```

docker run -d --name oracledb \
-p 10136:1521 \
-e ORACLE_SID=orcl \
-e ORACLE_PWD=oracle \
-e ORACLE_CHARACTERSET=ZHS16GBK \
-e SGA_SIZE=8G \
-e PGA_SIZE=8G \
-e DB_ROLE=primary \
-e ENABLE_ARCH=true \
-v /home/oracledata/data:/opt/oracle/oradata \
registry.cn-hangzhou.aliyuncs.com/woqutech/oracle-database-11.2.0.4.0-ee

```

>docker exec -it oracledb bash


 sqlplus /nolog
 
 conn /as sysdba
 
 alter user system identified by oracle;
 
 alter user sys identified by oracle;
 
 alter user scott identified by Q65137791o;
 
 alter user scott account unlock;
 
  ALTER PROFILE DEFAULT LIMIT PASSWORD_LIFE_TIME UNLIMITED;
