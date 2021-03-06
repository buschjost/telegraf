## v0.1.9 [unreleased]

### Release Notes
- InfluxDB output config change: `url` is now `urls`, and is a list. Config files
will still be backwards compatible if only `url` is specified.

### Features
- [#143](https://github.com/influxdb/telegraf/issues/143): InfluxDB clustering support
- [#181](https://github.com/influxdb/telegraf/issues/181): Makefile GOBIN support. Thanks @Vye!

### Bugfixes
- [#170](https://github.com/influxdb/telegraf/issues/170): Systemd support
- [#175](https://github.com/influxdb/telegraf/issues/175): Set write precision before gathering metrics
- [#178](https://github.com/influxdb/telegraf/issues/178): redis plugin, multiple server thread hang bug
- Fix net plugin on darwin
- [#84](https://github.com/influxdb/telegraf/issues/84): Fix docker plugin on CentOS. Thanks @neezgee!
- [#189](https://github.com/influxdb/telegraf/pull/189): Fix mem_used_perc. Thanks @mced!
- [#192](https://github.com/influxdb/telegraf/issues/192): Increase compatibility of postgresql plugin. Now supports versions 8.1+

## v0.1.8 [2015-09-04]

### Release Notes
- Telegraf will now write data in UTC at second precision by default
- Now using Go 1.5 to build telegraf

### Features
- [#150](https://github.com/influxdb/telegraf/pull/150): Add Host Uptime metric to system plugin
- [#158](https://github.com/influxdb/telegraf/pull/158): Apache Plugin. Thanks @KPACHbIuLLIAnO4
- [#159](https://github.com/influxdb/telegraf/pull/159): Use second precision for InfluxDB writes
- [#165](https://github.com/influxdb/telegraf/pull/165): Add additional metrics to mysql plugin. Thanks @nickscript0
- [#162](https://github.com/influxdb/telegraf/pull/162): Write UTC by default, provide option
- [#166](https://github.com/influxdb/telegraf/pull/166): Upload binaries to S3
- [#169](https://github.com/influxdb/telegraf/pull/169): Ping plugin

### Bugfixes

## v0.1.7 [2015-08-28]

### Features
- [#38](https://github.com/influxdb/telegraf/pull/38): Kafka output producer.
- [#133](https://github.com/influxdb/telegraf/pull/133): Add plugin.Gather error logging. Thanks @nickscript0!
- [#136](https://github.com/influxdb/telegraf/issues/136): Add a -usage flag for printing usage of a single plugin.
- [#137](https://github.com/influxdb/telegraf/issues/137): Memcached: fix when a value contains a space
- [#138](https://github.com/influxdb/telegraf/issues/138): MySQL server address tag.
- [#142](https://github.com/influxdb/telegraf/pull/142): Add Description and SampleConfig funcs to output interface
- Indent the toml config file for readability

### Bugfixes
- [#128](https://github.com/influxdb/telegraf/issues/128): system_load measurement missing.
- [#129](https://github.com/influxdb/telegraf/issues/129): Latest pkg url fix.
- [#131](https://github.com/influxdb/telegraf/issues/131): Fix memory reporting on linux & darwin. Thanks @subhachandrachandra!
- [#140](https://github.com/influxdb/telegraf/issues/140): Memory plugin prec->perc typo fix. Thanks @brunoqc!

## v0.1.6 [2015-08-20]

### Features
- [#112](https://github.com/influxdb/telegraf/pull/112): Datadog output. Thanks @jipperinbham!
- [#116](https://github.com/influxdb/telegraf/pull/116): Use godep to vendor all dependencies
- [#120](https://github.com/influxdb/telegraf/pull/120): Httpjson plugin. Thanks @jpalay & @alvaromorales!

### Bugfixes
- [#113](https://github.com/influxdb/telegraf/issues/113): Update README with Telegraf/InfluxDB compatibility
- [#118](https://github.com/influxdb/telegraf/pull/118): Fix for disk usage stats in Windows. Thanks @srfraser!
- [#122](https://github.com/influxdb/telegraf/issues/122): Fix for DiskUsage segv fault. Thanks @srfraser!
- [#126](https://github.com/influxdb/telegraf/issues/126): Nginx plugin not catching net.SplitHostPort error

## v0.1.5 [2015-08-13]

### Features
- [#54](https://github.com/influxdb/telegraf/pull/54): MongoDB plugin. Thanks @jipperinbham!
- [#55](https://github.com/influxdb/telegraf/pull/55): Elasticsearch plugin. Thanks @brocaar!
- [#71](https://github.com/influxdb/telegraf/pull/71): HAProxy plugin. Thanks @kureikain!
- [#72](https://github.com/influxdb/telegraf/pull/72): Adding TokuDB metrics to MySQL. Thanks vadimtk!
- [#73](https://github.com/influxdb/telegraf/pull/73): RabbitMQ plugin. Thanks @ianunruh!
- [#77](https://github.com/influxdb/telegraf/issues/77): Automatically create database.
- [#79](https://github.com/influxdb/telegraf/pull/56): Nginx plugin. Thanks @codeb2cc!
- [#86](https://github.com/influxdb/telegraf/pull/86): Lustre2 plugin. Thanks srfraser!
- [#91](https://github.com/influxdb/telegraf/pull/91): Unit testing
- [#92](https://github.com/influxdb/telegraf/pull/92): Exec plugin. Thanks @alvaromorales!
- [#98](https://github.com/influxdb/telegraf/pull/98): LeoFS plugin. Thanks @mocchira!
- [#103](https://github.com/influxdb/telegraf/pull/103): Filter by metric tags. Thanks @srfraser!
- [#106](https://github.com/influxdb/telegraf/pull/106): Options to filter plugins on startup. Thanks @zepouet!
- [#107](https://github.com/influxdb/telegraf/pull/107): Multiple outputs beyong influxdb. Thanks @jipperinbham!
- [#108](https://github.com/influxdb/telegraf/issues/108): Support setting per-CPU and total-CPU gathering.
- [#111](https://github.com/influxdb/telegraf/pull/111): Report CPU Usage in cpu plugin. Thanks @jpalay!

### Bugfixes
- [#85](https://github.com/influxdb/telegraf/pull/85): Fix GetLocalHost testutil function for mac users
- [#89](https://github.com/influxdb/telegraf/pull/89): go fmt fixes
- [#94](https://github.com/influxdb/telegraf/pull/94): Fix for issue #93, explicitly call sarama.v1 -> sarama
- [#101](https://github.com/influxdb/telegraf/issues/101): switch back from master branch if building locally
- [#99](https://github.com/influxdb/telegraf/issues/99): update integer output to new InfluxDB line protocol format

## v0.1.4 [2015-07-09]

### Features
- [#56](https://github.com/influxdb/telegraf/pull/56): Update README for Kafka plugin. Thanks @EmilS!

### Bugfixes
- [#50](https://github.com/influxdb/telegraf/pull/50): Fix init.sh script to use telegraf directory. Thanks @jseriff!
- [#52](https://github.com/influxdb/telegraf/pull/52): Update CHANGELOG to reference updated directory. Thanks @benfb!

## v0.1.3 [2015-07-05]

### Features
- [#35](https://github.com/influxdb/telegraf/pull/35): Add Kafka plugin. Thanks @EmilS!
- [#47](https://github.com/influxdb/telegraf/pull/47): Add RethinkDB plugin. Thanks @jipperinbham!

### Bugfixes
- [#45](https://github.com/influxdb/telegraf/pull/45): Skip disk tags that don't have a value. Thanks @jhofeditz!
- [#43](https://github.com/influxdb/telegraf/pull/43): Fix bug in MySQL plugin. Thanks @marcosnils!

## v0.1.2 [2015-07-01]

### Features
- [#12](https://github.com/influxdb/telegraf/pull/12): Add Linux/ARM to the list of built binaries. Thanks @voxxit!
- [#14](https://github.com/influxdb/telegraf/pull/14): Clarify the S3 buckets that Telegraf is pushed to.
- [#16](https://github.com/influxdb/telegraf/pull/16): Convert Redis to use URI, support Redis AUTH. Thanks @jipperinbham!
- [#21](https://github.com/influxdb/telegraf/pull/21): Add memcached plugin. Thanks @Yukki!

### Bugfixes
- [#13](https://github.com/influxdb/telegraf/pull/13): Fix the packaging script.
- [#19](https://github.com/influxdb/telegraf/pull/19): Add host name to metric tags. Thanks @sherifzain!
- [#20](https://github.com/influxdb/telegraf/pull/20): Fix race condition with accumulator mutex. Thanks @nkatsaros!
- [#23](https://github.com/influxdb/telegraf/pull/23): Change name of folder for packages. Thanks @colinrymer!
- [#32](https://github.com/influxdb/telegraf/pull/32): Fix spelling of memoory -> memory. Thanks @tylernisonoff!

## v0.1.1 [2015-06-19]

### Release Notes

This is the initial release of Telegraf.
