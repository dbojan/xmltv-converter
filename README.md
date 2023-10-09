# xmltv-converter
Convert XML TV EPG to another format like sqlite
<code> <pre> 

### 2023-10-09-1

## Downloand: 
Right click [here](https://raw.githubusercontent.com/dbojan/xmltv-converter/main/xmltv-converter.zip), select 'Save Link As' to save zip file.
Unzip it somewhere.


## Usage:
drag and drop unzipped xml to 'xmltv-converter_drop_xml_file_here.bat'

You can open sqlite file with [sqlitestudio](https://github.com/pawelsalawa/sqlitestudio)

You can use sql to filter results:
```
select * from items where db_channel like '%ko%' --and  (db_start like'2023100720%' or db_start like '2023100720%')
order by 2,4
```
or to show channel_id and display_name:
```
select distinct db_channel,db_channel_original,db_display_name from items order by 1
```

Epg xml addresses:

https://tvprofil.net/xmltv/data/epg_tvprofil.net.xml.gz (balkan channels)
http://cdn.iptvhr.net/tvdata/guide.xml (balkan channels)
https://i.mjh.nz/PlutoTV/all.xml.gz (plutotv)
more info [here](https://github.com/iptv-org/epg)



My other projects:
https://github.com/dbojan/free-iptv-balkan-plus (some free iptv channels)
https://github.com/dbojan/csvEdit_Esmeralda (m3u/tsv/csv editor)


## todo:
convert to html?

--
dbojan.github.io
