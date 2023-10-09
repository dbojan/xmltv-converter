
# xmltv-converter
Convert XML TV EPG to another format like sqlite

### version 2023-10-09-1

## Download: 
Right click [here](https://raw.githubusercontent.com/dbojan/xmltv-converter/main/xmltv-converter.zip), select 'Save Link As' to save zip file.
Unzip it somewhere.


## Usage:
drag and drop unzipped xml to 'xmltv-converter_drop_xml_file_here.bat'

You can open sqlite file with [SqliteStudio](https://github.com/pawelsalawa/sqlitestudio)

You can use sql to filter results:

(Open .db in SqliteStudio, press alt+e, or click on 'Open Sql Editor' icon in toolbar)
```
select * from items where db_channel like '%mov%' --and  (db_start like'2023100720%' or db_start like '2023100720%')
order by 2,4
```
or to show channel_id and display_name:
```
select distinct db_channel,db_channel_original,db_display_name from items order by 1
```

You can also change the way channels are displayed by setting variable in .py file.

### More info on EPG [here](https://github.com/iptv-org/epg)

Some epg xml tv sources:

https://tvprofil.net/xmltv/data/epg_tvprofil.net.xml.gz (balkan channels)

http://cdn.iptvhr.net/tvdata/guide.xml (balkan channels)

https://i.mjh.nz/PlutoTV/all.xml.gz (plutotv)


### Applications that support epg tv xml:

-[kodi](https://kodi.tv/), supports epg, kinda complicated to setup, and to navigate, supports epg, windows, android

-[ip-tv player by BorPas-Soft](https://borpas.info/iptvplayer) supports epg, windows only, freeware


### My other projects:

https://github.com/dbojan/free-iptv-balkan-plus (some free iptv channels)

https://github.com/dbojan/csvEdit_Esmeralda (m3u/tsv/csv editor)


## todo:
convert to html?

--
dbojan.github.io