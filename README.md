# APUE

APUE(Advanced Programming in the UNIX Environment (Third Edition))

UNIX 环境高级编程 第三版

## apue_err.c

Functions that print error to stderr.

输出至标准错误的出错函数

|函数<br>functino|从strerror添加字符串？<br>add str from strerror?|strerror的参数<br>args of strerror|终止？<br>terminate?|
|:--|:--:|:--:|:--|
|err_dump|是|errno|abort();|
|err_exit|是|显式参数|exit(1);|
|err_msg|否||return;|
|err_quit|否||exit(1);|
|err_ret|是|errno|return;|
|err_sys|是|errno|exit(1);|
|err_cont|是|显式参数|return;|

## apue_log.c

Error print functions for daemon.

用于守护进程的出错函数

|函数<br>functino|从strerror添加字符串？<br>add str from strerror?|strerror的参数<br>args of strerror|终止？<br>terminate?|
|:--|:--:|:--:|:--|
|log_msg|否||return;|
|log_quit|否||exit(2);|
|log_ret|是|errno|return;|
|log_sys|是|errno|exit(2);|
|log_exit|是|显式参数|exit(2);|
