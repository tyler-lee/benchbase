# BenchBase

[![BenchBase (Java with Maven)](https://github.com/tyler-lee/benchbase/actions/workflows/maven.yml/badge.svg?branch=apsardb-mysql)](https://github.com/tyler-lee/benchbase/actions/workflows/maven.yml)

---

## Quickstart

To clone and build BenchBase using the `apsaradb-mysql` profile,

```bash
git clone --depth 1 https://github.com/tyler-lee/benchbase.git -b apsaradb-mysql
cd benchbase
./mvnw clean package -P apsaradb-mysql
```

This produces artifacts in the `target` folder, which can be extracted,

```bash
cd target
tar xvzf benchbase-mysql.tgz
cd benchbase-mysql
```

Inside this folder, you can run BenchBase. For example, to execute the `tpcc` benchmark,

```bash
java -jar benchbase.jar -b tpcc -c config/mysql/sample_tpcc_apsaradb_config.xml --create=true --load=true --execute=true
```

A full list of options can be displayed,

```bash
java -jar benchbase.jar -h
```

Refer to [README.md](README.md) for more detailed description and user guide.
