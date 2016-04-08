
```

  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 24 bytes Time: 10.000000 seconds
TRAFFIC IN  <NETREAD> file descriptor=7
Byte buffer FD, length=24
--000: 00 00 00 00 00 00 00 1F 00 00 00 07 00 00 01 0A
--016: 00 00 00 00 00 00 00 00
   <........................>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 24 - 0 = 24
  DEBUG: from_client.c:FromClient(67) FromClient payload=31 size=0 type=7 sg=0x10A offset=0
  DEBUG: from_client.c:FromClient(75) FromClient (no servermessage) payload=31 size=0 type=7 controlflags=0x10A offset=0
  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 31 bytes Time: 10.000000 seconds
TRAFFIC IN  <NETREAD> file descriptor=7
Byte buffer FD, length=31
--000: 2F 75 6E 63 61 63 68 65 64 2F 31 46 2E 37 30 36
--016: 36 30 35 30 30 30 30 30 30 2F 6D 61 69 6E 00
   </uncached/1F.706605000000/main.>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 31 - 0 = 31
  DEBUG: handler.c:SingleHandler(155) START handler /uncached/1F.706605000000/main
   CALL: data.c:DataHandler(106) DataHandler: parse path=/uncached/1F.706605000000/main
  DEBUG: ow_parseobject.c:OWQ_create(160) /uncached/1F.706605000000/main
   CALL: ow_parsename.c:FS_ParsedName_anywhere(91) path=[/uncached/1F.706605000000/main]
  DEBUG: ow_cache.c:Cache_Get_Device(859) Looking for device 1F 70 66 05 00 00 00 2D
  DEBUG: ow_cache.c:Cache_Get_Common(1073) Get from cache sn 1F 70 66 05 00 00 00 2D pointer=0x400b1864 index=0 size=4
  DEBUG: ow_cache.c:Cache_Get_Common(1082) value found in cache. Remaining life: -703 seconds.
 DETAIL: ow_presence.c:CheckPresence(80) Checking presence of /uncached/1F.706605000000/main
  DEBUG: ow_select.c:BUS_select(78) Selecting a path (and device) path=/uncached/1F.706605000000/main SN=1F 70 66 05 00 00 00 2D last path=00 00 00 00 00 00 00 00
  DEBUG: ow_select.c:BUS_select(86) Continuing root branch
TRAFFIC OUT <write> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=1
--000: 72
   <r>
  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 3 bytes Time: 5.000000 seconds
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=3
--000: 50 0D 0A
   <P..>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 3 - 0 = 3
TRAFFIC OUT <write> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=52
--000: 62 46 30 46 46 46 46 36 44 44 42 46 36 37 46 46
--016: 42 42 37 37 46 44 46 42 37 36 44 44 42 42 36 36
--032: 44 44 42 42 36 36 44 44 42 42 36 36 44 44 46 42
--048: 46 36 46 0D
   <bF0FFFF6DDBF67FFBB77FDFB76DDBB66DDBB66DDBB66DDFBF6F.>
TRAFFIC OUT <write> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=36
--000: 42 42 37 37 46 44 46 42 37 36 44 44 42 42 36 36
--016: 44 44 42 42 36 36 44 44 42 42 36 36 44 44 46 42
--032: 46 36 46 0D
   <BB77FDFB76DDBB66DDBB66DDBB66DDFBF6F.>
TRAFFIC OUT <write> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=20
--000: 44 44 42 42 36 36 44 44 42 42 36 36 44 44 46 42
--016: 46 36 46 0D
   <DDBB66DDBB66DDFBF6F.>
TRAFFIC OUT <write> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=4
--000: 46 36 46 0D
   <F6F.>
  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 52 bytes Time: 5.000000 seconds
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=4
--000: 46 30 36 43
   <F06C>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=9
--000: 35 42 34 39 39 30 44 34 35
   <5B4990D45>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=10
--000: 36 36 41 41 35 35 36 35 35 32
   <66AA556552>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=9
--000: 35 34 39 39 32 32 34 34 39
   <549922449>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=10
--000: 39 32 32 34 34 39 39 32 32 34
   <9224499224>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=9
--000: 34 39 35 35 41 42 34 41 0D
   <4955AB4A.>
TRAFFIC IN  <NETREAD> bus=0 (/dev/ttyUSB0)
Byte buffer LinkHub-E v1.1, length=1
--000: 0A
   <.>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 52 - 0 = 52
  DEBUG: ow_transaction.c:BUS_transaction_single(209) verify = 0
  DEBUG: ow_transaction.c:BUS_transaction_single(201) end = 0
  DEBUG: ow_presence.c:CheckThisConnection(246) Presence of 1F 70 66 05 00 00 00 2D FOUND on bus /dev/ttyUSB0
  DEBUG: ow_cache.c:Cache_Add_Device(482) Adding device location 1F 70 66 05 00 00 00 2D bus=0
  DEBUG: ow_cache.c:Cache_Add_Common(594) Add to cache sn 1F 70 66 05 00 00 00 2D pointer=0x400b1864 index=0 size=4
  DEBUG: ow_cache.c:GetFlippedTree(562) Flipping cache tree (purging timed-out data)
   CALL: data.c:DataHandler(156) Directory message (all at once)
  DEBUG: dirall.c:DirallHandler(66) OWSERVER Dir-All SpecifiedBus=0 path = /uncached/1F.706605000000/main
  DEBUG: ow_dir.c:FS_dir_remote(74) path=/uncached/1F.706605000000/main
   CALL: ow_dir.c:FS_dir_both(98) path=/uncached/1F.706605000000/main
  DEBUG: ow_search.c:BUS_first(32) Start of directory path=/uncached/1F.706605000000/main device=1F 70 66 05 00 00 00 2D
  DEBUG: ow_dir.c:FS_dir_both(193) ret=-5
  DEBUG: ow_parsename.c:FS_ParsedName_destroy(55) /uncached/1F.706605000000/main
  DEBUG: data.c:DataHandler(186) DataHandler: FS_ParsedName_destroy done
  DEBUG: data.c:DataHandler(200) DataHandler: cm.ret=-5
  DEBUG: to_client.c:ToClient(56) payload=0 size=0, ret=-5, sg=0x10A offset=0 
TRAFFIC OUT <to server data> file descriptor=7
Byte buffer FD, length=0
-- NULL buffer
  DEBUG: data.c:DataHandler(220) Finished with client request
  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 24 bytes Time: 10.000000 seconds
TRAFFIC IN  <NETREAD> file descriptor=10
Byte buffer FD, length=24
--000: 00 00 00 00 00 00 00 1F 00 00 00 04 00 00 01 0A
--016: 00 00 00 00 00 00 00 00
   <........................>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 24 - 0 = 24
  DEBUG: from_client.c:FromClient(67) FromClient payload=31 size=0 type=4 sg=0x10A offset=0
  DEBUG: from_client.c:FromClient(75) FromClient (no servermessage) payload=31 size=0 type=4 controlflags=0x10A offset=0
  DEBUG: ow_tcp_read.c:tcp_read(64) attempt 31 bytes Time: 10.000000 seconds
TRAFFIC IN  <NETREAD> file descriptor=10
Byte buffer FD, length=31
--000: 2F 75 6E 63 61 63 68 65 64 2F 31 46 2E 37 30 36
--016: 36 30 35 30 30 30 30 30 30 2F 6D 61 69 6E 00
   </uncached/1F.706605000000/main.>
  DEBUG: ow_tcp_read.c:tcp_read(114) read: 31 - 0 = 31
  DEBUG: handler.c:SingleHandler(155) START handler /uncached/1F.706605000000/main
   CALL: data.c:DataHandler(106) DataHandler: parse path=/uncached/1F.706605000000/main
  DEBUG: ow_parseobject.c:OWQ_create(160) /uncached/1F.706605000000/main
   CALL: ow_parsename.c:FS_ParsedName_anywhere(91) path=[/uncached/1F.706605000000/main]
  DEBUG: ow_cache.c:Cache_Get_Device(859) Looking for device 1F 70 66 05 00 00 00 2D  DEBUG: handler.c:Handler(137) OWSERVER handler done
  DEBUG: ow_net_server.c:ProcessAcceptSocket(236) Normal exit.

  DEBUG: ow_cache.c:Cache_Get_Common(1073) Get from cache sn 1F 70 66 05 00 00 00 2D pointer=0x400b1864 index=0 size=4
  DEBUG: ow_cache.c:Cache_Get_Common(1082) value found in cache. Remaining life: 120 seconds.
  DEBUG: ow_presence.c:CheckPresence(75) Found device on bus 0
   CALL: data.c:DataHandler(152) Directory message (one at a time)
   CALL: dir.c:DirHandler(74) DirHandler: pn->path=/uncached/1F.706605000000/main
  DEBUG: dir.c:DirHandler(79) OWSERVER SpecifiedBus=0 path=/uncached/1F.706605000000/main
  DEBUG: ow_dir.c:FS_dir_remote(74) path=/uncached/1F.706605000000/main
   CALL: ow_dir.c:FS_dir_both(98) path=/uncached/1F.706605000000/main
  DEBUG: ow_search.c:BUS_first(32) Start of directory path=/uncached/1F.706605000000/main device=1F 70 66 05 00 00 00 2D
  DEBUG: ow_dir.c:FS_dir_both(193) ret=-5
  DEBUG: ow_parsename.c:FS_ParsedName_destroy(55) /uncached/1F.706605000000/main
  DEBUG: data.c:DataHandler(186) DataHandler: FS_ParsedName_destroy done
  DEBUG: data.c:DataHandler(200) DataHandler: cm.ret=-5
  DEBUG: to_client.c:ToClient(56) payload=0 size=0, ret=-5, sg=0x10A offset=0 
TRAFFIC OUT <to server data> file descriptor=10
Byte buffer FD, length=0
-- NULL buffer
  DEBUG: data.c:DataHandler(220) Finished with client request
  DEBUG: handler.c:Handler(137) OWSERVER handler done
  DEBUG: ow_net_server.c:ProcessAcceptSocket(236) Normal exit.



```