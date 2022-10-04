# Practice CSV

Practice CSV With [columnq-cli](https://github.com/roapi/roapi/tree/main/columnq-cli).

```bash
# Download And Install columnq-cli (MacOS Version)
$ curl -L 'https://github.com/roapi/roapi/releases/download/columnq-cli-v0.3.0/columnq-cli-apple-darwin.tar.gz' | tar xvf - -C "${HOME}/bin"
$ columnq --version
Columnq 0.3.0

# File Name Equals Table Name
$ columnq sql --table ./example.csv 'SELECT id, name, age FROM example'
+----+---------------+-----+
| id | name          | age |
+----+---------------+-----+
| 1  | Hoge          | 18  |
| 2  | Example, Name | 25  |
| 3  | Fuga          | 39  |
+----+---------------+-----+

# Define Table Name
$ columnq sql --table users=./example.csv 'SELECT id, name, age FROM users'
+----+---------------+-----+
| id | name          | age |
+----+---------------+-----+
| 1  | Hoge          | 18  |
| 2  | Example, Name | 25  |
| 3  | Fuga          | 39  |
+----+---------------+-----+

# Where And Order By
$ columnq sql --table users=./example.csv 'SELECT id, name, age FROM users WHERE age >= 20 ORDER BY age DESC'
+----+---------------+-----+
| id | name          | age |
+----+---------------+-----+
| 3  | Fuga          | 39  |
| 2  | Example, Name | 25  |
+----+---------------+-----+
```

- References
  - [JSON や CSV で SELECT * FROM したいときは columnq-cli が便利](https://zenn.dev/hankei6km/articles/select-from-json-csv-by-using-columnq-cli)


## Links

- [Neo's World](https://neos21.net/)
