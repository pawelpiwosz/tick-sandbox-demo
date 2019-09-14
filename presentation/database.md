#### Connect to InfluxDB (this script will be changed to Python CLI... someday...)

`make run container=influxdb1 type=database`

#### InfluxDB commands

`show databases`

`show retention policicies on telegraf`

`show tag keys`

`show tag values on telegraf with key = "host"`

`use telegraf`

`show measurements`

`select * from docker_log limit 10`

`show field keys from docker_log`

`select * from docker_log where container_image = 'ab' limit 10`

#### http connection to DB

`curl -G 'http://127.0.0.1:8086/query?pretty=true' --data-urlencode 'q=show databases'`

`curl -G 'http://127.0.0.1:8086/query?db=telegraf&pretty=true' --data-urlencode 'q=show measurements'`

`curl -G 'http://127.0.0.1:8086/query?db=telegraf&pretty=true' --data-urlencode 'q=select * from docker_log limit 2'`


