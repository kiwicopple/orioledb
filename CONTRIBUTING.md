# Contributing

## Ways to contribute

- Use OrioleDB.
- Help us solve a [GitHub issue](https://github.com/orioledb/orioledb/issues), or create a new one.
- Add some [documentation](https://github.com/orioledb/orioledb/wiki)
- Follow and share on [Twitter](https://twitter.com/orioledb)
- Contribute to this repo

## Familiarize yourself with the repo

- You can learn about some of the goals of OrioleDb by watching [Alexander's talk](https://www.postgresbuild.com/alexander-korotkov-2021).
- Learn about the [architecture](https://github.com/orioledb/orioledb/blob/main/doc/arch.md) of OrioleDB.
- Learn [how to use](https://github.com/orioledb/orioledb/blob/main/doc/usage.md) OrioleDb.

## Folder structure

```sh
├── ci                  
├── doc
├── expected
├── include
├── specs                        # Tests: Isolation tests to simulate multiple connections running simultaneously.
├── sql                          # Tests: Simple tests to compare OrioleDB compatibility with PostgreSQL.
├── src 
├── t                            # Tests: Python testgres tests for testing features like backups and replication.
├── orioledb--1.0.sql
├── orioledb.control
├── orioledb_isolation.conf
├── orioledb_regression.conf
├── stopevents_gen.py
├── stopevents.txt
├── typedefs_gen.py
└── valgrind.supp
```

## Common Tasks

### Adding tests

OrioleDB has 3 groups of tests:

- SQL-tests located in `sql` folder. These are most simple tests. The sql-file get passed to psql and the result is compared to the expected output.
- Isolation tests located in specs folder. These tests simulate multiple connections running simultaneously. See the PostgreSQL README.
- Python [testgres](https://pypi.org/project/testgres/) tests located in `t`. These tests allow to test the features like backups and replication. See the [testgres docs](https://postgrespro.github.io/testgres/).