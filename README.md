# JKNET

The bird config for my network

```
# Internal Community:
#  (207705,<999, 0)  Community for all my node
#  (207705,<999, 1)  Community only for this node
#  (207705,   1,*)   do not send to ibgp
#  (207705,   2,*)   do not send to ebgp
#  (207705,   3,*)   do not send to kernel
#  (207705, 101,*)   allow bgp_local_perf
#  (207705, 201,*)   transit routes
#  (207705, 202,*)   peer routes
#  (207705, 203,*)   customer routes
#  (207705, 204,*)   ibgp routes
#
# Control Community:
#   Actions:
#    _ = 0   do not announce to target
#    _ = 1   prepend 1 to target
#    _ = 2   prepend 2 to target
#    _ = 4   prepend 4 to target
#    _ = 8   prepend 8 to target
#   Action target selector:
#    _ = Action target selector
#    (207705,1_00,0)            Do action to everyone
#    (207705,1_01,asn)          Don't do action to this asn
#    (207705,1_02,asn)          Do action to this asn
#    (207705,1_10,0)            Do action to every region
#    (207705,1_11,region_code)  Don't do action to this region
#    (207705,1_12,region_code)  Do action to this region
#    (207705,1_20,0)            Do action to every country
#    (207705,1_21,country_code) Don't do action to this country
#    (207705,1_22,country_code) Do action to this country
#    (207705,1_30,1)            Do action to upstreams
#    (207705,1_30,2)            Do action to peers
#    (207705,1_30,3)            Do action to downstreams
#   Examples:
#    prepend 11 to AS6939: [(207705,1102,6939),(207705,1202,6939),(207705,1802,6939)]
#    prepend 1 to everyone but 6939: [(207705,1100,6939),(207705,1101,6939)]
#    do not announce to anyone: [(207705,1000,0)]
#
# Informational Community
#  (207705,10000,region_code)    Received from region
#  (207705,10001,country_code)   Received from country
# 
# Region code:
#  * 41: Europe
#  * 42: North America-E
#  * 43: North America-C
#  * 44: North America-W
#  * 45: Central America
#  * 46: South America-E
#  * 47: South America-W
#  * 48: Africa-N (above Sahara)
#  * 49: Africa-S (below Sahara)
#  * 50: Asia-S (IN,PK,BD)
#  * 51: Asia-SE (TH,SG,PH,ID,MY)
#  * 52: Asia-E (JP,CN,KR)
#  * 53: Pacific&Oceania (AU,NZ,FJ)
#  * 54: Antarctica
#  * 55: Asia-N (RU)
#  * 56: Asia-W (IR,TR,UAE)
#  * 57: Central Asia (AF,UZ,KZ)
#
# Country code:
#  ISO-3166 numeric-3 country code
```