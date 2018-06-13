# xlsx2protobuf
convert xlsx to .proto file and binary data file

# Usage
```
git clone https://github.com/Rhysol/xlsx2protobuf.git
cd src 
python generate.py
```

# Configuration
The config file path is xlsx2protobuf/src/config.ini. Put the \*.xlsx files in the *table* folder.
Then execute the follow command:
```
python generate.py
```
The output \*.proto files are in the *xlsx2protobuf/proto/* and 
binary data file is in the *xlsx2protobuf/binary_data/*.

# xlsx Format
|   |   | 
|---|---|
|first row   |column name |
|second row   |column description |
|after second row   |column data |
|   |   |

# Cell Data Type
The data type for cell data only support: string, int, date, string-array and int-array.
The column's data type would be decided by third row's value. If you want use the array
type, use ';' for delimiter. for example:

|InArrayColumn |StringArrayColumn|
|---|---|
|description |description |
|1;33;421; |abc;qst;ggg |

For more detail, you can check the *xlsx2protobuf/table/example.xlsx*.
