## Ubuntu

| Function      | Commands       |
|---------------|----------------|
| Restart SHELL | `exec "$SHELL"`|

## PYENV

| Function                   | Commands                         |
|----------------------------|----------------------------------|
| Install new python version | `pyenv install ${VERSION:3.12}`  |
| Activate version           | `pyenv global ${VERSION:3.12}`   |

## CQLSH

| Function                           | Commands                                                                     |
|------------------------------------|------------------------------------------------------------------------------|
| List all keyspaces                 | `select * from system_schema.keyspaces`                                      |
| Displays table syntax              | `desc ${TABLE_NAME}`                                                         |
| Displays user defined type syntax  | `desc type ${TYPE_NAME}`                                                     |
| Alter table                        | `alter table ${TABLE_NAME} add ${COLUMN} text`                               |
| Export table data to CSV file      | `copy ${TABLE_NAME} TO '${CSV_FILE_PATH:C:\test.csv}' with header = TRUE`    |
| Import data to table from CSV file | `copy ${TABLE_NAME} FROM '${CSV_FILE_PATH:C:\test.csv}'`                     |
| Get datacenter                     | `use system;select data_center from local`                                   |

## Node

| Function                       | Commands                                          |
|--------------------------------|---------------------------------------------------|
| Run typescript file using Node | `node --experimental-strip-types ${FILE_PATH}`    |