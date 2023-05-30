# Luobo-net

The bird config for my network

```
# Internal Community:
#  (201217,<999, 0)  Community for all my node
#  (201217,<999, 1)  Community only for this node
#  (201217,   1,*)   do not send to ibgp
#  (201217,   2,*)   do not send to ebgp
#  (201217,   3,*)   do not send to kernel
#  (201217,   4,*)   send to kernel but mark unreachable
#  (201217,   5,*)   send to kernel but mark blackhole
#  (201217, 101,*)   allow bgp_local_perf
#  (201217, 201,*)   transit routes
#  (201217, 202,*)   ixp rs routes
#  (201217, 203,*)   peer routes
#  (201217, 204,*)   customer routes
#  (201217, 209,*)   ibgp routes
#
# Control Community:
#   Actions:
#    ░ = 0   do not announce to target
#    ░ = 1   prepend 1 to target
#    ░ = 2   prepend 2 to target
#    ░ = 4   prepend 4 to target
#    ░ = 8   prepend 8 to target
#   Action target selector:
#    ░ = Action
#    (201217,1░00,0)            Do action to everyone
#    (201217,1░01,asn)          Don't do action to this asn
#    (201217,1░02,asn)          Do action to this asn
#    (201217,1░10,0)            Do action to every region
#    (201217,1░11,region_code)  Don't do action to this region
#    (201217,1░12,region_code)  Do action to this region
#    (201217,1019,0)            Disable (asn,1010,0), (asn,1011,local_region) as default value
#    (201217,1019,1)            Do not perform prepend to balance the path_len
#    (201217,1░20,0)            Do action to every country
#    (201217,1░21,country_code) Don't do action to this country
#    (201217,1░22,country_code) Do action to this country
#    (201217,1░30,1)            Do action to upstreams
#    (201217,1░30,2)            Do action to ixp rs
#    (201217,1░30,3)            Do action to peers
#    (201217,1░30,4)            Do action to downstreams
#    (201217,1░30,8)            Do action to route collectors
#    (201217,1░40,1)            Do action to non-self upstream
#    (201217,1░40,2)            Do action to non-self peers
#    (201217,1░40,3)            Do action to non-self ixrs
#   Examples:
#     prepend 11 to AS6939: 
#       (201217,1102,6939): prepend 1 to AS6939
#       (201217,1202,6939): prepend 2 to AS6939
#       (201217,1802,6939): prepend 8 to AS6939
#                   Total : 1+2+8 = 11
#    prepend 2 to everyone but 6939:
#      (201217,1200,0):     prepend 2 to everyone
#      (201217,1201,6939):  don't do this action(prepend 2) to AS6939
#    do not announce to anyone: 
#      (201217,1000,0):     do not announce to everyone
#
# Informational Community
#  (201217,10000,region_code)    Received from region
#  (201217,10001,country_code)   Received from country
# 
# Region code:
#  41: Europe
#  42: North America-E
#  43: North America-C
#  44: North America-W
#  45: Central America
#  46: South America-E
#  47: South America-W
#  48: Africa-N (above Sahara)
#  49: Africa-S (below Sahara)
#  50: Asia-S (IN,PK,BD)
#  51: Asia-SE (TH,SG,PH,ID,MY)
#  52: Asia-E (JP,KR,TW,HK,CN)
#  53: Pacific&Oceania (AU,NZ,FJ)
#  54: Antarctica
#  55: Asia-N (RU)
#  56: Asia-W (IR,TR,UAE)
#  57: Central Asia (AF,UZ,KZ)
#
# Country code:
#  ISO-3166 numeric-3 country code
```

### Credits

* Special thanks KSKB helps me complete some filters
