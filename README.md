# docker_mysql_low_memory
Low memory settings for mysql running on docker.


docker run -d --net=host --name mysql -e MYSQL_ROOT_PASSWORD=password --memory=256m --memory-swap=0m mysql:latest --performance_schema=off --innodb_buffer_pool_size=5m --max_connections=5 --sort_buffer_size=2m --key_buffer_size=8m --innodb_log_buffer_size=256K --innodb_sort_buffer_size=64K --thread_cache_size=0 --host_cache_size=0 --thread_stack=128k --tmp_table_size=16M
