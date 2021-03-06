# 指纹识别

> *译自：[Fingerprint](https://github.com/sqlmapproject/sqlmap/wiki/Usage#fingerprint)*

## 进行广泛的 DBMS（Database Management System，数据库管理系统）指纹识别

开关: `-f` 或 `--fingerprint`

默认 sqlmap 会自动帮你识别 Web 应用后端 DBMS 的相关信息。在检测阶段结束并提醒用户进一步选择检测可注入参数的时候，sqlmap 会自动识别后端 DBMS 信息，并根据特定的数据库架构采用合适的 SQL 语法、方言和相关查询，进行进一步的攻击测试。

如果你想采用特定 SQL 方言或者内带特定错误信息等技术展开详细的 DBMS 指纹识别，可以提供 `--fingerprint` 开关。这样，sqlmap 则会发起更多的请求，并对DBMS 版本，甚至是操作系统、系统架构和补丁级别信息等方面展开指纹收集。

如果你想要更加精准的指纹识别结果，可以提供开关 `-b` 或者 `--banner`。
