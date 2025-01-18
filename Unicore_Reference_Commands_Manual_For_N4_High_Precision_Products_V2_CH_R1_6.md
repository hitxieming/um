![](media/a86ed5dd8857736178420508489bbcd9.png)

[WWW.UNICORE.COM](http://WWW.UNICORE.COM/)

NebulasIV 系列高精度产品数据接口协议

Copyright© 2009-2024, Unicore Communications, Inc.

Data subject to change without notice.

## 修订记录

| 修订版 | 修订记录                                                             | 日期    |
|--------|----------------------------------------------------------------------|---------|
| R1.0   | 首次发布                                                             | 2022-10 |
| R1.1   | 新增以下消息：OBSVMCMP、OBSVHCMP、TROPINFO、                         | 2023-05 |
|        | MSPOS、CONFIG MMP、CONFIG SIGNALGROUP、                              |         |
|        | CONFIG IONMODE、CONFIG RTCMPHASERATE、                               |         |
|        | GPHPR2、GPTRA2、GPROT2；                                             |         |
|        | 扩展 IRNSS L5 支持，包括：MASK、UNMASK、NMEA 消                      |         |
|        | 息、OBSVM/H、OBSVBASE、BESTSAT、STADOP/H、                           |         |
|        | ADRDOP/H、SPPDOP/H、PPPDOP、SATSINFO、                               |         |
|        | SATELLITE、SATECEF；                                                 |         |
|        | 第 [4](#_bookmark31) 章 CONFIG：ANTIJAM 替换原 JAMMING 指令；        |         |
|        | 第 5.2 章：新增 MASK RTCMCN0/CN0 配置；                              |         |
|        | RTKSTATUS 第 16 字段由 Reserved 改为 dual RTK Flag；                 |         |
|        | 第 3.6 章：细化 MODE ROVER 的模式小类；                              |         |
|        | CONFIG SBAS 配置增加 timeout；                                       |         |
|        | OBSVM 增加 QZSS L1C Signal ID；                                      |         |
|        | 更新 HWSTATUS 中 DC18 的电压范围；                                   |         |
|        | 优化 CONFIG PPS ENABLE 和 ENABLE2 的描述；                           |         |
|        | 第 [3.4](#_bookmark21) 章：更新 MODE BASE 水平精度及高程精度的默认值 |         |
|        | 优化 CONFIG HEADING TRACTOR 的描述；                                 |         |
|        | FREQJAMSTATUS 适配产品增加 UM982；                                   |         |
|        | 标注 UM982 固件版本 Build9669 支持的内容                             |         |
| R1.2   | 扩展 SIGNALGROUP、 CONFIG SBAS 等配置                                | 2023-11 |
|        | 新增CONFIG EVENT2、 CONFIG RTCMCLOCKOFFSET、                         |         |
|        | CONFIG PVTALG、 CONFIG PSRPOSBIAS 等配置                             |         |
|        | 新增 QZSSEPH、 GPHPD 等消息输出                                      |         |

-   RTKSTATUS 字段 17 由reserved 改为 ADR Number
-   调整 BD3EPH 中的 IODC 和 IODE 的描述
-   表 7-54：更新 IRNSS 的 PRN 编号
-   更新MASK 指令： 取消MASK [高度角(可选)] [频点/系统]
-   表 3-8： 无人机Formation 模式名称改为 HighDyn R1.3  新增以下配置：

    [4.31](#_bookmark102) [网络 IP 地址配置](#_bookmark102)；[4.32](#_bookmark104) [网络端口号配置](#_bookmark104)；

    [4.33](#_bookmark106) [LOG 输出顺序配置](#_bookmark106)；[4.34](#_bookmark108) [Ntripserver 配置](#_bookmark108)；

    [4.35](#_bookmark110) [Ntripclient 配置](#_bookmark110)；[4.36](#_bookmark112) [RTCM 数据过滤配置](#_bookmark112)；

    [4.37](#_bookmark114) [星历输出配置](#_bookmark114)；

-   新增 CONFIG PPP ENABLE AUTO 配置；
-   更新 [4.23](#_bookmark84) [SIGNALGROUP 跟踪通道模式配置](#_bookmark84)；
-   [表7-78 GLONASS 星历标志代码](#_bookmark258)：更新 P3 描述；
-   新增以下消息输出：

    [7.3.22](#_bookmark262) [IRNSSEPH IRNSS 星历数据](#_bookmark262)；

    1.  [E6MASKBLOCK 掩码信息](#_bookmark378)
        1.  [E6ORBITBLOCK 轨道改正](#_bookmark383)
        2.  [E6CLOCKFULLBLOCK 钟差全集改正](#_bookmark386)
        3.  [E6CLOCKSUBBLOCK 钟差子集改正](#_bookmark389)
        4.  [E6CBIASBLOCK 码偏差改正](#_bookmark391)
        5.  [E6PBIASBLOCK 相位偏差改正](#_bookmark393)
        6.  [BSLNENUHD2 东北天坐标系下的基线长度](#_bookmark395)
        7.  [BSLNXYZHD2 直角坐标系下的基线长度](#_bookmark397)
        8.  [DOPHD2 Heading2 精度因子](#_bookmark399)

            [7.3.50](#_bookmark332) [HEADINGSTATUS Heading 解算状态](#_bookmark332)

2024-04

| R1.4 | Heading2 相关 log（GPHPR2、GPTRA2、GPROT2）补充说明：仅支持 ONCHANGED 输出； SIGNALGROUP 9 配置：删除 Galileo E6； [表7-56 通道跟踪状态](#_bookmark218)：QZSS 添加添加 L6D 和 L6E 类型定义； 新增配置：CONFIG VELSTDTHD、CONFIG RTKASITPPP； 新增带校验的输入指令： 第 [1](#_bookmark2) 章：添加关于带校验的输入指令相关说明；第 [4](#_bookmark31) 章：新增配置 CONFIG CMDFORMAT； 添加 UMD982 相关内容： SIGNALGROUP 中添加 UMD982 的频点； VERSION 中添加 UMD982 的编号；适用产品添加 UMD982； [4.27](#_bookmark94) 电离层模型配置：补充单北斗产品相关说明； 第 [7.3](#_bookmark207) 章 EPH 消息：当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式； [表7-50](#_bookmark210) 及[表7-51](#_bookmark211) Header 中的 version 信息写入原 reserved 字段； 添加 4.17 RTCMSWITCHL2CL2P 配置； [4.32](#_bookmark104) 网络端口号配置：添加端口号的范围要求； [7.1](#_bookmark140) 及 [7.2](#_bookmark172) NMEA 消息：补充各字段的有效位描述； BD3ION、BD3UTC、BD3EPH、TROPINFO 适用产品添加 UM982 和 UMD982。 | 2024-06 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| R1.5 | 添加 UMD980 相关内容： SIGNALGROUP 中添加 UMD980 的频点； VERSION 中添加 UMD980 的编号；适用产品添加 UMD980；                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 2024-08 |

-   [3.2](#_bookmark17) [以精确坐标设置基准站模式](#_bookmark17)中补充说明： 如果接收机自身解出的坐标与用户设置的坐标之间的 3D 误差超过 300

    米，则不输出 RTCM 数据。 R1.6  修改 GPHPR2 消息输出示例；

-   STANDALONE 配置和MODE BASE 中补充说明：开阔环境下推荐配置CONFIG PVTALG MULTI；
-   4.2 串口配置：支持奇偶校验和停止位配置；
-   PPPNAV 中补充基站 ID 的详细定义；
-   添加 QZSS L6 相关内容：

    添加 CONFIG SIGNALGROUP 10；

    消息输出中添加 L6MDCTYPE1/2/3/4/5/7； CONFIG PPP ENABLE 中添加 L6MDCPPP 参数；

-   添加 QZQSM 灾害告警信息；
-   添加 UMD960 相关内容；
-   CONFIG SBAS ENABLE 添加 SLAS 参数；
-   删除 CONFIG RTCMSWITCHL2CL2P 配置；
-   OBSVM 中的表 7-56 通道跟踪状态：添加 QZSS L1C/B 和 L1S；
-   CONFIG VELSTDTHD 补充参数取值范围；
-   添加 RTKSTATUS2 消息；
-   STANDALONE 中添加说明“某些场景下也可以通过MASK低仰角卫星减少多路径效应对模组的影响”；
-   添加 UBD9A0 相关内容；
-   CONFIG VELSTDTHD 的默认状态改为 DISABLE；
-   更新 CONFIG IONMODE 的参数描述；
-   CONFIG STANDALONE 添加TIMEOUT 配置；
-   添加章节 7.3.87 ENVINFO；
-   表 7-36 NMEA 消息中的卫星 PRN：添加 KASS 的编号；

2024-10

-   第 4.23 章：UM980 SIGNALGROUP 8 支持 50Hz PVT，调整

    相应描述

权利声明

本手册提供和芯星通科技（北京）有限公司（以下简称为“和芯星通”）相应型号产品信息。

和芯星通保留本手册文档，及其所载之所有数据、设计、布局图等信息的一切权利、权益，包括但不限于已有著作权、专利权、商标权等知识产权，可以整体、部分或以不同排列组合形式进行专利权、商标权、著作权授予或登记申请的权利，以及将来可能被授予或获批登记的知识产权。

和芯星通拥有“和芯星通”、“UNICORECOMM”、“Unicore”以及本手册下相应产品所属系列名称的注册商标专用权。

本手册之整体或其中任一部分，并未以明示、暗示、禁止反言或其他任何形式对和芯星通拥有的上述权利、权益进行整体或部分的转让、许可授予。

免责声明

本手册所载信息，系根据手册更新之时所知相应型号产品情形的“原样”提供，对上 述信息适于特定目的、用途之准确性、可靠性、正确性等，和芯星通不作任何保证或承诺。

和芯星通可能对产品规格、描述、参数、使用等相关事项进行修改，或一经发现手册误载信息后进行勘误，上述情形可能造成订购产品实际信息与本手册所载信息有差异。

如您发现订购产品的信息与本手册所载信息之间存有不符，请您与本公司或当地经销商联系，以获取最新的产品手册或其勘误表。

## 前言

本手册为您提供有关和芯星通高精度 GNSS 板卡和接收机的指令及 Log 参考，接收机默认配置，及相关使用示例等。

-   本手册为通用版本，请用户根据实际购买产品配置，针对 RTK、Heading、DGPS、单北斗等不同使用需求选择参考阅读。
-   每条指令都有其对应的适用产品，请根据文中标注的“适用产品”选择合适的指令或 Log。

##### 适用读者

本手册适用于对 GNSS 接收机有一定了解的技术人员使用。它并不面向一般读者。

##### 缩略词表

RTK GPS BDS GLO GAL

## 目录

## 

[目录 I](#_bookmark0)

[表目录 VIII](#_bookmark1)

1.  [常用配置指令 1](#_bookmark2)
    1.  [基准站设置 3](#_bookmark4)
    2.  [流动站设置 4](#_bookmark7)
    3.  [Heading 设置 5](#_bookmark8)
    4.  [Heading2 定向设置 5](#_bookmark9)
2.  [接收机命令分类 6](#_bookmark10)
3.  [MODE 指令 8](#_bookmark12)
    1.  [接收机工作模式查询 9](#_bookmark14)
    2.  [以精确坐标设置基准站模式 10](#_bookmark17)
    3.  [以自主优化方式设置基准站模式 12](#_bookmark19)
    4.  [缺省参数的基站模式 13](#_bookmark21)
    5.  [设置基准站的 ID 号 14](#_bookmark23)
    6.  [流动站模式指令 14](#_bookmark25)
    7.  [Heading2 模式指令 16](#_bookmark28)
4.  [CONFIG 指令 18](#_bookmark31)
    1.  [接收机的配置查询 19](#_bookmark33)
    2.  [串口配置 20](#_bookmark35)
    3.  [PPS 脉冲配置 21](#_bookmark38)
    4.  [高程异常改正值 23](#_bookmark41)
    5.  [DGPS 伪距差分数据龄期配置 23](#_bookmark43)
    6.  [RTK 引擎配置 24](#_bookmark46)
    7.  [STANDALONE 配置 26](#_bookmark49)
    8.  [HEADING 引擎配置 27](#_bookmark51)
    9.  [HEADING 航向和俯仰偏移量配置 29](#_bookmark54)
    10. [SBAS 配置 30](#_bookmark56)
    11. [EVENT 功能配置 31](#_bookmark58)
    12. [EVENT2 功能配置 32](#_bookmark60)
    13. [SMOOTH 功能配置 33](#_bookmark62)
    14. [MMP 多路径抑制配置 34](#_bookmark64)
    15. [NMEA 协议版本配置 35](#_bookmark66)
    16. [RTCMB1CB2a 版本配置 35](#_bookmark68)
    17. [RTCMPHASERATE 载波相位变化配置 36](#_bookmark70)
    18. [RTCMCLOCKOFFSET RTCM 数据钟差补偿配置 36](#_bookmark72)
    19. [PSRVELDRPOS 多普勒位置预测 37](#_bookmark74)
    20. [AGNSS 辅助定位配置 38](#_bookmark76)
    21. [PPP 配置 38](#_bookmark78)
    22. [ANTIJAM 抗干扰设置 40](#_bookmark82)
    23. [SIGNALGROUP 跟踪通道模式配置 41](#_bookmark84)
    24. [ANTENNADELTAHEN 天线高信息 45](#_bookmark88)
    25. [AUTHCODE 增加授权码 46](#_bookmark90)
    26. [ALGRESET 算法引擎的复位操作 46](#_bookmark92)
    27. [IONMODE 电离层模型配置 47](#_bookmark94)
    28. [BASEANTENNAMODEL 基准站天线信息 48](#_bookmark96)
    29. [PVTALG PVT 解算引擎配置 49](#_bookmark98)
    30. [PSRPOSBIAS PSRPOS 偏差补偿配置 49](#_bookmark100)
    31. [网络 IP 地址配置 50](#_bookmark102)
    32. [网络端口号配置 51](#_bookmark104)
    33. [LOG 输出顺序配置 52](#_bookmark106)
    34. [Ntripserver 配置 52](#_bookmark108)
    35. [Ntripclient 配置 53](#_bookmark110)
    36. [RTCM 数据过滤配置 54](#_bookmark112)
    37. [星历输出配置 54](#_bookmark114)
    38. [速度 STD 门限配置 55](#_bookmark116)
    39. [RTK 辅助 PPP 定位配置 55](#_bookmark118)
    40. [指令校验配置 56](#_bookmark120)
5.  [MASK 指令 57](#_bookmark122)
    1.  [接收机 MASK 配置查询 57](#_bookmark123)
    2.  [MASK 用于屏蔽接收机接收的卫星系统 57](#_bookmark125)
    3.  [UNMASK 用于解除屏蔽接收机接收的卫星系统 60](#_bookmark131)
6.  [AGNSS 辅助位置和辅助时间信息输入 62](#_bookmark134)
    1.  [辅助位置信息输入 62](#_bookmark135)
    2.  [辅助时间信息输入 63](#_bookmark137)
7.  [数据输出指令 64](#_bookmark139)
    1.  [NMEA 数据输出指令 64](#_bookmark140)
        1.  [NMEA V4.10（默认） 65](#_bookmark142)
        2.  [NMEA V4.11 86](#_bookmark157)
    2.  [Unicore 扩展的 NMEA 数据输出指令 106](#_bookmark172)
        1.  [GPGGAH 从天线计算的卫星定位信息 106](#_bookmark173)
        2.  [GPGLLH 从天线计算的地理位置信息 108](#_bookmark175)
        3.  [GPGNSH 从天线计算的定位数据输出 110](#_bookmark177)
        4.  [GPGRSH 从天线定位解算的卫星残差 112](#_bookmark179)
        5.  [GPGSAH 从天线参与定位解算的卫星信息 116](#_bookmark182)
        6.  [GPGSTH 从天线计算的伪距观测误差信息 118](#_bookmark185)
        7.  [GPGSVH 从天线的可视卫星信息输出 119](#_bookmark187)
        8.  [GPRMCH 从天线的卫星定位信息 121](#_bookmark189)
        9.  [GPVTGH 从天线的地面航向与速度信息 123](#_bookmark191)
        10. [GPTHS2 航向信息 124](#_bookmark193)
        11. [GPHPR 姿态参数 125](#_bookmark195)
        12. [GPHPR2 姿态参数 126](#_bookmark197)
        13. [GPTRA2 方向角输出 127](#_bookmark199)
        14. [GPROT2 旋转速度和方向信息 129](#_bookmark201)
        15. [GPHPD 定位定向信息 130](#_bookmark203)
        16. [QZQSM 灾害告警信息 131](#_bookmark205)
    3.  [Unicore 数据输出指令 132](#_bookmark207)
        1.  [VERSION 版本及授权信息 134](#_bookmark212)
        2.  [OBSVM 观测量 136](#_bookmark214)
        3.  [OBSVH 从天线的观测量 141](#_bookmark219)
        4.  [OBSVMCMP 压缩格式原始观测数据信息 142](#_bookmark221)
        5.  [OBSVHCMP 压缩格式的从天线的原始观测量 145](#_bookmark225)
        6.  [OBSVBASE 基准站观测量 147](#_bookmark228)
        7.  [BASEINFO 基准站信息 149](#_bookmark230)
        8.  [GPSION 电离层参数 150](#_bookmark232)
        9.  [BD3ION 电离层参数 152](#_bookmark234)
        10. [BDSION 电离层参数 153](#_bookmark236)
        11. [GALION 电离层参数 155](#_bookmark238)
        12. [GPSUTC 协调世界时数据 156](#_bookmark240)
        13. [BD3UTC 协调世界时数据 157](#_bookmark242)
        14. [BDSUTC 协调世界时数据 159](#_bookmark244)
        15. [GALUTC 协调世界时数据 160](#_bookmark246)
        16. [GPSEPH GPS 星历数据 162](#_bookmark248)
        17. [QZSSEPH QZSS 星历 164](#_bookmark250)
        18. [BD3EPH 北斗 3 代星历 167](#_bookmark252)
        19. [BDSEPH 北斗星历数据 170](#_bookmark254)
        20. [GLOEPH GLONASS 星历数据 173](#_bookmark256)
        21. [GALEPH 伽利略星历数据 177](#_bookmark260)
        22. [IRNSSEPH IRNSS 星历数据 180](#_bookmark262)
        23. [AGRIC 信息 183](#_bookmark264)
        24. [PVTSLN 定位定向信息 187](#_bookmark266)
        25. [UNILOGLIST 请求 log 列表输出 190](#_bookmark268)
        26. [BESTNAV 最佳位置和速度 191](#_bookmark271)
        27. [BESTNAVXYZ 最佳位置和速度（直角坐标系） 195](#_bookmark276)
        28. [BESTNAVH 从天线最佳的位置和速度 197](#_bookmark278)
        29. [BESTNAVXYZH 从天线最佳位置和速度（直角坐标系） 200](#_bookmark280)
        30. [BESTSAT 参与定位的卫星信息 202](#_bookmark282)
        31. [ADRNAV RTK 位置和速度信息 206](#_bookmark288)
        32. [ADRNAVH 从天线的 RTK 位置和速度信息 209](#_bookmark290)
        33. [PPPNAV PPP 定位的位置与速度信息 211](#_bookmark292)
        34. [SPPNAV 伪距位置和速度信息 213](#_bookmark294)
        35. [SPPNAVH 从天线的伪距位置和速度信息 216](#_bookmark296)
        36. [STADOP DOP 信息 219](#_bookmark298)
        37. [STADOPH 从天线 DOP 信息 220](#_bookmark300)
        38. [ADRDOP DOP 信息 221](#_bookmark302)
        39. [ADRDOPH 从天线 DOP 信息 223](#_bookmark304)
        40. [PPPDOP DOP 信息 224](#_bookmark306)
        41. [SPPDOP DOP 信息 226](#_bookmark308)
        42. [SPPDOPH 从天线 DOP 信息 227](#_bookmark310)
        43. [SATSINFO 卫星信息 229](#_bookmark312)
        44. [BASEPOS 基准站模式下基准站位置的输出信息 233](#_bookmark318)
        45. [SATELLITE 可见卫星 236](#_bookmark320)
        46. [SATECEF 直角坐标中的卫星位置 238](#_bookmark323)
        47. [RECTIME 时间信息 241](#_bookmark325)
        48. [UNIHEADING 航向信息 243](#_bookmark328)
        49. [UNIHEADING2 多流动站定向信息 245](#_bookmark330)
        50. [HEADINGSTATUS Heading 解算状态 246](#_bookmark332)
        51. [RTKSTATUS RTK 解算状态信息 248](#_bookmark334)
        52. [RTKSTATUS2 从天线的 RTK 解算状态信息 250](#_bookmark336)
        53. [AGNSSSTATUS 辅助定位状态信息 253](#_bookmark338)
        54. [RTCSTATUS RTC 初始化状态查询 255](#_bookmark340)
        55. [JAMSTATUS 干扰检测 257](#_bookmark342)
        56. [FREQJAMSTATUS 各频段干扰检测信息 258](#_bookmark344)
        57. [RTCMSTATUS 接收机接收到的 RTCM 数据包监测信息 259](#_bookmark346)
        58. [HWSTATUS 硬件状态信息 262](#_bookmark349)
        59. [AGC AGC 状态 264](#_bookmark352)
        60. [KSXT 定位定向数据输出语句 266](#_bookmark354)
        61. [INFOPART1 268](#_bookmark356)
        62. [INFOPART2 269](#_bookmark358)
        63. [MSPOS 双天线的最佳位置 270](#_bookmark360)
        64. [TROPINFO 对流层天顶延迟信息输出 272](#_bookmark362)
        65. [PPPB2BINFO1 信息类型 1 273](#_bookmark364)
        66. [PPPB2BINFO2 信息类型 2 274](#_bookmark366)
        67. [PPPB2BINFO3 信息类型 3 276](#_bookmark368)
        68. [PPPB2BINFO4 信息类型 4 277](#_bookmark370)
        69. [PPPB2BINFO5 信息类型 5 279](#_bookmark372)
        70. [PPPB2BINFO6 信息类型 6 280](#_bookmark374)
        71. [PPPB2BINFO7 信息类型 7 282](#_bookmark376)
        72. [E6MASKBLOCK 掩码信息 285](#_bookmark378)
        73. [E6ORBITBLOCK 轨道改正 288](#_bookmark383)
        74. [E6CLOCKFULLBLOCK 钟差全集改正 292](#_bookmark386)
        75. [E6CLOCKSUBBLOCK 钟差子集改正 294](#_bookmark389)
        76. [E6CBIASBLOCK 码偏差改正 296](#_bookmark391)
        77. [E6PBIASBLOCK 相位偏差改正 298](#_bookmark393)
        78. [BSLNENUHD2 东北天坐标系下的基线长度 300](#_bookmark395)
        79. [BSLNXYZHD2 直角坐标系下的基线长度 302](#_bookmark397)
        80. [DOPHD2 Heading2 精度因子 304](#_bookmark399)
        81. [L6MDCTYPE1 卫星掩码信息 305](#_bookmark401)
        82. [L6MDCTYPE2 轨道改正数 308](#_bookmark404)
        83. [L6MDCTYPE3 时钟改正数 310](#_bookmark406)
        84. [L6MDCTYPE4 码间偏差改正数 311](#_bookmark408)
        85. [L6MDCTYPE5 相位偏差改正数 313](#_bookmark410)
        86. [L6MDCTYPE7 用户测距精度 315](#_bookmark412)
        87. [ENVINFO 环境信息 316](#_bookmark414)
8.  [其它指令 319](#_bookmark417)
    1.  [Unlog 停止串口输出 319](#_bookmark418)
    2.  [Freset 清除 NVM 中的数据并重新启动接收机 320](#_bookmark420)
    3.  [Reset 重启接收机 320](#_bookmark422)
    4.  [Saveconfig 保存用户配置至非易失性存储器（NVM） 321](#_bookmark424)

        [附录 1：32 位 CRC 校验 323](#_bookmark426)

        [附录 2：RTCM V3 差分电文 327](#_bookmark427)

        [附录 3：EVENT 输出 329](#_bookmark428)

9.  [EVENTFLAG EVENT 位置信息 329](#_bookmark429)
10. [EVENTSLN EVENT 位置及时间信息 331](#_bookmark432)

### 表目录

[表1-1 常用指令集 1](#_bookmark3)

[表1-2 固定基站模式 3](#_bookmark5)

[表1-3 自主优化设置基站模式 4](#_bookmark6)

[表2-1 接收机指令集分类 6](#_bookmark11)

[表3-1 接收机工作模式列表 8](#_bookmark13)

[表3-2 接收机工作模式查询指令 9](#_bookmark15)

[表3-3 MODE 消息说明 9](#_bookmark16)

[表3-4 基准站工作模式参数列表 11](#_bookmark18)

[表3-5 基准站工作模式参数列表 12](#_bookmark20)

[表3-6 基准站工作模式参数列表 13](#_bookmark22)

[表3-7 基准站工作模式参数 14](#_bookmark24)

[表3-8 流动站指令格式说明 15](#_bookmark26)

[表3-9 流动站模式默认配置 15](#_bookmark27)

[表3-10 定向工作模式参数 17](#_bookmark30)

[表4-1 设备/功能名称列表 19](#_bookmark32)

[表4-2 接收机配置查询指令 20](#_bookmark34)

[表4-3 串口设备参数列表 20](#_bookmark36)

[表4-4 串口支持的波特率 21](#_bookmark37)

[表4-5 PPS 功能表 22](#_bookmark39)

[表4-6 PPS 配置指令 22](#_bookmark40)

[表4-7 高程异常改正值配置表格 23](#_bookmark42)

[表4-8 配置 DGPS 伪距差分数据龄期 24](#_bookmark44)

[表4-9 DGPS TIMEOUT 默认配置 24](#_bookmark45)

[表4-10 配置 RTK 模块指令 25](#_bookmark47)

[表4-11 RELIABILITY 可靠性门限配置参数 25](#_bookmark48)

[表4-12 STANDALONE 参数 27](#_bookmark50)

[表4-13 Heading 引擎配置参数 28](#_bookmark52)

[表4-14 HEADING LENGTH 配置参数 29](#_bookmark53)

[表4-15 Heading 航向和俯仰偏移量配置参数 30](#_bookmark55)

[表4-16 配置 SBAS 指令 30](#_bookmark57)

[表4-17 配置 EVENT 模块指令 32](#_bookmark59)

[表4-18 配置 EVENT2 模块指令 33](#_bookmark61)

[表4-19 配置 SMOOTH 功能指令 34](#_bookmark63)

[表4-20 配置 MMP 指令 34](#_bookmark65)

[表4-21 配置 NMEA0183 版本指令 35](#_bookmark67)

[表4-22 配置 RTCMB1CB2a 功能指令 36](#_bookmark69)

[表4-23 配置 RTCMPHASERATE 功能指令 36](#_bookmark71)

[表4-24 配置 RTCMCLOCKOFFSET 功能指令 37](#_bookmark73)

[表4-25 配置 PSRVELDRPOS 功能指令 38](#_bookmark75)

[表4-26 配置 AGNSS 功能指令 38](#_bookmark77)

[表4-27 配置 PPP 功能指令 39](#_bookmark79)

[表4-28 PPP CONVERGE 配置参数 40](#_bookmark80)

[表4-29 抗干扰功能配置的指令说明 40](#_bookmark83)

[表4-30 配置频点组合选择功能指令 42](#_bookmark85)

[表4-31 频点组合表 42](#_bookmark86)

[表4-32 产品默认频点组合及支持的配置 44](#_bookmark87)

[表4-33 配置天线高信息配置的功能指令 45](#_bookmark89)

[表4-34 配置接收机授权码的功能指令 46](#_bookmark91)

[表4-35 ALGRESET 指令参数 47](#_bookmark93)

[表4-36 IONMODE 指令参数 47](#_bookmark95)

[表4-37 BASEANTENNAMODEL 指令参数 48](#_bookmark97)

[表4-38 PVTALG 指令参数 49](#_bookmark99)

[表4-39 PSRPOSBIAS 指令参数 50](#_bookmark101)

[表 4-40 网络 IP 地址配置参数列表 50](#_bookmark103)

[表4-41 网络端口号配置参数列表 51](#_bookmark105)

[表4-42 LOG 输出顺序配置参数列表 52](#_bookmark107)

[表4-43 NtripServer 配置参数列表 53](#_bookmark109)

[表4-44 Ntripclient 配置参数列表 54](#_bookmark111)

[表4-45 RTCM 数据过滤指令参数 54](#_bookmark113)

[表4-46 星历输出配置指令参数 55](#_bookmark115)

[表4-47 速度 STD 门限配置参数 55](#_bookmark117)

[表4-48 RTK 辅助 PPP 定位配置参数 56](#_bookmark119)

[表4-49 指令校验配置参数 56](#_bookmark121)

[表5-1 接收机 MASK 配置查询指令 57](#_bookmark124)

[表5-2 Mask 指令参数（1） 58](#_bookmark126)

[表5-3 Mask 指令参数（2） 59](#_bookmark127)

[表5-4 Mask 指令参数（3） 59](#_bookmark128)

[表5-5 卫星系统及频点 59](#_bookmark129)

[表5-6 Mask RTCMCN0、CN0 指令 60](#_bookmark130)

[表5-7 Unmask 指令参数（1） 61](#_bookmark132)

[表5-8 Unmask 指令参数（2） 61](#_bookmark133)

[表6-1 AGNSS 辅助位置信息参数定义 62](#_bookmark136)

[表6-2 AGNSS 辅助时间信息参数定义 63](#_bookmark138)

[表7-1 卫星系统及其简化符号 65](#_bookmark141)

[表7-2 DTM 数据结构 65](#_bookmark143)

[表7-3 GBS 数据结构 67](#_bookmark144)

[表7-4 GGA 数据结构 68](#_bookmark145)

[表7-5 GLL 数据结构 70](#_bookmark146)

[表7-6 GNS 数据结构 71](#_bookmark147)

[表7-7 GRS 数据结构 74](#_bookmark148)

[表7-8 GSA 数据结构 76](#_bookmark149)

[表7-9 GST 数据结构 77](#_bookmark150)

[表7-10 GSV 数据结构 79](#_bookmark151)

[表7-11 THS 数据结构 80](#_bookmark152)

[表7-12 RMC 数据结构 81](#_bookmark153)

[表7-13 ROT 数据结构 83](#_bookmark154)

[表7-14 VTG 数据结构 84](#_bookmark155)

[表7-15 ZDA 数据结构 85](#_bookmark156)

[表7-16 DTM 数据结构 86](#_bookmark158)

[表7-17 GBS 数据结构 87](#_bookmark159)

[表7-18 GGA 数据结构 89](#_bookmark160)

[表7-19 GLL 数据结构 91](#_bookmark161)

[表7-20 GNS 数据结构 92](#_bookmark162)

[表7-21 GRS 数据结构 95](#_bookmark163)

[表7-22 GSA 数据结构 96](#_bookmark164)

[表7-23 GST 数据结构 98](#_bookmark165)

[表7-24 GSV 数据结构 100](#_bookmark166)

[表7-25 THS 数据结构 101](#_bookmark167)

[表7-26 RMC 数据结构 102](#_bookmark168)

[表7-27 ROT 数据结构 104](#_bookmark169)

[表7-28 VTG 数据结构 104](#_bookmark170)

[表7-29 ZDA 数据结构 106](#_bookmark171)

[表7-30 GGAH 数据结构 107](#_bookmark174)

[表7-31 GLLH 数据结构 108](#_bookmark176)

[表7-32 GNSH 数据结构 110](#_bookmark178)

[表7-33 GRSH 数据结构 113](#_bookmark180)

[表7-34 GNSS ID 114](#_bookmark181)

[表7-35 GSAH 数据结构 116](#_bookmark183)

[表7-36 NMEA 消息中的卫星 PRN 118](#_bookmark184)

[表7-37 GSTH 数据结构 118](#_bookmark186)

[表7-38 GSVH 数据结构 120](#_bookmark188)

[表7-39 RMCH 数据结构 121](#_bookmark190)

[表7-40 VTGH 数据结构 123](#_bookmark192)

[表7-41 THS2 数据结构 125](#_bookmark194)

[表7-42 HPR 数据结构 125](#_bookmark196)

[表7-43 HPR2 数据结构 127](#_bookmark198)

[表7-44 TRA2 数据结构 128](#_bookmark200)

[表7-45 ROT2 数据结构 129](#_bookmark202)

[表7-46 HPD 数据结构 130](#_bookmark204)

[表7-47 QZQSM 数据结构 131](#_bookmark206)

[表7-48 Unicore ASCII 及 Binary 数据结构 132](#_bookmark208)

[表7-49 二进制数据格式 Header 的三个同步字节 133](#_bookmark209)

[表7-50 二进制数据格式 Header（头）结构 133](#_bookmark210)

[表7-51 ASCII 数据格式 Header（头）结构 134](#_bookmark211)

[表7-52 VERSION 数据结构 135](#_bookmark213)

[表7-53 OBSVM 数据结构 137](#_bookmark215)

[表7-54 Unicore 消息中的卫星 PRN 138](#_bookmark216)

[表7-55 Unicore 消息中的卫星 PRN 偏移 138](#_bookmark217)

[表7-56 通道跟踪状态 139](#_bookmark218)

[表7-57 OBSVH 数据结构 141](#_bookmark220)

[表7-58 OBSVMCMP 压缩说明 143](#_bookmark222)

[表7-59 Psrstd Index 表 144](#_bookmark223)

[表7-60 OBSVMCMP 数据结构 144](#_bookmark224)

[表7-61 OBSVHCMP 压缩说明 146](#_bookmark226)

[表7-62 OBSVHCMP 数据结构 146](#_bookmark227)

[表7-63 OBSVBASE 数据结构 148](#_bookmark229)

[表7-64 BASEINFO 数据结构 150](#_bookmark231)

[表7-65 GPSION 数据结构 151](#_bookmark233)

[表7-66 BD3ION 数据结构 153](#_bookmark235)

[表7-67 BDSION 数据结构 154](#_bookmark237)

[表7-68 GALION 数据结构 155](#_bookmark239)

[表7-69 GPSUTC 数据结构 156](#_bookmark241)

[表7-70 BD3UTC 数据结构 158](#_bookmark243)

[表7-71 BDSUTC 数据结构 159](#_bookmark245)

[表7-72 GALUTC 数据结构 161](#_bookmark247)

[表7-73 GPSEPH 数据结构 162](#_bookmark249)

[表7-74 QZSSEPH 数据结构 165](#_bookmark251)

[表7-75 BD3EPH 数据结构 168](#_bookmark253)

[表7-76 BDSEPH 数据结构 171](#_bookmark255)

[表7-77 GLOEPH 数据结构 174](#_bookmark257)

[表7-78 GLONASS 星历标志代码 176](#_bookmark258)

[表7-79 P1 标志取值范围 177](#_bookmark259)

[表7-80 GALEPH 数据结构 178](#_bookmark261)

[表7-81 IRNSSEPH 数据结构 181](#_bookmark263)

[表7-82 AGRIC 数据结构 184](#_bookmark265)

[表7-83 PVTSLN 数据结构 188](#_bookmark267)

[表7-84 UNILOGLIST 数据结构 190](#_bookmark269)

[表7-85 端口标识符 191](#_bookmark270)

[表7-86 BESTNAV 数据结构 192](#_bookmark272)

[表7-87 GPS/GLONASS/BDS2 使用的信号掩码 194](#_bookmark273)

[表7-88 Galileo&BDS3 使用的信号掩码 194](#_bookmark274)

[表7-89 扩展解状态 194](#_bookmark275)

[表7-90 BESTNAVXYZ 数据结构 196](#_bookmark277)

[表7-91 BESTNAVH 数据结构 198](#_bookmark279)

[表7-92 BESTNAVXYZH 数据结构 201](#_bookmark281)

[表7-93 BESTSAT 数据结构 203](#_bookmark283)

[表7-94 BESTSAT GPS Signal Mask 205](#_bookmark284)

[表7-95 BESTSAT GLONASS Signal Mask 205](#_bookmark285)

[表7-96 BESTSAT BDS Signal Mask 205](#_bookmark286)

[表7-97 BESTSAT Galileo Signal Mask 206](#_bookmark287)

[表7-98 ADRNAV 数据结构 207](#_bookmark289)

[表7-99 ADRNAVH 数据结构 209](#_bookmark291)

[表7-100 PPPNAV 数据结构 212](#_bookmark293)

[表7-101 SPPNAV 数据结构 214](#_bookmark295)

[表7-102 SPPNAVH 数据结构 217](#_bookmark297)

[表7-103 STADOP 数据结构 219](#_bookmark299)

[表7-104 STADOPH 数据结构 221](#_bookmark301)

[表7-105 ADRDOP 数据结构 222](#_bookmark303)

[表7-106 ADRDOPH 数据结构 224](#_bookmark305)

[表7-107 PPPDOP 数据结构 225](#_bookmark307)

[表7-108 SPPDOP 数据结构 227](#_bookmark309)

[表7-109 SPPDOPH 数据结构 228](#_bookmark311)

[表7-110 SATSINFO 数据结构 230](#_bookmark313)

[表7-111 频率标识 231](#_bookmark315)

[表7-112 系统标识 232](#_bookmark316)

[表7-113 频点标识 232](#_bookmark317)

[表7-114 BASEPOS 数据结构 234](#_bookmark319)

[表7-115 SATELLITE 数据结构 237](#_bookmark321)

[表7-116 卫星系统 238](#_bookmark322)

[表7-117 SATECEF 数据结构 240](#_bookmark324)

[表7-118 RECTIME 数据结构 241](#_bookmark326)

[表7-119 UNIHEADING 数据结构 243](#_bookmark329)

[表7-120 UNIHEADING2 数据结构 245](#_bookmark331)

[表7-121 HEADINGSTATUS 数据结构 247](#_bookmark333)

[表7-122 RTKSTATUS 数据结构 248](#_bookmark335)

[表7-123 RTKSTATUS2 数据结构 251](#_bookmark337)

[表7-124 AGNSSSTATUS 数据结构 254](#_bookmark339)

[表7-125 RTCSTATUS 数据结构 256](#_bookmark341)

[表7-126 JAMSTATUS 数据结构 257](#_bookmark343)

[表7-127 FREQJAMSTATUS 数据结构 258](#_bookmark345)

[表7-128 RTCMSTATUS 数据结构 260](#_bookmark347)

[表7-129 L1\~L6 对应关系表 261](#_bookmark348)

[表7-130 HWSTATUS 数据结构 263](#_bookmark350)

[表7-131 HWFLAG 字段比特位说明表 264](#_bookmark351)

[表7-132 AGC 数据结构 265](#_bookmark353)

[表7-133 KSXT 数据结构 266](#_bookmark355)

[表7-134 INFOPART1 数据结构 268](#_bookmark357)

[表7-135 INFOPART2 数据结构 270](#_bookmark359)

[表7-136 MSPOS 数据结构 271](#_bookmark361)

[表7-137 TROPINFO 数据结构 273](#_bookmark363)

[表7-138 PPPB2BINFO1 数据结构 274](#_bookmark365)

[表7-139 PPPB2BINFO2 数据结构 275](#_bookmark367)

[表7-140 PPPB2BINFO3 数据结构 276](#_bookmark369)

[表7-141 PPPB2BINFO4 数据结构 278](#_bookmark371)

[表7-142 PPPB2BINFO5 数据结构 280](#_bookmark373)

[表7-143 PPPB2BINFO6 数据结构 281](#_bookmark375)

[表7-144 PPPB2BINFO7 数据结构 283](#_bookmark377)

[表7-145 E6MASKBLOCK 数据结构 285](#_bookmark379)

[表7-146 卫星掩码 287](#_bookmark380)

[表7-147 信号掩码 288](#_bookmark381)

[表7-148 导航电文索引 288](#_bookmark382)

[表7-149 E6ORBITBLOCK 数据结构 289](#_bookmark384)

[表7-150 有效期间隔 291](#_bookmark385)

[表7-151 E6CLOCKFULLBLOCK 数据结构 292](#_bookmark387)

[表7-152 DCM 参数 294](#_bookmark388)

[表7-153 E6CLOCKSUBBLOCK 数据结构 294](#_bookmark390)

[表7-154 E6CBIASBLOCK 数据结构 297](#_bookmark392)

[表7-155 E6PBIASBLOCK 数据结构 299](#_bookmark394)

[表7-156 BSLNENUHD2 数据结构 301](#_bookmark396)

[表7-157 BSLNXYZHD2 数据结构 303](#_bookmark398)

[表7-158 DOPHD2 数据结构 305](#_bookmark400)

[表7-159 L6MDCTYPE1 数据结构 306](#_bookmark402)

[表7-160 L6 改正数消息头 307](#_bookmark403)

[表7-161 L6MDCTYPE2 数据结构 309](#_bookmark405)

[表7-162 L6MDCTYPE3 数据结构 311](#_bookmark407)

[表7-163 L6MDCTYPE4 数据结构 312](#_bookmark409)

[表7-164 L6MDCTYPE5 数据结构 314](#_bookmark411)

[表7-165 L6MDCTYPE7 数据结构 315](#_bookmark413)

[表 7-166 ENVINFO 数据结构 316](#_bookmark415)

[表 7-167 基站打分分值标准 317](#_bookmark416)

[表8-1 Unlog 指令参数 319](#_bookmark419)

[表8-2 Freset 指令参数 320](#_bookmark421)

[表8-3 Reset 指令参数 321](#_bookmark423)

[表8-4 Saveconfig 指令参数 322](#_bookmark425)

[表0- 1 EVENTFLAG 数据结构 330](#_bookmark430)

[表0- 2 STATUS 字段比特位说明 331](#_bookmark431)

[表0- 3 EVENTSLN 数据结构 332](#_bookmark433)

[表0- 4 位置或速度类型 334](#_bookmark434)

[表0- 5 解的状态 335](#_bookmark435)

# 常用配置指令

和芯星通科技（北京）有限公司高精度接收机输入指令支持不带校验的简化 ASCII 格式以及带校验的ASCII 格式，示例如下：

不带校验的指令：RESET 带校验的指令：\$RESET\*55

无校验位的简化ASCII 格式更便于用户输入，而带校验位的ASCII 格式则可以避免模块误识别指令。默认情况下，模块仅识别不带校验的简化 ASCII 格式，用户如需使用带校验的指令，则需要首先配置 CONFIG CMDFORMAT 1（详见第 [4.40](#_bookmark120) 章），之后再输入带校验的指令。

所有指令由指令头和配置参数（参数部分可以为空，则该指令只有一个指令头）组成，头字段包含指令名称或消息头。常用指令如下表所示：

表 1-1 常用指令集

| 指令         | 描述                                                                          |
|--------------|-------------------------------------------------------------------------------|
|  freset      | 清除保存的接收机设置、卫星星历、位置信息等，串口波特 率变为 115200bps         |
| version      | 查询版本号                                                                    |
| config       | 查询接收机串口状态                                                            |
|  mask BDS    | 禁用 BDS 卫星系统 可以分别禁用 BDS、GPS、GLO、GAL                             |
|   unmask BDS | 启用 BDS 卫星系统 可以分别启用 BDS、GPS、GLO、GAL；接收机默认跟踪所有卫星系统 |

| 指令                                                                                              | 描述                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    config com1 115200                                                                             | 设置 com1 波特率为 115200 可以分别对 com1、com2、com3 设置为 9600, 19200, 38400, 57600, 115200, 230400，460800，921600 中任意 一个波特率                                                                                           |
| unlog                                                                                             | 禁止当前串口所有输出                                                                                                                                                                                                               |
| saveconfig                                                                                        | 保存设置                                                                                                                                                                                                                           |
|   mode base time 60                                                                               | 接收机自主定位 60 秒，把水平定位的平均值和高程定位的平均值作为基准站坐标值 断电重启后，将重复计算并生成新基准点坐标                                                                                                                |
|      mode base lat Lon height                                                                     | 手动设置基准点坐标为：lat，lon，height（断电重启后基准点坐标不变化）举例 lat=40.07898324818, lon=116.23660197714, height=60.4265 注：经度纬度坐标可以通过 bestnav 命令获取；若位置为南纬，Lat 值需输入负值；西经，lon 需输入负值。 |
| mode base                                                                                         | 设置为基准站                                                                                                                                                                                                                       |
|  mode rover                                                                                       | 缺省 Rover 模式（该指令可使接收机从基站模式转换到流动 站模式）                                                                                                                                                                     |
| rtcm1033 comx 10 rtcm1006 comx 10 rtcm1074 comx 1 rtcm1124 comx 1 rtcm1084 comx 1 rtcm1094 comx 1 |    基站模式及流动站模式设置 COMX 发送差分报文，COMX 可以指定为 COM1、COM2、COM3 等任意一个                                                                                                                                         |
| *NMEA0183* 输出语句                                                                               |                                                                                                                                                                                                                                    |

| 指令            | 描述                                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    gpgga comx 1 | 设置 1Hz 输出 GGA 消息 消息类型和更新率可自设：更新率可设置为 1、0.5、0.2、 0.1、0.05、0.02\*，分别对应输出频率 1Hz、2Hz、5Hz、 10Hz、20Hz、50Hz\*；类型包括 GGA、RMC、ZDA、VTG 等 |
| gpths comx 1    | 输出当前时刻的航向信息 THS                                                                                                                                                         |

### 基准站设置

固定基站即将接收机天线安装在固定位置，在整个使用过程中不移动。同时将已知测站的精密坐标和接收到的卫星信息直接或经过处理后（如 RTCM 格式的改正数信息）实时发送给流动站接收机（待定位点），流动站接收机在接收卫星观测值的同时也接收到基准站的信息，进行 RTK 定位解算，实现 RTK 高精度定位，达到 cm 或者 mm 级定位精度。

适用产品：UM960、UMD960、UM960L、UM982、UMD982、UM980、UMD980、 UB9A0、UBD9A0

在已知精密坐标时输入接收机中的指令如下[表1-2 固定基站模式](#_bookmark5)。

表 1-2 固定基站模式

| 序号 | 指令                                       | 说明                                              |
|------|--------------------------------------------|---------------------------------------------------|
|  1   | mode base 40.078983248 116.236601977 60.42 | 设置为基站模式，并配置精确的纬度、经度和 高程信息 |
| 2    | rtcm1006 com2 10                           | RTK 基准站天线参考点坐标（含天线高）              |
| 3    | rtcm1033 com2 10                           | 接收机和天线说明                                  |
| 4    | rtcm1074 com2 1                            | GPS 差分电文                                      |
| 5    | rtcm1124 com2 1                            | BDS 差分电文                                      |

\* 50Hz 输出频率需要特定产品、特定固件支持

| 序号 | 指令            | 说明             |
|------|-----------------|------------------|
| 6    | rtcm1084 com2 1 | GLO 差分电文     |
| 7    | rtcm1094 com2 1 | Galileo 差分电文 |
| 8    | saveconfig      | 保存配置         |

自主优化设置基准站：即在将架设基准站的点没有精确坐标时，可设置接收机在安装点上进行一定时间的收敛和自主优化，取此段时间内的平均值设置为基准站的坐标。指令如[表1-3 自主优化设置基站模式](#_bookmark6)。

表 1-3 自主优化设置基站模式

| 序号 | 指令                 | 说明                                                                                                                   |
|------|----------------------|------------------------------------------------------------------------------------------------------------------------|
|    1 |    mode base time 60 | 接收机自主定位 60 秒，把水平定位的平均值和高程定位的平均值作为基准站坐标值 断电重启后，将重复计算并生成新基准点坐 标。 |
| 2    | rtcm1006 com2 10     | RTK 基准站天线参考点坐标（含天线高）                                                                                   |
| 3    | rtcm1033 com2 10     | 接收机和天线说明                                                                                                       |
| 4    | rtcm1074 com2 1      | GPS 差分电文                                                                                                           |
| 5    | rtcm1124 com2 1      | BDS 差分电文                                                                                                           |
| 6    | rtcm1084 com2 1      | GLO 差分电文                                                                                                           |
| 7    | rtcm1094 com2 1      | Galileo 差分电文                                                                                                       |
| 8    | saveconfig           | 保存配置                                                                                                               |

### 流动站设置

RTK 流动站（移动站）是实时接收基准站的差分改正数信息，同时接收卫星信号进行 RTK 定位解算，实现 RTK 高精度定位。接收机可自适应识别 RTCM 数据输入的端口和格式。RTK 流动站的常用指令为：

MODE ROVER SAVECONFIG

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

### Heading 设置

本指令用于设置支持单板卡（模块）双天线定向的接收机。Heading 定向是指双天线 接收机的主天线（ANT1）与从天线（ANT2）之间构成一个基线向量，确定真北顺时针方 向与此基线向量的夹角。单板卡（模块）双天线定向的接收机默认开机进行 Heading 工作。原理示意图如[图3-1 定向原理结构图](#_bookmark29)。

命令如下： GPTHS 1 SAVECONFIG

适用产品：UM982、UMD982

### Heading2 定向设置

Heading2 定向是指基站的 GNSS 天线与流动站天线构成一个基线向量，确定真北顺时针方向与此基线向量的夹角。

支持双天线定向的接收机，Heading2 定向是指双天线接收机的主天线（ANT1）与基站的 GNSS 天线之间的定向。原理结构图如[图3-1 定向原理结构图](#_bookmark29)。

定向常用指令如下： MODE HEADING2 GPTHS2 ONCHANGED SAVECONFIG

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、 UM982、 UMD982

# 接收机命令分类

高精度接收机的命令主要分为 MODE 指令集，CONFIG 指令集，MASK 指令集， AGNSS 指令集，数据输出指令集，保存配置和恢复出厂设置等指令。

表 2-1 接收机指令集分类

| 序号  | 指令            | 描述                                        | 适用接收机型号                                                |
|-------|-----------------|---------------------------------------------|---------------------------------------------------------------|
|     1 |     MODE 指令   |  配置接收机的工作模式，比如：基站、流动站等 | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|       |                 |   查询接收机当前的工作模式                  | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|     2 |     CONFIG 指令 |  配置接收机的功能和接口相关的指令集         | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|       |                 |   查询接收机当前的配置信息                  | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|     3 |     MASK 指令   |  设置接收机跟踪的卫星系统、频点、高度角     | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|       |                 |  查询接收机跟踪的卫星系统、频点、高度角     | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|  4    |  AGNSS 指令     | 输入辅助位置信息及辅助时间 信息             | UM982/UMD982/UM980/UMD980/ UB9A0/UBD9A0                       |

| 序号 | 指令            | 描述                              | 适用接收机型号                                                |
|------|-----------------|-----------------------------------|---------------------------------------------------------------|
|   5  |  数据输出指令集 |  请求输出定位，定向等信息的指令集 | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |
|   6  |   其它指令      |  保存配置，恢复出厂配置等指令     | UM960/ UMD960/UM960L/UM980/ UMD980/UM982/UMD982/UB9A0/ UBD9A0 |

# MODE 指令

MODE 指令用来设置接收机工作模式，接收机的工作模式有基准站工作模式，流动站工作模式，定向工作模式，高精度授时工作模式。向接收机重新输入新的工作模式指令，接收机将按照最后一次输入的工作模式重新解算。例如接收机处于基准站工作模式，重新发送 RTK 流动站工作模式，接收机将进入流动站工作模式，进行 RTK 初始化等计算工作。接收机具备上述所有功能的工作模式，但是实际使用时需要根据实际购买的授权获得相应功能。接收机默认是流动站工作模式，并且接收机能自动识别 RTCM 数据格式协议类别，用户无需指定类型。

命令格式为：

MODE [模式名称] [参数]

命令示例：

MODE BASE 40.45628476579 116.2859754968 58.0984 MODE ROVER

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 3-1 接收机工作模式列表

| 序号 | 工作模式 | 接收机工作模式描述           |
|------|----------|------------------------------|
| 1    | BASE     | 设置接收机作为基准站工作模式 |
| 2    | ROVER    | 设置接收机作为流动站工作模式 |
| 3    | HEADING2 | 设置接收机为定向工作模式     |

### 接收机工作模式查询

高精度接收机支持用 MODE 指令查询接收机当前的工作模式。

命令格式为：

MODE

命令示例：

MODE

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

信息输出示例：

\#MODE,81,GPS,FINE,2230,547967000,0,0,18,518;MODE ROVER SURVEY,\*1B

表 3-2 接收机工作模式查询指令

| 指令 | 描述                                         |
|------|----------------------------------------------|
| MODE | 查询接收机当前的工作模式，比如：基站、流动站 |

表 3-3 MODE 消息说明

| 序号   | 内容      | 描述                                                                                                                     |
|--------|-----------|--------------------------------------------------------------------------------------------------------------------------|
| 1      | HEADER    | ASCII 消息头结构请参考[表7-51](#_bookmark211)                                                                            |
|      2 |      MODE | 工作模式（以下内容标识）： MODE ROVER UAV MODE ROVER AUTOMOTIVE MODE ROVER SURVEY MODE BASE MODE BASE TIME MODE HEADING2 |

| 序号   | 内容             | 描述                                                                                                                                                                                   |
|--------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      3 |      HEADINGMODE | HEADING2 模式（以下内容标识） HEADINGMODE FIXLENGTH HEADINGMODE VARIABLELENGTH HEADINGMODE LOWDYNAMIC HEADINGMODE STATIC HEADINGMODE TRACTOR HEADING2 模式未使能的情况下，此字段为空。 |
|  4     |  \*xx            | 异或校验，\# 到 \* 之间（包括 \#，不包括 \*）的数异 或后的值，十六进制                                                                                                                 |
| 5      | [CR][LF]         | 语句结束符(仅 ASCII)                                                                                                                                                                   |

### 以精确坐标设置基准站模式

本指令设置基准站接收机的坐标值，使接收机以基准站模式工作。接收机支持大地坐标系和地心地固坐标系下的坐标输入。设置基准站坐标后， 接收机输出的位置信息

（GPGGA 语句中）始终显示输入的坐标值。

如果接收机自身解出的坐标（可通过 BASEPOS 指令输出）与用户设置的坐标之间的 3D 误差超过 300 米，则不输出 RTCM 数据。

开阔环境下，推荐将 PVT 解算引擎配置为 MULTI，即 CONFIG PVTALG MULTI，以提高定位精度。

命令格式为：

MODE BASE [ID] [param1 param2 param3]

命令示例：

MODE BASE 40.45628476579 116.2859754968 58.0984

MODE BASE -2160489.0276 4383620.1006 4084738.1110

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 3-4 基准站工作模式参数列表

| 模式命令                 | 模式名称                 | ID                                                        | 参数列表     | 参数描述                                                                                         |
|--------------------------|--------------------------|-----------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------|
|                     MODE |                     BASE |                  基站标识， 0\~4095 之间的整数（可省略）1 |      param1  | 输入坐标参数： -90 ≤ param1 ≤ 90，为大地坐标系下的纬度坐标，以度为单位，输入有效位 11 位         |
|                          |                          |                                                           |              | param1＜-90 或者param1＞90，为地心地固坐标系下的 X 轴坐标 值，以米为单位，输入有效位 4 位        |
|                          |                          |                                                           |       param2 | 输入坐标参数： -180 ≤ param2 ≤ 180，为大地坐标系下的经度坐标，以度为单位，输入有效位 11 位       |
|                          |                          |                                                           |              | Param2 ＜ -180 或者 param2 ＞ 180，为地心地固坐标系下的 Y 轴坐标值，以米为单位，输入有效位 4 位  |
|                          |                          |                                                           |       param3 | 输入坐标参数： -30000 ≤ param3 ≤ 30000，为海拔高，以米为单位，输入有效位 6 位                    |
|                          |                          |                                                           |              | Param3＜-30000 或者 Param3＞ 30000，为地心地固坐标系下的 Z轴坐标值，以米为单位，输入有效 位 4 位 |

1 仅对 RTCM3.2 有效

### 以自主优化方式设置基准站模式

接收机以自主优化的方式进入基准站模式。

开阔环境下，推荐将PVT 解算引擎配置为MULTI，即 CONFIG PVTALG MULTI，以提高定位精度。

命令格式为：

MODE BASE [ID] TIME [T] [Distance]

命令示例：

MODE BASE TIME 60 MODE BASE TIME 60 5

MODE BASE 1 TIME 60

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 3-5 基准站工作模式参数列表

| 模式命令       | 模式名称       | ID                                   | 指令名称       | 参数列表      | 参数描述                                                                                                                                                                         |
|----------------|----------------|--------------------------------------|----------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           MODE |           BASE |        0\~4095 之间的整数 （可省略） |           Time |    T          | 计算平均位置的最大时长，以秒为单位，不可以输入负值，最大不超过 3600 秒。收敛时间从定位质量较好的点开始计 算，非首个点开始计算。                                                  |
|                |                |                                      |                |      Distance | 距离，以米为单位。接收机以自主优化方式设置基站模式启动， 优化的坐标将保存到 flash 中。当接收机重新启动，将再次以自主优化方式计算坐标，若新计算的坐标 与 flash 中存储的坐标距离小 |

| 模式命令 | 模式名称 | ID | 指令名称 | 参数列表 | 参数描述                                                                                                                                                                                      |
|----------|----------|----|----------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          |          |    |          |          | 于“ Distance ”，接收机将用 flash 中存储的坐标作为基站坐标。“ Distance ”取值范围：0≤Distance≤10。当 Distance = 0 时，接收机以自主优化方式设置基站模式启动，以本次优化的结果坐标 作为基站坐标。 |

### 缺省参数的基站模式

缺省参数的基站模式，MODE BASE，输入指令 BASE 后面不带参数。接收机将启动默认的基准站配置。基准站默认配置为：接收机当前定位结果 60 秒的坐标平均值设置为基准站的坐标。60 秒的平均值满足以下条件：优化时间达到 60s，或者位置平均的平面精度限差达到默认值 2.5m 且位置平均的高程精度限差达到默认值 3.5m。

开阔环境下，推荐将 PVT 解算引擎配置为 MULTI，即 CONFIG PVTALG MULTI，以提高定位精度。

命令格式为：

MODE BASE

命令示例：

MODE BASE

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 3-6 基准站工作模式参数列表

| 模式命令 | 模式名称 | 参数列表 | 参数描述           |
|----------|----------|----------|--------------------|
| MODE     | BASE     | -        | 设置为默认基站模式 |

### 设置基准站的 ID 号

设置基准站的 ID 号。ID 的取值范围 0\~4095（0 ≤ ID \< 4096）之间的整数。

命令格式为：

MODE BASE [ID]

命令示例：

MODE BASE 1

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 3-7 基准站工作模式参数

| 模式命令 | 模式名称 | ID                  | 参数描述                                      |
|----------|----------|---------------------|-----------------------------------------------|
|  MODE    |  BASE    | 0≤ID\<4096 （整数） | 设置接收机为基准站工作模式，并设 置其 ID 号。 |

### 流动站模式指令

该指令用于配置接收机在移动站模式下根据不同的应用场景选择最适合的工作模式。

命令格式为：

MODE ROVER [参数 1] [参数 2（可选）]

命令示例：

MODE ROVER UAV MODE ROVER SURVEY

MODE ROVER UAV HIGHDYN

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

-   UM980 Build7923 及之后的版本支持；
-   UM982 Build7650 及之后的版本支持。

表 3-8 流动站指令格式说明

| 模式命令      | 参数 1     | 参数 2（可选） | 备注                       |
|---------------|------------|----------------|----------------------------|
|    MODE ROVER |  UAV       | DEFAULT        | 无人机飞行动态模式（默认） |
|               |            | HIGHDYN        | 无人机高机动飞行模式       |
|               |  SURVEY    | DEFAULT        | 精准测量模式（默认）       |
|               |            | MOW            | 割草机模式                 |
|               | AUTOMOTIVE | DEFAULT        | 车载动态模式（默认）       |

-   参数 2 配置为空时，则为默认模式。

无人机飞行动态模式（UAV）：适用于大多数无人机动态场景，如农业无人机、测绘无人机、航拍无人机、巡检巡线无人机等，垂直加速度大、水平速度与车载相当的场景，水平最大速度 50m/s，最大垂直速度 30m/s，最大海拔高 18000m，位置变化率大。

无人机高机动飞行模式（UAV HIGHDYN）：适用于对无人机机动性要求更高的应用场景，如编队表演无人机，穿越无人机等。

车载动态模式（AUTOMOTIVE）：适用于乘用车、园区物流智能驾驶类应用，垂直加速度较低，场景变化多样，最大水平速度 100m/s，最大垂直速度 15m/s，位置变化率一般。

精准测量模式（SURVEY）：该场景主要适配高精度测量型天线，对定位精度要求更高、动态特性低的应用场景。场景适配测量测绘、精准农业等应用。

默认模式：根据板卡型号选择不同的默认模式，且默认状态可被查询。

表 3-9 流动站模式默认配置

| 产品型号                         | 默认模式   | 备注               |
|----------------------------------|------------|--------------------|
| UM980/UMD980/UMD960/UB9A0/UBD9A0 | SURVEY     | 精准测量模式       |
| UM982/UMD982                     | UAV        | 无人机飞行动态模式 |
|  UM960                           | SURVEY MOW | 割草机模式         |

### Heading2 模式指令

本指令用于设置用两个接收机之间进行定向。Heading2 定向是指基站的 GNSS 天线与流动站天线构成一个基线向量，确定真北顺时针方向与此基线向量的夹角。

支持双天线定向接收机，Heading2 定向是指双天线接收机的主天线（ANT1）与基站的 GNSS 天线之间的定向。原理结构图如[图3-1 定向原理结构图](#_bookmark29)。

![](media/63c6b474d0e7dd041d2e08d1c6a7346b.jpeg)

图 3-1 定向原理结构图

命令格式为：

MODE HEADING2 [参数]

命令示例：

MODE HEADING2

MODE HEADING2 FIXLENGTH

MODE HEADING2 VARIABLELENGTH MODE HEADING2 STATIC

MODE HEADING2 LOWDYNAMIC

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

表 3-10 定向工作模式参数

| 模式命令           | 模式名称               | 指令参数         | 参数描述                                                                                                                                                 |
|--------------------|------------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|               MODE |               HEADING2 |    FIXLENGTH     | 使能 Heading2 定向模式，并且进入移动基站和定向端的天线间距离保持固定，两天线可同步运动或静止的定向模式（mode heading2 参数空缺时默认 为 FIXLENGTH 模式） |
|                    |                        |   STATIC         | 使能 Heading2 定向模式，并且进入移动基站和定向端的天线均在静止状态的 定向模式                                                                            |
|                    |                        |   VARIABLELENGTH | 使能 Heading2 定向模式，并且进入移动基站和定向端的天线相对位置、距离 实时动态变化的定向模式                                                              |
|                    |                        |   LOWDYNAMIC     | 使能 Heading2 定向模式，低动态，适用于打桩机之类的低速运动载体，移动 基站和定向端的天线间距离保持固定。                                                  |
|                    |                        |  TRACTOR         | 针对农机应用，工作模式，移动基站和 定向端的天线间距离保持固定。                                                                                          |

# CONFIG 指令

CONFIG 是用于配置接收机串口、PPS 脉冲、高程异常值、DGNSS 引擎、RTK 引擎等属性的指令头，即进行接收机属性配置时需要以 CONFIG 为命令头，目前支持配置如下：

1.  接收机串口波特率等属性；
2.  PPS 输出脉冲周期等特性；
3.  高程异常值；
4.  DGPS 引擎属性；
5.  RTK 引擎属性
6.  Heading 引擎属性
7.  Heading2 引擎属性
8.  SBAS 功能
9.  EVENT 功能

    ……

可解析的字符包括：数字、大小写字母、一些特定的非法字符，包括双引号（“ ”）、连接符（-）、冒号（:）、下划线（_）、美元符（\$）、逗号（,）、正斜线（/）、反斜线

（\\\\）。除以上字符外，不解析为命令。

命令格式：

CONFIG [设备/功能名称] [参数]

命令示例：

CONFIG COM1 115200 8 n 1

CONFIG PPS ENABLE BDS POSITIVE 100000 1000 0 0

CONFIG UNDULATION 9.7 CONFIG RTK TIMEOUT 60 CONFIG DGPS TIMEOUT 100

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、

UM982、UMD982

表 4-1 设备/功能名称列表

| 序号 | 设备/功能名称 | 参数描述                                                                                        |
|------|---------------|-------------------------------------------------------------------------------------------------|
| 1    | COM1          | COM1 串口，与 COM1 相关的配置，如波特率，[奇偶校验](http://baike.baidu.com/view/444171.htm)比特 |
| 2    | COM2          | COM2 串口，与 COM2 相关的配置，如波特率，[奇偶校验](http://baike.baidu.com/view/444171.htm)比特 |
| 3    | COM3          | COM3 串口，与 COM3 相关的配置，如波特率，[奇偶校验](http://baike.baidu.com/view/444171.htm)比特 |
| 4    | PPS           | 设置接收机输出特定周期、脉宽的 PPS 脉冲信号、上下沿                                             |
| 5    | EVENT         | 设置外部事件输入                                                                                |
| 6    | UNDULATION    | 设置输入特定的大地水准面差距或使用内置大地水准面差距格网值                                      |
| 7    | RTK           | 配置 RTK 参数，如设置模式，差分有效时间                                                         |
| 8    | DGPS          | 配置 DGPS 参数，如 DGPS 差分有效时间                                                            |

### 接收机的配置查询

高精度接收机支持用 CONFIG 指令查询接收机当前的配置信息。

命令格式：

CONFIG

命令示例：

CONFIG

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

输出示例：

\$CONFIG,COM1,CONFIG COM1 460800\*65

\$CONFIG,COM2,CONFIG COM2 115200\*23

\$CONFIG,COM3,CONFIG COM3 115200\*23

\$CONFIG,PPS,CONFIG PPS ENABLE GPS POSITIVE 500000 1000 0 0\*6E

表 4-2 接收机配置查询指令

| 指令   | 描述                             |
|--------|----------------------------------|
| CONFIG | 查询接收机当前功能及当前配置信息 |

注：CONFIG 配置可以查询到当前接收机的配置状态（包括默认配置状态均可被查询）。

### 串口配置

串口是接收机输入和输出数据的接口。配置串口指令以 CONFIG 为指令头，指令头后是串口的设备及串口属性，用于设置串口的波特率，数据位，奇偶校验，停止位特性等。

高精度 GNSS 接收机支持 3 个串口，分别是COM1，COM2，COM3。接收机三个串口功能相同，但各串口数据输入输出以各自配置进行独立工作。另外，三个串口可以相互配置，即通过 COM1 可以配置 COM2 的串口属性，同时通过 COM2 可以配置 COM1 的串口属性。在集成 GNSS 板卡或者模块时建议保留 COM1 为升级接口。

命令格式：

CONFIG [串口设备号] [串口属性参数]

命令示例：

CONFIG COM1 115200

CONFIG COM1 115200 8 n 1

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-3 串口设备参数列表

| 指令       | 串口设备          | 序号 | 串口参数  | 参数描述                                                                                                                        |
|------------|-------------------|------|-----------|---------------------------------------------------------------------------------------------------------------------------------|
|     CONFIG |    COM1 COM2 COM3 |  1   |  波特率   | 设置串口的波特率。串口支持的波特率见[表](#_bookmark37) [4-4 串口支持的波特率](#_bookmark37)                                     |
|            |                   |    2 |    数据位 | 设置串口的数据位；若要设置串口的数据位，须确保前面的波特率不能为空。 注: 数据传输中支持的数据位：7 或 8，目前 产品仅支持 8 位。 |

| 指令 | 串口设备 | 序号 | 串口参数    | 参数描述                                                                                                                    |
|------|----------|------|-------------|-----------------------------------------------------------------------------------------------------------------------------|
|      |          |    3 |    奇偶校验 | 设置串口的奇偶校验；若要设置串口奇偶校验，须确保前面的参数不能为空。 注：数据传输中支持的奇偶校验：N，E， O。缺省默认为 N。 |
|      |          |    4 |    停止位   | 设置串口的停止位；若要设置串口停止位，须确保前面的参数不能为空。 注：数据传输中支持的停止位：1 或 2。缺 省默认为 1。        |

表 4-4 串口支持的波特率

| 接口名称 | 描述                                                      |
|----------|-----------------------------------------------------------|
| COM1     | 9600, 19200, 38400, 57600, 115200, 230400, 460800, 921600 |
| COM2     | 9600, 19200, 38400, 57600, 115200, 230400, 460800, 921600 |
| COM3     | 9600, 19200, 38400, 57600, 115200, 230400, 460800, 921600 |

### PPS 脉冲配置

该指令设置接收机输出特定周期、脉宽的 PPS 脉冲信号，并可对 PPS 延迟进行补偿。

命令格式：

CONFIG PPS [设备参数]

命令示例：

CONFIG PPS ENABLE GPS POSITIVE 500000 1000 0 0

适用产品：UM960、UMD960、UM960L2、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

2 UM960L 不支持 ENABLE2、ENABLE3

表 4-5 PPS 功能表

| 指令头         | 功能名称    | 使能参数         | 描述                                                                                                                         |
|----------------|-------------|------------------|------------------------------------------------------------------------------------------------------------------------------|
|         CONFIG |         PPS | DISABLE          | 关闭 PPS 输出                                                                                                                |
|                |             |  ENABLE （默认） | 使能 PPS 输出，在模组/板卡定位后且 PPS 完成收敛后输出 PPS，当卫星失锁，接收机不定位时，PPS 会 维持大概 30 秒左右后停止输出。 |
|                |             |   ENABLE2        | 使能 PPS 输出，PPS 输出后一直保持。当模组/板卡正常定位且PPS 收敛完成，输出和 ENABLE 配置同样 误差的 PPS                      |
|                |             |  ENABLE3         | 使能 PPS 信号输出，在接收机启动之后一直保持 PPS 信号输出。                                                                   |

表 4-6 PPS 配置指令

| 指令头            | 功能名称       | 使能参数                                | PPS 参数  | ASCII 值                | 描述                                  |
|-------------------|----------------|-----------------------------------------|-----------|-------------------------|---------------------------------------|
|            CONFIG |            PPS |  DISABLE                                |  -        |  -                      | 关闭 PPS 输出，DISABLE 后不跟其它参数 |
|                   |                |       ENABLE （默认）/ ENABLE2/ ENABLE3 |  Timeref  | GPS/BDS/G AL/GLO        | 当前仅支持 BDST 、 GPST、GLOST、GALST |
|                   |                |                                         |  polarity | POSITIVE                | PPS 上升沿有效                        |
|                   |                |                                         |           | NEGATIVE                | PPS 下降沿有效                        |
|                   |                |                                         |  Width    | 脉冲宽度应 小于周期     |  PPS 脉冲宽度（微秒）                 |
|                   |                |                                         |  Period   | 脉冲输出的 周期         | 毫秒，取值为：50，100， 200，…，20000 |
|                   |                |                                         |   RfDelay | -32768 \~32767 间的整数 |   RF 延迟（纳秒）                     |

| 指令头 | 功能名称 | 使能参数 | PPS 参数    | ASCII 值                | 描述                   |
|--------|----------|----------|-------------|-------------------------|------------------------|
|        |          |          |   UserDelay | -32768 \~32767 间的整数 |   用户设置延迟（纳秒） |

### 高程异常改正值

该指令输入特定的大地水准面差距或使用内置大地水准面差距格网值。

当需要配置接收机为基准站模式时，应当先配置 UNDULATION 再进行基准站配置。

命令格式：

CONFIG UNDULATION [参数]

命令示例：

CONFIG UNDULATION 9.7

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-7 高程异常改正值配置表格

| 指令头    | 功能名称      | 参数列表        | 参数描述                                                                 |
|-----------|---------------|-----------------|--------------------------------------------------------------------------|
|    CONFIG |    UNDULATION | Auto            | 使用内置格网表（默认配置）                                               |
|           |               |   Separation(m) | 使用用户指定的大地水准面差距值，取值范围：±1000.0000m，小数点后四 位有效 |

### DGPS 伪距差分数据龄期配置

该指令用于设置接收的DGPS 差分数据的最大龄期。接收到的滞后于指定龄期的DGPS差分数据被忽略，也用于禁止 DGPS 定位计算。

命令格式：

CONFIG DGPS [参数]

命令示例：

CONFIG DGPS TIMEOUT 100

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-8 配置 DGPS 伪距差分数据龄期

| 指令头    | 功能名称 | 参数       | 参数列表 | 参数描述                                                                                      |
|-----------|----------|------------|----------|-----------------------------------------------------------------------------------------------|
|    CONFIG |    DGPS  |    TIMEOUT | 0        | 关闭 DGPS 定位                                                                                |
|           |          |            |   1-1800 | 数据最大龄期（不同产品的默认值不 同，详见[表 4-9](#_bookmark45)），单位：秒，仅支持整数输入。 |

表 4-9 DGPS TIMEOUT 默认配置

| 产品型号              | 默认配置 |
|-----------------------|----------|
| UM982；UMD982         | 600 s    |
| UM980；UMD980         | 300 s    |
| UM960；UMD960；UM960L | 300 s    |
| UB9A0；UBD9A0         | 300 s    |

### RTK 引擎配置

该指令配置 RTK 引擎，配置 RTK 工作模式，或清除 RTK 参数。

命令格式：

CONFIG RTK [参数]

CONFIG RTK RELIABILITY [参数 1] [参数 2]

命令示例：

CONFIG RTK TIMEOUT 60 CONFIG RTK RELIABILITY 3 1

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-10 配置 RTK 模块指令

| 指令头               | 功能名称          | 参数           | 参数描述                                                                                                     |                                                                      |
|----------------------|-------------------|----------------|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
|               CONFIG |               RTK |    TIMEOUT     | 0                                                                                                            | 关闭 RTK 功能                                                        |
|                      |                   |                |   1-1800                                                                                                     | 数据最大龄期\*，单位为秒。无 Standalone 授权版本最 大可设置到 600s。 |
|                      |                   |    RELIABILITY | RTK 引擎可靠性门限配置： 1：可靠性要求宽松 2：可靠性要求一般 3：可靠性要求较严（默认状态） 4：可靠性要求严格 |                                                                      |
|                      |                   | USER_DEFAULTS  | 默认状态                                                                                                     |                                                                      |
|                      |                   |  CN0THD        | 0：CN0 有效性要求一般 1：CN0 有效性要求严格                                                                  |                                                                      |
|                      |                   |  MMPL          | 0：多路径抑制要求一般 1：多路径抑制要求严格                                                                  |                                                                      |
|                      |                   | RESET          | 重置 RTK 解算                                                                                                |                                                                      |
|                      |                   | DISABLE        | 不计算 RTK 结果，包括浮点解和固定解                                                                          |                                                                      |

\* UM982/UMD982 RTK TIMEOUT 默认值为 600s；UM980/UMD980 默认值为 120s。

表 4-11 RELIABILITY 可靠性门限配置参数

| 指令头    | 功能名称          | 指令参数                        | 参数描述                                                                            |
|-----------|-------------------|---------------------------------|-------------------------------------------------------------------------------------|
|    CONFIG |   RTK RELIABILITY |  参数 1：RTK 定位引擎可靠性门限 | 1：可靠性要求宽松 2：可靠性要求一般 3：可靠性要求较严（默认状态） 4：可靠性要求严格 |

| 指令头 | 功能名称 | 指令参数                 | 参数描述                                                                            |
|--------|----------|--------------------------|-------------------------------------------------------------------------------------|
|        |          |   参数 2：ADR 可靠性门限 | 1：可靠性要求宽松（默认状态） 2：可靠性要求一般 3：可靠性要求较严 4：可靠性要求严格 |

### STANDALONE 配置

本指令用于设定接收机 STANDALONE 的功能，STANDALONE 模式下接收机在没有接收到差分改正数时仍能进行一段时间的厘米级定位。

该模式推荐在开阔环境下使用，推荐将 PVT 解算引擎配置为 MULTI，即 CONFIG PVTALG MULTI，以提高定位精度。在某些场景下也可以通过 MASK 低仰角卫星减少多路径效应对模组的影响，以提高定位精度。

命令格式：

CONFIG STANDALONE [功能参数] [参数 1] [参数 2] [参数 3]

命令示例：

CONFIG STANDALONE ENABLE 40.113452 114.212234 57.23 CONFIG STANDALONE DISABLE

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

表 4-12 STANDALONE 参数

| 指令头                 | 功能名称                   | 功能参数         | 参数 1                                                                                            | 参数 2                                                                                              | 参数 3                                                                                  |
|------------------------|----------------------------|------------------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
|                 CONFIG |                 STANDALONE |        ENABLE    | param1 是输入的坐标参 数：-90≤ param1≤90为大地坐标系下的纬度坐标，以度为单位（输入有效 位 11 位） | param2 是输入的坐标参数：-180≤ param2≤180为大地坐标系下的经度坐 标，以度为单 位（输入有效位 11 位） | param3 是输入的坐标参 数：-30000≤ param3≤ 18000 为海拔高，以米为单位（输入有效位 6 位） |
|                        |                            |   ENABLE         | 时间参数，用于配置自动进入 STANDALONE 模式的等待时间。3≤param1≤100，单位 s，默认 100s             |                                                                                                     |                                                                                         |
|                        |                            |  ENABLE          | 为空时，为默认模式，使用接收机解算出的位置作 为初值，默认 100s 后进入 STANDALONE 模式             |                                                                                                     |                                                                                         |
|                        |                            | DISABLE （默认） |                                                                                                   |                                                                                                     |                                                                                         |
|                        |                            |   TIMEOUT\*      | 时间参数，用于配置 STANDALONE 模式的持续时 间。范围：1800 ≤param1 ≤86400，单位 s，默认 86400 s    |                                                                                                     |                                                                                         |

\* 目前单北斗产品暂不支持 TIMEOUT 配置

### HEADING 引擎配置

本指令用于设置支持单板卡（模块）双天线定向的接收机。设置 Heading 定向的基线长度固定、基线长度变化、低动态方式。单板卡（模块）双天线定向的接收机默认开机进行 Heading 工作。原理示意图如[图3-1 定向原理结构图](#_bookmark29)。

命令格式：

CONFIG HEADING [参数]

CONFIG HEADING LENGTH [参数 1 (可选)] [参数 2 (可选)]

命令示例：

CONFIG HEADING FIXLENGTH CONFIG HEADING VARIABLELENGTH CONFIG HEADING STATIC

CONFIG HEADING LOWDYNAMIC

适用产品：UM982、UMD982

表 4-13 Heading 引擎配置参数

| 指令头             | 功能名称            | 指令参数         | 参数描述                                                                                             |
|--------------------|---------------------|------------------|------------------------------------------------------------------------------------------------------|
|             CONFIG |             HEADING |    FIXLENGTH     | 双天线接收机的主天线（ANT1）与从天线（ ANT2 ） 之间距离保持固定，两天线可同步运动或静止（默认 模式） |
|                    |                     |   VARIABLELENGTH | 双天线接收机的主天线（ANT1）与 从天线（ANT2）的相对位置、距离实时动态变化                            |
|                    |                     |  STATIC          | 双天线接收机的主天线（ANT1）与 从天线（ANT2）均在静止状态                                            |
|                    |                     |  LOWDYNAMIC      | 低动态，对打桩机类低速运动载体可 启用                                                                |
|                    |                     |   TRACTOR        | 双天线接收机的主天线（ANT1）与 从天线（ANT2）之间的距离缓慢变化，类似于拖拉机的作业速度              |

| 指令头 | 功能名称 | 指令参数    | 参数描述                                                          |
|--------|----------|-------------|-------------------------------------------------------------------|
|        |          |             | 用于配置双天线基线长度， 用来对                                   |
|        |          |  LENGTH     | Heading 解算的结果进行约束，适用 于已知基线长度的场景，详细参见下 |
|        |          |             | 表                                                                |
|        |          |             | Heading 引擎可靠性门限配置：                                      |
|        |          |             | 1：可靠性要求宽松                                                 |
|        |          | RELIABILITY | 2：可靠性要求一般                                                 |
|        |          |             | 3：可靠性要求较严（默认状态）                                     |
|        |          |             | 4：可靠性要求严格                                                 |

表 4-14 HEADING LENGTH 配置参数

| 指令头   | 功能名称        | 参数 1                                                 | 参数 2                                                   |
|----------|-----------------|--------------------------------------------------------|----------------------------------------------------------|
|   CONFIG |  HEADING LENGTH | 固定基线的长度，单位： cm。如基线长度 20cm，则 输入 20 | 能够忍受的误差范围，单位： cm。如误差范围 3cm，则输 入 3 |

注：若用户不配置参数 1、参数 2，则系统采用默认配置进行约束。

### HEADING 航向和俯仰偏移量配置

本指令用于设置航向角和俯仰角的偏移量，该偏移量将修正接收机输出的 HEADING、 GPTHS、Heading2 信息中的航向角和俯仰角。

命令格式：

CONFIG HEADING OFFSET [Headingoffset Pitchoffset]

命令示例：

CONFIG HEADING OFFSET 90 45

适用产品：UM982、UMD982、UM980、UMD980、UB9A0、 UBD9A0

表 4-15 Heading 航向和俯仰偏移量配置参数

| 指令头    | 功能名称         | 指令参数       | 参数描述                                    |
|-----------|------------------|----------------|---------------------------------------------|
|    CONFIG |   HEADING OFFSET |  Headingoffset | 航向角改正值，deg. 取值范围：-180.0 \~180.0 |
|           |                  |  Pitchoffset   | 俯仰角改正值，deg. 取值范围：-90.0 \~ 90.0  |

### SBAS 配置

该指令配置 SBAS 功能开启和关闭，SBAS 功能配置支持自主选择 SBAS 改正数系统

（AUTO 模式），也支持指定改正数系统，在使用的过程中，若了解使用地区的改正数系统的运行情况，建议指定改正数系统配置。

命令格式：

CONFIG SBAS [参数 1] [参数 2]

命令示例：

CONFIG SBAS ENABLE WAAS CONFIG SBAS TIMEOUT 600

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

表 4-16 配置 SBAS 指令

| 指令头      | 功能名称  | 参数 1     | 参数 2 | 参数描述                    |
|-------------|-----------|------------|--------|-----------------------------|
|      CONFIG |      SBAS | ENABLE     | Auto   | SBAS 自动选择改正数系统模式 |
|             |           |     ENABLE | WAAS   | 单独使能 WAAS 改正数功能    |
|             |           |            | GAGAN  | 单独使能 GAGAN 改正数功能   |
|             |           |            | MSAS   | 单独使能 MSAS 改正数功能    |
|             |           |            | EGNOS  | 单独使能 EGNOS 改正数功能   |
|             |           |            | SDCM   | 单独使能 SDCM 改正数功能    |
|             |           |            | ASECNA | 单独使能 ASECNA 改正数功能  |

| 指令头 | 功能名称 | 参数 1      | 参数 2 | 参数描述                                                                                  |
|--------|----------|-------------|--------|-------------------------------------------------------------------------------------------|
|        |          |             | KASS   | 单独使能 KASS 改正数功能                                                                  |
|        |          |             | SPAN   | 单独使能 SPAN 改正数功能                                                                  |
|        |          |             | BDS    | 单独使能 BDS SBAS 改正数功能                                                              |
|        |          |             | SLAS3  | 单独使能 QZSS SLAS 改正数功能                                                             |
|        |          | DISABLE     | -      | 关闭 SBAS 功能（默认）                                                                    |
|        |          |   TIMEOUT\* |   t    | SBAS timeout 时间配置， 范围： 120\~1800s，默认为 1200s； 若配置为 0 时，则等同于 DISABLE |

\* TIMEOUT 参数配置：UM982 Build9669 及之后的版本支持

### EVENT 功能配置

该指令配置 EVENT 功能及相关参数。EVENT 功能默认为关闭状态。

命令格式：

CONFIG EVENT [参数 1] [参数 2] [参数 3]

命令示例：

CONFIG EVENT ENABLE POSITIVE 10

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

3 SLAS 仅 UM980、UM982、UB9A0 支持

表 4-17 配置 EVENT 模块指令

| 指令头 | 功能名称 | 参数 1                      | 参数 2         | 参数 3                                                                     |
|--------|----------|-----------------------------|----------------|----------------------------------------------------------------------------|
|        |          | DISABLE                     |                |                                                                            |
|        |          | （关闭 EVENT 功             |                |                                                                            |
|        |          | 能，默认状态）              |                |                                                                            |
|        |          |                             |                | TGUARD                                                                     |
|        |          |                             | POSITIVE       | （两个有效脉冲之间的                                                       |
| CONFIG | EVENT    |  ENABLE （开启 EVENT 功能） | （上升沿有效） | 最短时间要求,单位 ms。若小于 TGuard， 则第二个 Event 被忽视。默认值：4，最 |
|        |          |                             |   NEGATIVE     |                                                                            |
|        |          |                             | （下降沿有效） | 小：2，最大：                                                              |
|        |          |                             |                | 3,599,999）                                                                |

### EVENT2 功能配置

该指令配置 EVENT2 功能及相关参数。EVENT2 功能默认为关闭状态。

命令格式：

CONFIG EVENT2 [参数 1] [参数 2] [参数 3]

命令示例：

CONFIG EVENT2 ENABLE POSITIVE 10

适用产品：UM982、UMD982

表 4-18 配置 EVENT2 模块指令

| 指令头 | 功能名称 | 参数 1                       | 参数 2         | 参数 3                                                                     |
|--------|----------|------------------------------|----------------|----------------------------------------------------------------------------|
|        |          | DISABLE                      |                |                                                                            |
|        |          | （关闭 EVENT2 功             |                |                                                                            |
|        |          | 能，默认状态）               |                |                                                                            |
|        |          |                              |                | TGUARD                                                                     |
|        |          |                              | POSITIVE       | （两个有效脉冲之间的                                                       |
| CONFIG | EVENT2   |  ENABLE （开启 EVENT2 功能） | （上升沿有效） | 最短时间要求,单位 ms。若小于 TGuard，则第二个 Event 被忽 视。默认值：4，最 |
|        |          |                              |   NEGATIVE     |                                                                            |
|        |          |                              | （下降沿有效） | 小：2，最大：                                                              |
|        |          |                              |                | 3,599,999）                                                                |

### SMOOTH 功能配置

该指令配置 RTK 解算结果、Heading 解算结果以及 SPPNAV 中的多普勒速度的 SMOOTH 功能及相关参数。SMOOTH 功能默认为关闭状态。

命令格式：

CONFIG SMOOTH [解算引擎] [参数]

命令示例：

CONFIG SMOOTH RTKHEIGHT 10 CONFIG SMOOTH HEADING 10 CONFIG SMOOTH PSRVEL ENABLE

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-19 配置 SMOOTH 功能指令

| 指令头       | 功能名称     | 解算引擎   | 参数      | 参数描述                          |
|--------------|--------------|------------|-----------|-----------------------------------|
|       CONFIG |       SMOOTH |  RTKHEIGHT |  时间长度 | 单位：epoch，取值范围 0\~100      |
|              |              |  HEADING   |  时间长度 | 单位：epoch，取值范围 0\~100      |
|              |              |   PSRVEL   |  ENABLE   | SPPNAV 中的多普勒速度 smooth 使能 |
|              |              |            |  DISABLE  | SPPNAV 中的多普勒速度 smooth 关闭 |

### MMP 多路径抑制配置

该指令用于使能 GNSS 模块输出的原始观测量的伪距多路径抑制功能，默认为关闭状态。

命令格式：

CONFIG MMP [参数]

命令示例：

CONFIG MMP ENABLE

适用产品：UM980、UMD980、UB9A0、UBD9A0

表 4-20 配置 MMP 指令

| 指令头    | 功能名称 | 参数     | 参数描述                                                  |
|-----------|----------|----------|-----------------------------------------------------------|
|    CONFIG |    MMP   |  ENABLE  | 开启模块输出的原始观测量的伪距多 路径抑制功能             |
|           |          |  DISABLE | 关闭模块输出的原始观测量的伪距多 路径抑制功能（默认状态） |

### NMEA 协议版本配置

该指令用于配置输出的NMEA 数据协议版本。默认状态下，NMEA 协议版本为 V410。

命令格式：

CONFIG NMEA0183 [参数]

命令示例：

CONFIG NMEA0183 V410

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-21 配置 NMEA0183 版本指令

| 指令头    | 功能名称   | 参数  | 参数描述                                           |
|-----------|------------|-------|----------------------------------------------------|
|    CONFIG |   NMEA0183 |  V410 | 配置NMEA 协议版本 V4104（扩展支 持北斗）           |
|           |            |  V411 | 配置 NMEA 协议版本 V411（详见 NMEA V411 官方协议） |

### RTCMB1CB2a 版本配置

该指令用于配置是否将 BDS 系统卫星的 B1C&B2a 信号编入 RTCM 协议。此配置默认状态为 ENABLE 状态。

命令格式：

CONFIG RTCMB1CB2a [参数]

命令示例：

CONFIG RTCMB1CB2a ENABLE

4 参数 V410 中的“0”不可省略

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

表 4-22 配置 RTCMB1CB2a 功能指令

| 指令头  | 功能名称    | 参数    | 参数描述                         |
|---------|-------------|---------|----------------------------------|
|  CONFIG |  RTCMB1CB2a | ENABLE  | 将 B1C&B2a 信号编入 RTCM（默认） |
|         |             | DISABLE | 不将 B1C&B2a 信号编入 RTCM       |

### RTCMPHASERATE 载波相位变化配置

该指令用于配置 RTCM 编码中载波相位变化的数值符号的正负。

命令格式：

CONFIG RTCMPHASERATE [参数]

命令示例：

CONFIG RTCMPHASERATE POSITIVE

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

-   UM982 Build9669 及之后的版本支持

表 4-23 配置 RTCMPHASERATE 功能指令

| 指令头    | 功能名称         | 参数      | 参数描述                                          |
|-----------|------------------|-----------|---------------------------------------------------|
|    CONFIG |    RTCMPHASERATE |  POSITIVE | 与 RTCM 编码的载波相位变化的数值 符号相同（默认） |
|           |                  |  NEGATIVE | 与 RTCM 编码的载波相位变化的数值 符号相反         |

### RTCMCLOCKOFFSET RTCM 数据钟差补偿配置

该指令用于配置接收机输出 RTCM 原始数据时是否对原始数据进行钟差补偿，默认模式下该指令为ENABLE 状态，会进行钟差补偿后输出。

命令格式：

CONFIG RTCMCLOCKOFFSET [参数]

命令示例：

CONFIG RTCMCLOCKOFFSET DISABLE

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

表 4-24 配置 RTCMCLOCKOFFSET 功能指令

| 指令头  | 功能名称         | 参数    | 参数描述             |
|---------|------------------|---------|----------------------|
|  CONFIG |  RTCMCLOCKOFFSET | ENABLE  | 功能使能（默认状态） |
|         |                  | DISABLE | 功能关闭             |

### PSRVELDRPOS 多普勒位置预测

该指令用于使能接收机多普勒位置预测功能。多普勒位置预测功能默认为使能状态，该功能开启后，接收机会在伪距观测值质量较差、但多普勒解算成功且质量较好时，利用实时更新的多普勒速度进行下一个位置点的预测，此时，在 GGA 中的定位结果仍然会显示为 1，但是参与定位的卫星数量会标为 0。

命令格式：

CONFIG PSRVELDRPOS [参数]

命令示例：

CONFIG PSRVELDRPOS ENABLE //使能多普勒位置预测功能 CONFIG PSRVELDRPOS DISABLE //关闭多普勒位置预测功能

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

表 4-25 配置 PSRVELDRPOS 功能指令

| 指令头  | 功能名称     | 参数    | 参数描述             |
|---------|--------------|---------|----------------------|
|  CONFIG |  PSRVELDRPOS | ENABLE  | 功能使能（默认状态） |
|         |              | DISABLE | 关闭                 |

### AGNSS 辅助定位配置

该指令用于使能接收机的辅助定位功能，辅助定位功能开启后，在接收到 GNSS 辅助信息时，如卫星星历、时间等，可以加快接收机的首次定位时间。功能开启后，在接收到有效辅助数据后首次定位时间\<5s。

命令格式：

CONFIG AGNSS [参数]

命令示例：

CONFIG AGNSS ENABLE

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

-   UM980 Build7923 及之后的版本支持；
-   UM982 Build7650 及之后的版本支持。

表 4-26 配置 AGNSS 功能指令

| 指令头  | 功能名称 | 参数     | 参数描述                             |
|---------|----------|----------|--------------------------------------|
|  CONFIG |  AGNSS   | ENABLE   | 开启 AGNSS 辅助定位功能              |
|         |          |  DISABLE | 关闭 AGNSS 辅助定位功能 （默认配置） |

### PPP 配置

该指令用于配置接收机的 PPP 定位相关功能配置，在特定版本上支持。

命令格式：

CONFIG PPP [参数 1] [参数 2]

CONFIG PPP CONVERGE [参数 1] [参数 2]

命令示例：

CONFIG PPP ENABLE B2b-PPP CONFIG PPP DISABLE

CONFIG PPP CONVERGE 10 20

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

-   UM980 Build7923 及之后的版本支持；
-   UM982 Build7650 及之后的版本支持。

表 4-27 配置 PPP 功能指令

| 指令头              | 功能名称         | 参数 1     | 参数 2                                                                     | 参数描述                           |
|---------------------|------------------|------------|----------------------------------------------------------------------------|------------------------------------|
|              CONFIG |              PPP |     ENABLE | B2b-PPP\*                                                                  | B2b PPP 功能                       |
|                     |                  |            | E6-HAS\*                                                                   | E6 HAS 功能                        |
|                     |                  |            |  AUTO                                                                      | 根据场景自动选择合适的 PPP 改正数  |
|                     |                  |            | SSR-RX                                                                     | RXN PPP SSR 服务                   |
|                     |                  |            | L6MDCPPP\*                                                                 | QZSS L6E (MADOCA) PPP 服务         |
|                     |                  |   DATUM    | WGS84                                                                      | 参考坐标系基准 WGS84 坐标系        |
|                     |                  |            |  PPPORIGINAL                                                               | 与 PPP 服务采用坐标系一致 （默认） |
|                     |                  |   TIMEOUT  | 取值范围 90\~180s，默认为 120s，当配置 TIMEOUT 为 0 时，PPP 解算功能关闭。 |                                    |
|                     |                  |  CONVERGE  | PPP 定位精度收敛阈值，详细参 见下表                                        |                                    |
|                     |                  | DISABLE    | 关闭 PPP 功能（默认）                                                      |                                    |

表 4-28 PPP CONVERGE 配置参数

| 指令头  | 功能名称      | 参数 1                        | 参数 2                        |
|---------|---------------|-------------------------------|-------------------------------|
|  CONFIG |  PPP CONVERGE | HorSTD 水平误差阈值5，单位 cm | VerSTD 高程误差阈值6，单位 cm |

-   B2b-PPP 功能仅在 UM980 Build7923 及之后的版本 SIGNALGROUP 2 模式下支持；
-   B2b-PPP 功能仅在 UM982 Build7650 及之后的版本 SIGNALGROUP 3 6 模式支持；
-   E6-HAS 功能在 UM980 Build11833 及之后的版本支持；在 UM982 Build11826 及之后的版本支持。
-   L6MDCPPP 功能在UM980 Build16606 及之后的版本支持。

### ANTIJAM 抗干扰设置

该指令用于设置接收机的抗干扰模式，ANTIJAM 指令替换原 JAMMING 指令。命令格式：

CONFIG ANTIJAM [mode]

命令示例：

CONFIG ANTIJAM DISABLE CONFIG ANTIJAM AUTO CONFIG ANTIJAM FORCE

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0

-   UM980 Build10110 及之后的版本支持；

表 4-29 抗干扰功能配置的指令说明

| 指令头 | 功能名称 | 参数    | 参数描述       |
|--------|----------|---------|----------------|
| CONFIG |          | DISABLE | 关闭抗干扰功能 |

5, [6](#_bookmark81) 水平误差阈值推荐大于 10cm；高程误差阈值推荐大于 15cm

| 指令头 | 功能名称  | 参数   | 参数描述                                    |
|--------|-----------|--------|---------------------------------------------|
|        |   ANTIJAM | AUTO   | 自适应模式（默认）                          |
|        |           |  FORCE | 强制抗干扰模式，模式开启后模组功耗 会提高。 |

### SIGNALGROUP 跟踪通道模式配置

该指令用于选择接收机主从天线跟踪频点的不同组合配置，参数 1 代表主天线的频点

组合，参数 2 代表从天线的频点组合。

主天线默认支持 SBAS L1C/A 频点解算，从天线不支持 SBAS。

单天线产品仅支持参数 1 配置，配置参数 2 时系统会报错，并给出提示不支持该参数。

双天线产品可对参数 1 和参数 2 进行配置；当参数 2 不被配置时，默认配置为 0。

参数 1 和参数 2 的配置方法参见下文。

命令配置后，若与被配置模块的当前配置不相同，模块会自动重启，实施新配置方案。此命令配置后会自动保存，不需要使用 Saveconfig 命令进行保存。

因此若对模块进行多个 CONFIG 配置，且配置中包含 SIGNALGROUP 配置，应确保其他配置被模组保存，避免因配置了 SIGNALGROUP 使得模组重启，导致其他配置指令未被模组保存。

命令格式：

CONFIG SIGNALGROUP [参数 1] [参数 2]

命令示例：

CONFIG SIGNALGROUP 1

CONFIG SIGNALGROUP 2 3

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

表 4-30 配置频点组合选择功能指令

| 指令头 | 功能名称    | 参数 1  | 参数 2  | 参数描述         |
|--------|-------------|---------|---------|------------------|
| CONFIG | SIGNALGROUP | TypeNum | TypeNum | TypeNum 详见下表 |

表 4-31 频点组合表

| TypeNum | 频点组合详细说明                                                                                                                             |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | 关闭从天线                                                                                                                                   |
|     1   | BDS：B1I、B2I、B3I、B1C、B2a、B2b GPS：L1C/A、L2C/L2P、L5 GLO：G1、G2 GAL：E1、E5a、E5b QZSS：L1C/A、L2C、L5                                 |
|     2   | BDS：B1I、B2I、B3I、B1C、B2a、B2b GPS：L1C/A、L1C、L2C、L2P(Y)、L5 GLO：G1、G2、G3 GAL：E1、E5a、E5b、E6 QZSS：L1C/A、L1C、L2C、L5 NavIC：L5 |
|     3   | BDS：B1I、B3I、B1C、B2b-PPP GPS：L1C/A、L2C/L2P、L5 GLO：G1、G2 GAL：E1、E5a、E5b、E6 QZSS：L1C/A、L2C、L5                                   |
|     4   | BDS：B1I、B2I、B3I GPS：L1C/A、L2C/L2P、L5 GLO：G1、G2 GAL：E1、E5a、E5b QZSS：L1C/A、L2C、L5                                                |

| TypeNum | 频点组合详细说明                                                                                                       |
|---------|------------------------------------------------------------------------------------------------------------------------|
|     5   | BDS：B1I、B2I、B3I GPS：L1C/A、L2C/L2P GLO：G1、G2 GAL：E1、E5b QZSS：L1C/A、L2C                                       |
|     6   | BDS：B1I、B3I GPS：L1C/A、L2C/L2P GLO：G1、G2 GAL：E1、E5b QZSS：L1C/A、L2C                                            |
|    7    | BDS：B1I、B2I、B3I、B1C、B2a、B2b GPS：L1C/A、L2C/L2P、L5 GLO：G1、G2 GAL：E1、E5a、E5b QZSS：L1C/A、L2C、L5           |
|   8     | GPS：L1C/A、L2C/L2P、L5； BDS：B1I、B3I、B1C、B2a； GAL：E1、E5a、E5b；                                                |
|     9   | BDS: B1I、B2I、B3I、B1C、B2a、B2b GPS: L1C/A、L2P(Y)/L2C、L5 GLO: L1C/A、L2C/A GAL: E1C、E5A、E5B QZSS: L1C/A、L2C、L5 |

| TypeNum | 频点组合详细说明                                                                                                  |
|---------|-------------------------------------------------------------------------------------------------------------------|
|     10  | BDS：B1I、B2I 、B3I、B1C、B2a、B2b GPS：L1C/A、L2C/L2P、L5 GLO：G1、G2 GAL：E1、E5a、E5b QZSS：L1C/A、L2C、L5、L6 |

表 4-32 产品默认频点组合及支持的配置

| 产品 型号 | 默认 TypeNum 配置 | 支持的 TypeNum 配置 |  备注                 |        |                  |
|-----------|-------------------|---------------------|-----------------------|--------|------------------|
|           | 主天线            | 从天线              | 主天线                | 从天线 |                  |
|   UM982   |   4               |   5                 | 4                     | 5      |                  |
|           |                   |                     | 3                     | 6      |                  |
|           |                   |                     | 5                     | 0      | 低功耗模式       |
|           |                   |                     | 7                     | 0      | 仅用于基准站模式 |
|   UM980   |   1               | 1                   |                       |        |                  |
|           |                   | 2                   |                       |        |                  |
|           |                   | 8\*                 | 该模式下支持最高 50Hz |        |                  |
|           |                   | 10                  |                       |        |                  |
|  UB9A0    |  2                | 2                   |                       |        |                  |
|           |                   | 9                   | 该模式下支持最高 50Hz |        |                  |

-   对于单北斗产品（UMD982、UMD980、UBD9A0），接收机跟踪北斗全频，即 B1I、 B2I、B3I、B1C、B2a、B2b。
-   UM980 SIGNALGROUP 8 模式下支持最高 50Hz 定位、测速及 50Hz RAWDATA（RTCM

    格式）的数据输出。

-   UM982 SIGNALGROUP 3 6 模式下在 Build10979 之后在特定 log 请求下可支持 20Hz 定位数据更新。

### ANTENNADELTAHEN 天线高信息

该指令用来设置接收机作为基准站时，天线相对于地面标识点的高度（天线高）和平面偏移信息，这些信息将影响 RTCM1006 差分电文中有关天线的描述。

命令格式：

CONFIG ANTENNADELTAHEN [height] [east] [north]

命令示例：

CONFIG ANTENNADELTAHEN 1.521 0.0 0.0

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-33 配置天线高信息配置的功能指令

| 指令头           | 功能名称                  | 参数      | 值                 | 参数描述                                                                           |
|------------------|---------------------------|-----------|--------------------|------------------------------------------------------------------------------------|
|           CONFIG |           ANTENNADELTAHEN |    Height |    0.0000-6.5535   | 从地面点标识中心到天线参考点（ ARP ） 的垂直距离（天线高），单 位 m，默认为 0.0000 |
|                  |                           |    East   |    0.0000-100.0000 | 从地面点标识中心到天线参考点（ ARP ） 的东向偏差，单位 m，默认 为 0.0000           |
|                  |                           |    North  |    0.0000-100.0000 | 从地面点标识中心到天线参考点（ ARP ） 的北向偏差，单位 m，默认 为 0.0000           |

### AUTHCODE 增加授权码

该指令用于为接收机添加授权码。一旦使用该指令输入正确的授权码后，接收机将会自动保存授权信息，并重启。接收机内保存的授权信息无法用更新固件或 FRESET 命令擦除，输入错误的授权码会导致接收机无法正常工作。

命令格式：

CONFIG AUTHCODE [string]

命令示例：

Config AUTHCODE 0x000000bf:080101007502:961101144100099:E9CC4A711D000 001:556fb037:696CC7AE564AAC66AA92AA8116D26CE71E15692D581B2CA308C5D90E4 FDC2DBE6FBDB48942BF0DF7CAF1271DBA54D7123D73585EA4E8FA496C847E184D126 C5607A2050E696812D9EB05015B4A0630531380CE34A893F49F1192984BD279AC9FB0 9EB0EAEACA71F0108B56302F9120DC2BBA5394A969B31A5959AB1F25DE0416

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

表 4-34 配置接收机授权码的功能指令

| 指令头 | 功能名称 | 参数   | 参数描述     |
|--------|----------|--------|--------------|
| CONFIG | AUTHCODE | string | 授权码字符串 |

### ALGRESET 算法引擎的复位操作

该指令用于对各 ALG 模块进行复位操作。

命令格式：

CONFIG ALGRESET [type]

命令示例：

CONFIG ALGRESET HEADING

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

表 4-35 ALGRESET 指令参数

| 指令头        | 功能名称        | 参数     | 参数描述                                                                          |
|---------------|-----------------|----------|-----------------------------------------------------------------------------------|
|        CONFIG |        ALGRESET | RTK1     | 复位主天线 RTK 计算引擎                                                           |
|               |                 |  RTK2    | 复位从天线 RTK 计算引擎，仅 UM982 或 UMD982 产品支持                              |
|               |                 |  HEADING | 复位 HEADING 计算引擎，仅 UM982 或 UMD982 产品支持                                |
|               |                 |   PPP    | 复位主天线 PPP 计算引擎，仅 UM982、UMD982、UM980、 UMD980、UB9A0、UBD9A0 产品支持 |
|               |                 | ADR      | 复位主从天线 ADR 计算引擎                                                         |

### IONMODE 电离层模型配置

该指令用于配置接收机当前采用的电离层模型。

命令格式：

CONFIG IONMODE [type]

命令示例：

CONFIG IONMODE GPSK8

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

-   UM982 Build9669 及之后的版本支持
-   UM980 Build10110 及之后的版本支持

表 4-36 IONMODE 指令参数

| 指令头  | 功能名称 | 参数  | 参数描述                                    |
|---------|----------|-------|---------------------------------------------|
|  CONFIG |  IONMODE | GPSK8 | GPS 电离层模型（多系统产品的默认配置）      |
|         |          | BD2K8 | 北斗 2 代电离层模型（单北斗产品的默认配置） |

| 指令头 | 功能名称 | 参数      | 参数描述                        |
|--------|----------|-----------|---------------------------------|
|        |          | BD3GIM\*  | 北斗 3 代电离层模型（暂不支持） |
|        |          | GALNTCM\* | Galileo 电离层模型（暂不支持）  |

### BASEANTENNAMODEL 基准站天线信息

该指令用来设置接收机作为基准站时，天线的 ID、名称、型号和相位中心偏差信息

（ 当前仅支持字段 1-5 ）， 这些信息将影响 RTCM1005 、RTCM1006 、RTCM1007 、 RTCM1033 差分电文中有关天线的描述。

指令中天线相位中心偏差和随高度角变化的数值均参考 NGS 给出的天线相位中心参数定义。

由于 RTCM v3.2 中天线命名采用 IGS 的标准，为了处理 IGS 天线名称中的空格，在使用该命令设置含有空格的天线名称时，需使用 “ ” 输入天线名称，例如，对于华信 HX- CGX601A 天线，IGS 规定的名称为：HXCCGX601A HXCS，在命令中需输入 “HXCCGX601A HXCS"。

命令格式：

CONFIG BASEANTENNAMODEL [name] [SN] [setupID] [type]

命令示例：

CONFIG BASEANTENNAMODEL "HXCCGX601A HXCS" 62815 1 USER

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 4-37 BASEANTENNAMODEL 指令参数

| 指令头   | 功能名称           | 参数   | ASCII 值 | 参数描述                                                    |
|----------|--------------------|--------|----------|-------------------------------------------------------------|
|   CONFIG |   BASEANTENNAMODEL |   name |   String | 天线名称，最长 31 个 ASCII 字 符 ， 默 认 为 ADVNULLANTENNA |

| 指令头 | 功能名称 | 参数     | ASCII 值    | 参数描述                                        |
|--------|----------|----------|-------------|-------------------------------------------------|
|        |          |   SN     |   String    | 天线序列号，最长 31 个 ASCII 字符，默认为 a0001 |
|        |          |  setupID |  0-255      | 天线识别号，0-255 的 整数，默认为 0             |
|        |          |  type    | NO，或 USER |  天线型号，默认为 NO                            |

### PVTALG PVT 解算引擎配置

该指令用于配置接收机 PVT 解算引擎。

命令格式：

CONFIG PVTALG [参数 1]

命令示例：

CONFIG PVTALG MULTI

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

表 4-38 PVTALG 指令参数

| 指令头   | 功能名称 | 参数 1 | 参数描述        |
|----------|----------|--------|-----------------|
|   CONFIG |   PVTALG | SINGLE | 单频解算        |
|          |          | AUTO   | 单频和 ION 估计 |
|          |          | MULTI  | 双频解算        |

注：UM980/UMD980/UB9A0/UBD9A0 默认为 AUTO 模式，UM982/UMD982 默认为 SINGLE 模式。

### PSRPOSBIAS PSRPOS 偏差补偿配置

该指令用于开启或关闭接收机的 PSRPOS 偏差补偿，补偿伪距定位和 RTK 定位的固有偏差。

命令格式：

CONFIG PSRPOSBIAS [参数 1]

命令示例：

CONFIG PSRPOSBIAS ENABLE

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

表 4-39 PSRPOSBIAS 指令参数

| 指令头  | 功能名称    | 参数 1          | 备注                 |
|---------|-------------|-----------------|----------------------|
|  CONFIG |  PSRPOSBIAS | ENABLE          | 启用 PSRPOS 偏差补偿 |
|         |             | DISABLE（默认） | 关闭 PSRPOS 偏差补偿 |

### 网络IP 地址配置

网络设备 ETH1 是接收机网络接口。配置网络指令以 CONFIG 为指令头，指令头后是网络设备及网络设备属性，用于设置网络的 IPv4 地址。高精度 GNSS 接收机支持 1 个网络设备：ETH1。

命令格式：

CONFIG ETH1 [参数]

命令示例：

CONFIG ETH1 DHCP

CONFIG ETH1 192.168.0.100 192.168.0.1 255.255.255.0 192.168.0.1

适用产品：UB9A0、UBD9A0

表 4-40 网络 IP 地址配置参数列表

| 指令头 | 功能名称 | 参数列表 | 参数描述               |
|--------|----------|----------|------------------------|
| CONFIG | ETH1     | DHCP     | 使用 DHCP 模式获取配置 |

| 指令头 | 功能名称 | 参数列表    | 参数描述                                                                                               |
|--------|----------|-------------|--------------------------------------------------------------------------------------------------------|
|        |          |   IPv4 列表 | IP GateWay NetMask DNS_Server 使用 ASCII 字符“空格”作为分割符号 本机 IP IP 网关 IP 网络掩码 DNS 服务器 |

### 网络端口号配置

网络串口是接收机输入和输出数据的接口。配置串口指令以 CONFIG 为指令头，指令头后是网络串口的设备及网络串口属性，用于设置网络串口的端口号或者服务端的 IP 和端口号等。

高精度 GNSS 接收机支持 3 个网络串口，分别是 icom1，icom2，icom3。接收机三个串口功能相同，但各网络串口数据输入输出以各自配置进行独立工作。

命令格式：

CONFIG [网络串口设备号] [串口属性参数]

命令示例：

CONFIG ICOM1 TCP 30001

CONFIG ICOM1 TCP 192.168.0.2 30001

适用产品：UB9A0、UBD9A0

表 4-41 网络端口号配置参数列表

| 指令头     | 串口列表          | 串口参数 | 参数描述                                                                      |
|------------|-------------------|----------|-------------------------------------------------------------------------------|
|     CONFIG | ICOM1 ICOM2 ICOM3 |  Disable |  关闭接收机网络 TCP/IP client 连接服务器功能                                  |
|            | ICOM1 ICOM2 ICOM3 | 协议     | TCP 或者 UDP。缺省默认为 TCP 协议。                                           |
|            |                   |  IP      | 设置网络端口的服务端 IPv4 地址，如果缺省， 则网络端口为服务器模式（Server）。 |

| 指令头 | 串口列表 | 串口参数 | 参数描述                                                                                     |
|--------|----------|----------|----------------------------------------------------------------------------------------------|
|        |          |  端口号7 | 设置端口号。范围：1 \~ 65534 如果服务器模式，为本地（local）端口号否则，设置为服务端的端口号 |

### LOG 输出顺序配置

本条消息用于配置 LOG 的输出顺序。

命令格式：

CONFIG LOGSEQ [参数]

命令示例：

CONFIG LOGSEQ 1

CONFIG LOGSEQ 2

适用产品：UB9A0、UBD9A0

表 4-42 LOG 输出顺序配置参数列表

| 指令头   | 功能名称 | 参数 | 参数描述                                                  |
|----------|----------|------|-----------------------------------------------------------|
|   CONFIG |   LOGSEQ | 1    | 输出顺序为：位置信息、RTCM、OBSVM、EPHEM                  |
|          |          | 2    | 输出顺序为：RTCM、OBSVM、EPHEM、位置信息 （默认输出顺序） |

### Ntripserver 配置

Ntripserver 是接收机向 Ntripcaster 上传数据的专用设备，目前仅支持Ntrip 协议版本

V1。

高精度 GNSS 接收机支持 3 个Ntripserver，分别是 NCOM1，NCOM2，NCOM3。

7 端口号 40000 已被内部程序占用，不能配置

建议使用 30001/30002/30003，尽量避免使用 32768 以上端口

命令格式：

CONFIG [Ntrip Server 设备号] [属性参数]

命令示例：

CONFIG NCOM1 10.0.100.2 9000 UB9A0_RTCM32 SERV_PASSWORD

适用产品：UB9A0、UBD9A0

表 4-43 NtripServer 配置参数列表

| 指令头     | 串口设备           | 串口参数  | 参数描述                        |
|------------|--------------------|-----------|---------------------------------|
|     CONFIG | NCOM1 NCOM2 NCOM3  |  Disable  |  关闭 Ntripserver 功能          |
|            |  NCOM1 NCOM2 NCOM3 | Caster IP | Ntrip caster TCP IP v4 地址     |
|            |                    | port      | Ntrip caster TCP 端口号         |
|            |                    | mountport | Ntrip caster 挂载结点名称       |
|            |                    | password  | Ntrip caster 上传数据的访问密码 |

### Ntripclient 配置

Ntripclient 是接收机从 Ntrip caster 收取数据的专用设备，目前仅支持 Ntrip 协议版本

V1。

高精度 GNSS 接收机支持 1 个Ntrip Client: NCOM20。

命令格式：

CONFIG [Ntrip Client 设备号] [属性参数]

命令示例：

CONFIG NCOM20 10.0.100.2 9000 UB9A0_RTCM32 UNAME CLI_PASSWORD

适用产品：UB9A0、UBD9A0

表 4-44 Ntripclient 配置参数列表

| 指令头     | 串口设备  | 串口参数     | 参数描述                        |
|------------|-----------|--------------|---------------------------------|
|     CONFIG | NCOM20    | Disable      | 关闭 Ntripclient 功能           |
|            |    NCOM20 | Caster IP    | Ntrip caster IP v4 地址或者域名 |
|            |           | port         | Ntrip caster TCP 端口号         |
|            |           | mountport    | Ntrip caster 挂载结点名称       |
|            |           | uname        | Ntrip caster 下载数据的用户名称 |
|            |           | cli_password | Ntrip caster 下载数据的访问密码 |

### RTCM 数据过滤配置

当基站同时发送RTCM 3.0 和 3.2 系列数据时，该指令用于配置移动端优先解析 RTCM

3.2 数据，过滤掉RTCM 3.0 数据。

命令格式：

CONFIG RTCMDECAUTO [参数]

命令示例：

CONFIG RTCMDECAUTO ENABLE

适用产品：UM980、UMD980、UM982、UMD982、UB9A0、UBD9A0

表 4-45 RTCM 数据过滤指令参数

| 指令头  | 功能名称     | 参数    | 参数描述                   |
|---------|--------------|---------|----------------------------|
|  CONFIG |  RTCMDECAUTO | ENABLE  | 启用 RTCM 数据过滤         |
|         |              | DISABLE | 关闭 RTCM 数据过滤（默认） |

### 星历输出配置

该指令用于配置接收机一次输出的卫星星历数量。使能该指令后，接收机会一次性输出某卫星系统下所有卫星的星历。

命令格式：

CONFIG ALLEPHRTCM [参数]

命令示例：

CONFIG ALLEPHRTCM ENABLE

适用产品：UM980、UMD980、UM982、UMD982、UB9A0、UBD9A0

表 4-46 星历输出配置指令参数

| 指令头  | 功能名称    | 参数    | 参数描述                         |
|---------|-------------|---------|----------------------------------|
|  CONFIG |  ALLEPHRTCM | ENABLE  | 输出所有卫星的星历               |
|         |             | DISABLE | 一次仅输出一颗卫星的星历（默认） |

### 速度STD 门限配置

该指令用于配置速度 STD 门限，当超出配置时将速度标记为无效。

命令格式：

CONFIG VELSTDTHD [参数 1] [参数 2] [参数 3]

命令示例：

CONFIG VELSTDTHD ENABLE 120 120

适用产品：UM982、UMD982、UB9A0

表 4-47 速度 STD 门限配置参数

| 指令头 | 功能名称  | 参数 1            | 参数 2             | 参数 3           |
|--------|-----------|-------------------|--------------------|------------------|
|        |           | ENABLE            | HORSTD             | VERSTD           |
|        |           | 开启速度 STD 门限 | 水平方向上的速度   | 垂直方向上的速度 |
|        |           | 配置              | STD 值，单位       | STD 值，单位     |
|        |           |                   | cm/s，范围：       | cm/s，范围：     |
| CONFIG | VELSTDTHD |                   | 10\~1000，只能取整 | 10\~1000，只能取 |
|        |           |                   | 数，默认为 50      | 整数，默认为 50  |
|        |           | DISABLE           | -                  | -                |
|        |           | 关闭速度 STD 门限 |                    |                  |
|        |           | 配置（默认状态）  |                    |                  |

### RTK 辅助 PPP 定位配置

该指令用于开启或关闭 RTK 结果辅助 PPP 收敛和定位的功能。

命令格式：

CONFIG RTKASITPPP [参数]

命令示例：

CONFIG RTKASITPPP ENABLE

适用产品：UM982、UMD982、UB9A0

表 4-48 RTK 辅助 PPP 定位配置参数

| 指令头  | 功能名称    | 参数    | 参数描述                                   |
|---------|-------------|---------|--------------------------------------------|
|  CONFIG |  RTKASITPPP | ENABLE  | 开启RTK 结果辅助PPP 收敛和定位功能（默认） |
|         |             | DISABLE | 关闭 RTK 结果辅助 PPP 收敛和定位功能       |

### 指令校验配置

该指令用于配置模块输入指令格式是否强制为带校验模式。

带校验模式可以避免模块误识别指令。若用户使用带校验的指令，首先需要将 CONFIG CMDFORMAT 配置为 1，其次再输入带异或校验的命令，例如：\$RESET\*55。

命令格式：

CONFIG CMDFORMAT [参数]

命令示例：

CONFIG CMDFORMAT 1

适用产品：UM982、UMD982、UB9A0

表 4-49 指令校验配置参数

| 指令头  | 功能名称   | 参数 | 参数描述                                 |
|---------|------------|------|------------------------------------------|
|  CONFIG |  CMDFORMAT | 0    | 关闭校验模式（默认），输入的指令不带校验 |
|         |            | 1    | 开启校验模式，输入的指令带异或校验       |

# MASK 指令

### 接收机 MASK 配置查询

高精度接收机支持用 MASK 指令查询当前的配置。

命令格式为：

MASK

命令示例：

MASK

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出示例：

\$CONFIG,MASK,MASK 5.000000\*15

\$CONFIG,MASK,MASK GPS\*4A

\$CONFIG,MASK,MASK 10.000000\*21

\$CONFIG,MASK,GPSMaskPrn:12,\*13

\$CONFIG,MASK,QZSSMaskPrn:194,\*63

表 5-1 接收机 MASK 配置查询指令

| 指令 | 描述                       |
|------|----------------------------|
| MASK | 查询接收机当前的 MASK 配置 |

### MASK 用于屏蔽接收机接收的卫星系统

本指令用于设置接收机接收到的卫星系统、卫星频点、卫星截止高度角。如设置截止高度角，当卫星上升到高于截止高度角位置时，接收机才会自动搜索卫星；当卫星下降到低于截止高度角位置时接收机不再搜索卫星，除非进行重新配置。MASK 高度角默认配置为 5 度。

MASK 卫星系统/UNMASK 卫星系统与 MASK 特定卫星号/UNMASK 特定卫星号不能混合使用，即，当MASK 某个卫星系统时，使用 UNMASK 该系统的特定卫星号时，UNMASK卫星号操作将不起作用。

命令格式为：

MASK [频点/卫星系统] MASK [高度角]

MASK [卫星系统] PRN [卫星号] MASK RTCMCN0 [数值] [频点(可选)]

MASK CN0 [数值] [频点(可选)]

命令示例：

MASK GPS 禁止接收机跟踪 GPS 卫星系统

MASK BDS 禁止接收机跟踪BDS 卫星系统

MASK GLO 禁止接收机跟踪 GLO 卫星系统

MASK GAL 禁止接收机跟踪 GAL 卫星系统 MASK QZSS 禁止接收机跟踪 QZSS 卫星系统

MASK 10 设置接收机跟踪卫星的截止角度为 10 度

MASK 0 设置接收机跟踪卫星的截止角度为 0 度 MASK B1 禁止接收机跟踪北斗卫星系统的 B1 频点信号

MASK E5a 禁止接收机跟踪 Galileo 卫星系统的 E5a 频点信号 MASK GPS PRN 10 禁止接收机跟踪GPS 卫星系统的第 10 号卫星

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 5-2 Mask 指令参数（1）

| 功能名称 | 参数 1                                                     |
|----------|------------------------------------------------------------|
|  MASK    | 频点/ 卫星系统 （见[表5-5 卫星系统及频点](#_bookmark129)） |

表 5-3 Mask 指令参数（2）

| 功能名称 | 参数 1                                |
|----------|---------------------------------------|
|  MASK    |  高度角（范围：-90°\~90°；默认为 5°） |

表 5-4 Mask 指令参数（3）

| 功能名称 | 参数 1    | 固定值 | 参数 2                           |
|----------|-----------|--------|----------------------------------|
|  MASK    |  卫星系统 |  PRN   | 卫星号 （见 OBSVM 中卫星号定义） |

表 5-5 卫星系统及频点

| 序号   | 系统     | 卫星频点                                                | 描述                                                                                                                                                                                                                                                 |
|--------|----------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    1   |    GPS   |   L1、L1CA、L1C、 L2、L2C、L2P、L5                      | GPS 卫星系统支持频点信号：L1CA（即 L1C/A）、 L1C、L2C、L2P、L5 当 MASK L1 时，作用到 L1C/A 和 L1C； 当 MASK L2 时，作用到 L2C 和 L2P；                                                                                                               |
|      2 |      BDS |    B1、B2、B3、 B1I、B2I、B3I、 BD3B1C、 BD3B2A、BD3B2B | 北斗二号卫星系统支持频点信号：B1I、B2I、B3I北斗三号卫星系统支持频点信号：B1I、B3I 北斗三号卫星系统支持频点信号： BD3B1C 、 BD3B2A、BD3B2B 当 MASK B1 时，作用到 B1I 和 BD3B1C； 当 MASK B2 时，作用到 B2I 和 B2a 和 B2b；当 MASK B3 时，作用到 B3I； |
| 3      | GLO      | R1、R2、R3                                              | GLONASS 系统支持频点信号：R1、R2、R3                                                                                                                                                                                                                 |
|  4     |  GAL     | E1 、 E5a 、 E5b 、 E6C                                 |  伽利略系统支持频点信号：E1、E5b、E5a、E6C                                                                                                                                                                                                           |

| 序号  | 系统     | 卫星频点                     | 描述                                                                                                                                                                                                                             |
|-------|----------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     5 |     QZSS |    Q1、Q2、Q5 Q1CA、Q1C、Q2C | QZSS 系统支持频点信号： Q1 、 Q2 、 Q5 （即 QZSSL5 ） 、Q1CA（即 QZSSL1C/A ） 、Q1C （即 QZSSL1C）、Q2C（即 QZSSL2C） 当 MASK Q1 时，作用到 QZSSL1C/A 和 QZSSL1C；当 MASK Q2 时，作用到 QZSSL2C； 当 MASK Q5 时，作用到 QZSSL5； |
|  6    |  IRNSS   |  I5                          | IRNSS 系统支持频点信号：I5 (IRNSS L5) 当 MASK I5 时，作用到 IRNSS L5；                                                                                                                                                           |

表 5-6 Mask RTCMCN0、CN0 指令

| 功能名称 | 指令      | 参数 1                                 | 参数 2（可选）                                                           |
|----------|-----------|----------------------------------------|--------------------------------------------------------------------------|
|     MASK |   RTCMCN0 | C/N0 数值， 限制 RTCM 输出的原始观测值 |  频点(参见[表5-5](#_bookmark129))，当参数 2 配置为空时，将作用到所有频点 |
|          |   CN0     | C/N0 数值， 限制 OBSV 输出的原始观测值 |  频点(参见[表5-5](#_bookmark129))，当参数 2 配置为空时，将作用到所有频点 |

-   Mask RTCMCN0 及 MASK CN0 指令：UM982 Build9669 及之后的版本支持

### UNMASK 用于解除屏蔽接收机接收的卫星系统

该指令用于设置接收机接收到的卫星系统、卫星频点。

命令格式为：

UNMASK [频点/卫星系统] UNMASK [卫星系统] PRN [卫星号]

命令示例：

UNMASK GPS 使能接收机跟踪 GPS 卫星系统

UNMASK BDS 使能接收机跟踪 BDS 卫星系统 UNMASK GLO 使能接收机跟踪 GLO 卫星系统 UNMASK GAL 使能接收机跟踪 GAL 卫星系统

UNMASK B1 使能接收机跟踪 BDS 卫星系统的 B1 频点信号 UNMASK E5a 使能接收机跟踪 Galileo 卫星系统的 E5a 频点信号

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 5-7 Unmask 指令参数（1）

| 功能名称 | 参数                                                       |
|----------|------------------------------------------------------------|
|  UNMASK  | 频点/ 卫星系统 （见[表5-5 卫星系统及频点](#_bookmark129)） |

表 5-8 Unmask 指令参数（2）

| 功能名称 | 参数 1    | 固定值 | 参数 2                           |
|----------|-----------|--------|----------------------------------|
|  UNMASK  |  卫星系统 |  PRN   | 卫星号 （见 OBSVM 中卫星号定义） |

# AGNSS 辅助位置和辅助时间信息输入

### 辅助位置信息输入

本指令用于输入辅助位置信息（辅助位置与实际位置误差不宜超过 10000m）。

消息格式：

\$AIDPOS,Latitude,LatDir,Longitude,LonDir,Altitude

输入示例：

\$AIDPOS,4002.229934,N,11618.096855,E,37.254

适用产品：UM982、UMD982、UM980、UMD980、UB9A0、UBD9A0

表 6-1 AGNSS 辅助位置信息参数定义

| 序号 | 参数名      | 类型     | 描述                                              |
|------|-------------|----------|---------------------------------------------------|
|   1  |   Latitude  |   DOUBLE | 纬度，格式为 ddmm.mmmmmm dd – 度 mm.mmmmmm – 分   |
|   2  |   LatDir    |   Str    | 北纬或南纬指示 N – 北纬 S – 南纬                  |
|   3  |   Longitude |   DOUBLE | 经度，格式为 dddmm.mmmmmm ddd – 度 mm.mmmmmm – 分 |
|   4  |   LonDir    |   Str    | 东经或西经指示 E – 东经 W – 西经                  |
| 5    | Altitude    | DOUBLE   | 椭球高，单位米                                    |

### 辅助时间信息输入

本指令用于输入辅助时间信息（UTC 时间误差±3s）。

消息格式：

\$AIDTIME,Year,Month,Day,Hour,Minute,Second,Millisecond,Leapsec

输入示例：

\$AIDTIME,2021,12,3,15,2,36,400,18

适用产品：UM982、UMD982、UM980、UMD980、UB9A0、UBD9A0

表 6-2 AGNSS 辅助时间信息参数定义

| 序号 | 参数名      | 类型 | 描述 |
|------|-------------|------|------|
| 1    | Year        | UINT | 年   |
| 2    | Month       | UINT | 月   |
| 3    | Day         | UINT | 日   |
| 4    | Hour        | UINT | 时   |
| 5    | Minute      | UINT | 分   |
| 6    | Second      | UINT | 秒   |
| 7    | Millisecond | UINT | 毫秒 |
| 8    | Leapsec     | UINT | 闰秒 |

# 数据输出指令

数据输出指令用于输出定位、定向等信息，包括：1）NMEA 标准数据输出指令；2） Unicore 扩展的NMEA 数据输出指令；3）Unicore 定义的数据输出指令。

命令格式为：

[命令名称] [串口号(可选)] [输出频率/ONCHANGED (可选)]

命令示例：

GPGGA 1

GPGGA COM2 1 GPSIONA ONCHANGED

OBSVBASEA COM1 ONCHANGED VERSIONA

-   [串口号] 和[输出频率] 为可选参数。若不设定[串口号]，则默认在当前串口输出消息；若不设定[输出频率]，则只输出一次消息。
-   ONCHANGED 输出频率不固定。当输出一次消息之后，若消息内容有变化，则再次输出，否则不再输出。该请求方式只适用于 Unicore 格式的部分消息，详见各小节消息说明。
-   目前支持的输出频率仅包括 1Hz、2Hz、5Hz、10Hz、20Hz、50Hz\*，对应的参数分别为 1、0.5、0.2、0.1、0.05、0.02\*。

### NMEA 数据输出指令

当用户使用 Unicore 产品请求 NMEA 消息时，需在消息名称前加 GP，例如 GPGSV、 GPGGA 等，不可使用 GB、GL、GA、GN 等字符作为指令请求消息。在消息输出中，GP代表 GPS 系统，GB 代表 BDS 系统……GN 代表多系统联合定位（命令输入仍为 GP）。

下表为各卫星系统对应的符号说明：

\* 50Hz 输出频率需要特定产品、特定固件支持

表 7-1 卫星系统及其简化符号

| 卫星系统       | 指令      | 消息输出 |
|----------------|-----------|----------|
| GPS            |     GP--- | GP---    |
| BDS            |           | GB---    |
| GLONASS        |           | GL---    |
| Galileo        |           | GA---    |
| QZSS           |           | GQ---    |
| 多系统联合定位 |           | GN---    |

#### NMEA V4.10（默认）

##### GPDTM 坐标信息

本指令用于输出大地坐标系信息。包含纬度、经度及偏移量等。

简化ASCII 格式：

GPDTM 1 当前串口输出 1Hz 的 GPDTM 信息 GPDTM COM2 1 在com2 输出 1Hz 的 GPDTM 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNDTM,W84,,0.0,N,0.0,E,0.0,W84\*71

表 7-2 DTM 数据结构

| ID   | 字段          | 数据描述                                             | 符号   |
|------|---------------|------------------------------------------------------|--------|
| 1    | \$--DTM       | Log 头                                               |        |
|    2 |    Datum code | 本地坐标系代码： W84 = WGS84 W72 = WGS72 S85 = SGS85 |    ccc |

| ID   | 字段             | 数据描述                                                        | 符号   |
|------|------------------|-----------------------------------------------------------------|--------|
|      |                  | P90 = PE90 999 = 用户自定义 IHO datum code1                     |        |
|  3   |  Sub code        | 坐标系子代码，占一个字符。 用户自定义坐标系的参考字符，或为空   |  a     |
| 4    | Lat offset       | 纬度偏移量，单位分，N/S，保留 1 位小数                          | x.x    |
| 5    | Lat dir          | 纬度偏移标记(N, S)                                              | a      |
| 6    | Lon offset       | 经度偏移量，单位分，E/W，保留 1 位小数                          | x.x    |
| 7    | Lon dir          | 经度偏移标记(E, W)                                              | a      |
| 8    | Alt offset       | 海拔偏移量，单位米，保留 1 位小数                               | x.x    |
|    9 |    Rf datum code | 参考坐标系代码： W84 = WGS84 W72 = WGS72 S85 = SGS85 P90 = PE90 |    ccc |
| 10   | \*xx             | 校验和                                                          |        |
| 11   | [CR][LF]         | 语句结束符                                                      |        |

1 若使用的坐标系不在上述列表中，使用 IHO 坐标代码；若坐标系未知，此字段为空

##### GPGBS 卫星故障检测信息

本指令用于卫星故障检测（支持 RAIM）。

简化ASCII 格式：

GPGBS 1 当前串口输出 1Hz 的 GPGBS 信息 GPGBS COM2 1 在com2 输出 1Hz 的 GPGBS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGBS,023509.00,0.5,0.4,1.3,39,0.0,2.1,10.6,5,6\*42

表 7-3 GBS 数据结构

| ID   | 字段      | 数据描述                                                                  | 符号         |
|------|-----------|---------------------------------------------------------------------------|--------------|
| 1    | \$--GBS   | Log 头                                                                    |              |
|    2 |    Utc    | 已知位置的 UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒      |    hhmmss.ss |
| 3    | Lat exp   | 纬度预期误差，单位米，保留 1 位小数                                       | x.x          |
| 4    | Lon exp   | 经度预期误差，单位米，保留 1 位小数                                       | x.x          |
| 5    | Alt exp   | 海拔预期误差，单位米，保留 1 位小数                                       | x.x          |
|    6 |    ID     | 故障卫星 ID GPS:1\~32 GLONASS: 65\~99 Galileo: 1\~36, 37\~64 SBAS: 33\~64 |    x.x       |
| 7    | pro       | 故障卫星漏检概率，保留 1 位小数                                           | x.x          |
| 8    | est       | 故障卫星估计偏差，单位米，保留 1 位小数                                   | x.x          |
| 9    | Dev std   | 偏差估计标准差，保留 1 位小数                                             | x.x          |
| 10   | Sys id    | GNSS 系统 ID，参考[表7-34 GNSS ID](#_bookmark181)                         | h            |
| 11   | Signal id | GNSS 信号 ID，参考[表7-34 GNSS ID](#_bookmark181)                         | h            |
| 12   | \*xx      | 校验和                                                                    |              |
| 13   | [CR][LF]  | 语句结束符                                                                |              |

##### GPGGA 卫星定位信息

本指令用于输出卫星系统定位数据。

简化ASCII 格式：

GPGGA 1 当前串口输出 1Hz 的 GPGGA 信息 GPGGA COM2 1 在 com2 输出 1Hz 的 GPGGA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGGA,023634.00,4004.73871635,N,11614.19729418,E,1,28,0.7,61.0988,M,- 8.4923,M,,\*58

表 7-4 GGA 数据结构

| ID   | 字段    | 数据描述                                                             | 符号         |
|------|---------|----------------------------------------------------------------------|--------------|
| 1    | \$--GGA | Log 头                                                               |              |
|    2 |    utc  | 位置对应的 UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|   3  |   lat   | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm：分                   |   IIII.II    |
| 4    | lat dir | 纬度方向（N = 北纬，S =南纬）                                        | a            |
|   5  |   lon   | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                |   yyyyy.yy   |
| 6    | lon dir | 经度方向（E = 东经，W = 西经）                                       | a            |
|  7   |  qual   | GPS 状态 0 = 定位不可用或无效                                        |  x           |

| ID    | 字段         | 数据描述                                                                                                           | 符号   |
|-------|--------------|--------------------------------------------------------------------------------------------------------------------|--------|
|       |              | 1 = 单点定位 2 = 差分定位 3 = GPS PPS 模式 4 = RTK Int 5 = RTK Float 6 = 惯导模式 7 = 手动输入模式 8 = 模拟器模式  |        |
| 8     | \# sats      | 使用中的卫星数。可能与所见数不一致                                                                                 | xx     |
| 9     | hdop         | 水平精度因子，保留 1 位小数                                                                                        | x.x    |
|  10   |  alt         | 海拔高度，参考 MSL（大地水准面），保 留 4 位小数                                                                   |  x.x   |
| 11    | a-units      | 海拔高度单位（M = m）                                                                                              | M      |
|   12  |   undulation | 地球椭球面相对大地水准面的高度。大地水准面高于椭球面为正值，否则，为负 值。保留 4 位小数                           |   x.x  |
|  13   |  u-units     | 地球椭球面相对大地水准面的高度单位（M = m）                                                                        |  M     |
|    14 |    age       | 差分数据龄期，单位秒（从最近一次接收到差分信号 SC104 Type1 或 9 开始的秒数），保留 2 位小数。不是差分定位时， 为空 |    x.x |
| 15    | stn ID       | 差分基站 ID，0000-1023                                                                                             | xxxx   |
| 16    | \*xx         | 校验和                                                                                                             | \*hh   |
| 17    | [CR][LF]     | 语句结束符                                                                                                         |        |

##### GPGLL 地理位置信息

本指令用于输出地理位置经度/纬度信息。

简化ASCII 格式：

GPGLL 1 当前串口输出 1Hz 的 GPGLL 信息 GPGLL COM2 1 在com2 输出 1Hz 的 GPGLL 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGLL,4004.73885655,N,11614.19746477,E,023842.00,A,A\*75

表 7-5 GLL 数据结构

| ID   | 字段      | 数据描述                                                  | 符号        |
|------|-----------|-----------------------------------------------------------|-------------|
| 1    | \$--GLL   | Log 头                                                    |             |
|   2  |   lat     | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分       |   IIII.II   |
| 3    | lat dir   | 纬度方向（N = 北纬，S =南纬）                             | a           |
|   4  |   lon     | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分     |   yyyyy.yy  |
| 5    | lon dir   | 经度方向（E = 东经，W = 西经）                            | a           |
|    6 |    Utc    | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |   hhmmss.ss |
|    7 |    status | 状态： V = 数据无效 A = 自适应 D = 差分                   |    A        |

| ID     | 字段          | 数据描述                                                                                 | 符号   |
|--------|---------------|------------------------------------------------------------------------------------------|--------|
|      8 |      mode ind | 定位系统模式： N = 未定位 A = 自主定位 D = 差分定位 E = 惯导模式 M = 手动输入 S = 模拟器 |      a |
| 9      | \*xx          | 校验和                                                                                   | \*hh   |
| 10     | [CR][LF]      | 语句结束符                                                                               |        |

##### GPGNS 定位数据输出

本指令用于输出GNSS 定位数据。

简化ASCII 格式：

GPGNS 1 当前串口输出 1Hz 的 GPGNS 信息 GPGNS COM2 1 在 com2 输出 1Hz 的 GPGNS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGNS,024034.00,4004.73854216,N,11614.19720023,E,ANAAA,28,0.8,61.6865,- 8.4923,,,S\*4E

表 7-6 GNS 数据结构

| ID | 字段    | 数据描述 | 符号 |
|----|---------|----------|------|
| 1  | \$--GNS | Log 头   |      |

| ID          | 字段           | 数据描述                                                                                                                                                                                                                      | 符号           |
|-------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
|    2        |    utc         | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                                                                                                                                     |    hhmmss.ss   |
|   3         |   Lat          | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分                                                                                                                                                                           |   IIII.II      |
| 4           | Lat dir        | 纬度方向（N = 北纬，S =南纬）                                                                                                                                                                                                 | a              |
|   5         |   Lon          | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                                                                                                                                                                         |   yyyyy.yy     |
| 6           | Lon dir        | 经度方向（E = 东经，W = 西经）                                                                                                                                                                                                | a              |
|           7 |           mode | 模式标识。字符长度可变，前 3 个字符依次为 GPS、GLONASS、Galileo 卫星系统每个卫星系统包含以下模式： A = 自主模式 D = 差分模式 E = 惯导模式 F = RTK Float M = 手动输入模式 N = 未定位 P = 高精度模式 R = RTK Int S = 模拟器模式 |           c--c |
| 8           | Use sat        | 使用中的卫星数，00-99                                                                                                                                                                                                         | xx             |
| 9           | Hdop           | 水平精度因子 HDOP，保留 1 位小数                                                                                                                                                                                              | x.x            |
|  10         |  Ant alt       | 天线高，单位米，保留 4 位小数， 参考 MSL（大地水准面）                                                                                                                                                                        |  x.x           |

| ID    | 字段       | 数据描述                                                                                           | 符号  |
|-------|------------|----------------------------------------------------------------------------------------------------|-------|
|   11  |   Geo sep  | 地球椭球面相对大地水准面的高度，单位 米。大地水准面高于椭球面为正值，否则，为负值。保留 4 位小数。 |   x.x |
|  12   |  Age       | 1 差分数据龄期，单位秒，保留 2 位小数。 非差分定位时为空                                           |  x.x  |
| 13    | Station id | 2 差分基站 ID。非差分定位时为空                                                                    | x.x   |
|    14 |    status  | 导航状态指示 S = 安全 C = 注意 U = 危险 V = 导航状态不可用                                         |    a  |
| 15    | \*xx       | 校验和                                                                                             | \*hh  |
| 16    | [CR][LF]   | 语句结束符                                                                                         |       |

1,2 若 log 头为\$GNGNS 且多个卫星系统为差分模式，差分数据龄期（字段 12）和差分站 ID（字段 13）为空

##### GPGRS 定位解算的卫星残差

本指令用于输出定位解算的卫星的残差，支持 RAIM。

简化ASCII 格式：

GPGRS 1 当前串口输出 1Hz 的 GPGRS 信息 GPGRS COM2 1 在com2 输出 1Hz 的 GPGRS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGRS,024356.00,0,0.1,0.2,0.1,0.2,0.4,,,,,,,,1,1\*7D

\$GNGRS,024356.00,0,0.1,0.1,0.3,0.1,0.2,,,,,,,,1,4\*7C

\$GNGRS,024356.00,0,0.1,,0.1,0.0,0.1,,,,,,,,1,8\*5F

\$GNGRS,024356.00,0,0.7,0.2,0.4,0.1,,,,,,,,,3,7\*53

\$GNGRS,024356.00,0,0.1,0.1,0.1,0.1,,,,,,,,,3,1\*55

\$GNGRS,024356.00,0,0.1,0.1,0.1,0.1,,,,,,,,,3,2\*56

\$GNGRS,024356.00,0,0.2,1.4,0.7,0.2,0.7,0.5,0.2,0.2,0.3,0.3,0.6,1.0,4,1\*55

\$GNGRS,024356.00,0,1.8,0.3,0.3,0.6,1.2,,,,,,,,4,1\*70

\$GNGRS,024356.00,0,0.2,0.3,0.2,0.1,0.3,0.2,0.2,0.1,0.1,0.1,0.2,0.1,4,8\*58

\$GNGRS,024356.00,0,0.3,0.1,0.1,0.1,0.2,,,,,,,,4,8\*75

\$GNGRS,024356.00,0,0.2,0.4,0.2,0.2,0.2,0.2,0.6,0.2,,,,,4,11\*61

\$GNGRS,024356.00,0,0.2,0.7,,,,,,,,,,,5,1\*56

\$GNGRS,024356.00,0,0.1,0.2,,,,,,,,,,,5,6\*57

\$GNGRS,024356.00,0,0.1,0.1,,,,,,,,,,,5,8\*5A

表 7-7 GRS 数据结构

| ID   | 字段    | 数据描述                                                                                                                            | 符号         |
|------|---------|-------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1    | \$--GRS | Log 头                                                                                                                              |              |
|    2 |    Utc  | GGA/GNS UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                                   |    hhmmss.ss |
|    3 |    Mode | 模式： 0 = 用于计算匹配 GGA /GNS 中给定位置的残差 1 = 在计算 GGA/GNS 位置后重新计算的残 差                                          |    x         |
| 4    |    Res  | 参与定位解算的卫星的范围残差，单位米。范围：±999。保留 1 位小数。 如果范围残差超过±99.9，则舍弃小数部 分，取整数（如-103.7 取-103） | x.x          |
| 5    |         |                                                                                                                                     | x.x          |
| 6    |         |                                                                                                                                     | x.x          |
| 7    |         |                                                                                                                                     | x.x          |

| ID | 字段      | 数据描述                                          | 符号 |
|----|-----------|---------------------------------------------------|------|
| 8  |           |                                                   | x.x  |
| 9  |           |                                                   | x.x  |
| 10 |           |                                                   | x.x  |
| 11 |           |                                                   | x.x  |
| 12 |           |                                                   | x.x  |
| 13 |           |                                                   | x.x  |
| 14 |           |                                                   | x.x  |
| 15 |           |                                                   | x.x  |
| 16 | Sys id    | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181) | h    |
| 17 | Signal id | 信号 ID。参考[表7-34 GNSS ID](#_bookmark181)      | h    |
| 18 | \*xx      | 校验和                                            | \*hh |
| 19 | [CR][LF]  | 语句结束符                                        |      |

##### GPGSA 参与定位解算的卫星信息

本指令用于输出接收机工作模式、参与定位解算的卫星及 DOP 等信息。

简化ASCII 格式：

GPGSA 1 当前串口输出 1Hz 的 GPGSA 信息 GPGSA COM2 1 在 com2 输出 1Hz 的 GPGSA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGSA,M,3,10,12,23,25,32,,,,,,,,1.7,0.7,1.5,1\*3D

\$GNGSA,M,3,05,09,24,31,,,,,,,,,1.7,0.7,1.5,3\*32

\$GNGSA,M,3,01,02,03,06,08,09,13,16,19,20,36,37,1.7,0.7,1.5,4\*34

\$GNGSA,M,3,38,39,46,59,60,,,,,,,,1.7,0.7,1.5,4\*34

\$GNGSA,M,3,02,07,,,,,,,,,,,1.7,0.7,1.5,5\*39

表 7-8 GSA 数据结构

| ID   | 字段          | 数据描述                                                                                           | 符号 |
|------|---------------|----------------------------------------------------------------------------------------------------|------|
| 1    | \$--GSA       | Log 头                                                                                             |      |
|   2  |   mode MA     | 卫星工作模式： M = 手动设置 2D/3D 模式 A = 自动切换 2D/3D 模式                                     |   a  |
|    3 |    mode 123   | 定位模式： 1 = 未定位 2 = 2D 3 = 3D                                                                |    x |
| 4    |           prn |          参与定位解算的卫星 ID，详见[表7-36 NMEA 消](#_bookmark184)[息中的卫星 PRN](#_bookmark184) | xx   |
| 5    |               |                                                                                                    | xx   |
| 6    |               |                                                                                                    | xx   |
| 7    |               |                                                                                                    | xx   |
| 8    |               |                                                                                                    | xx   |
| 9    |               |                                                                                                    | xx   |
| 10   |               |                                                                                                    | xx   |
| 11   |               |                                                                                                    | xx   |
| 12   |               |                                                                                                    | xx   |
| 13   |               |                                                                                                    | xx   |
| 14   |               |                                                                                                    | xx   |
| 15   |               |                                                                                                    | xx   |
| 16   | pdop          | PDOP，保留 1 位小数                                                                                | x.x  |
| 17   | hdop          | HDOP，保留 1 位小数                                                                                | x.x  |
| 18   | vdop          | VDOP，保留 1 位小数                                                                                | x.x  |
| 19   | SysID         | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                  | h    |
| 20   | \*xx          | 校验和                                                                                             | \*hh |
| 21   | [CR][LF]      | 语句结束符                                                                                         |      |

##### GPGST 伪距观测误差信息

本指令用于输出伪距误差信息。

简化ASCII 格式：

GPGST 1 当前串口输出 1Hz 的 GPGST 信息 GPGST COM2 1 在com2 输出 1Hz 的 GPGST 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGST,054013.00,0.67,1.67,1.37,115.3800,1.432,1.620,3.399\*41

表 7-9 GST 数据结构

| ID   | 字段     | 数据描述                                                          | 符号         |
|------|----------|-------------------------------------------------------------------|--------------|
| 1    | \$--GST  | Log 头                                                            |              |
|    2 |    utc   | GGA/GNS UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|  3   |  rms     | 伪距、DGNSS 改正数标准差（RMS 值），保留 2 位 小数                |  x.x         |
| 4    | smjr std | 误差椭圆长半轴的标准差，单位米，保留 2 位小数                     | x.x          |
| 5    | smnr std | 误差椭圆短半轴的标准差，单位米，保留 2 位小数                     | x.x          |
| 6    | orient   | 误差椭圆长半轴方向，与真北夹角，保留 4 位小数                     | x.x          |
| 7    | lat std  | 纬度误差标准差，单位米，保留 3 位小数                             | x.x          |
| 8    | lon std  | 经度误差标准差，单位米，保留 3 位小数                             | x.x          |
| 9    | alt std  | 高程误差标准差，单位米，保留 3 位小数                             | x.x          |
| 10   | \*xx     | 校验和                                                            | \*hh         |
| 11   | [CR][LF] | 语句结束符                                                        |              |

##### GPGSV 可视卫星信息

本指令用于输出可视卫星数量、ID 等信息。

简化ASCII 格式：

GPGSV 1 当前串口输出 1Hz 的 GPGSV 信息 GPGSV COM2 1 在 com2 输出 1Hz 的 GPGSV 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GPGSV,2,1,06,32,48,134,47,31,70,011,46,25,24,046,32,29,27,081,39,1\*61

\$GPGSV,2,2,06,26,60,213,46,16,20,213,30,1\*64

\$GPGSV,2,1,05,32,48,134,43,31,70,011,43,25,24,046,34,29,27,081,37,4\*6E

\$GPGSV,2,2,05,26,60,213,44,4\*56

\$GPGSV,1,1,03,32,48,134,49,25,24,046,41,26,60,213,50,8\*59

\$GLGSV,2,1,06,82,04,015,32,71,34,167,43,65,36,322,37,73,27,042,37,1\*72

\$GLGSV,2,2,06,74,66,350,47,72,76,245,48,1\*73

\$GLGSV,2,1,05,82,04,015,28,71,34,167,43,65,36,322,32,73,27,042,39,3\*73

\$GLGSV,2,2,05,72,76,245,45,3\*49

\$GBGSV,6,1,21,36,72,016,49,19,24,172,36,39,75,082,50,30,13,111,38,1\*7B

\$GBGSV,6,2,21,10,30,201,35,27,10,062,32,01,34,140,40,07,40,195,39,1\*74

\$GBGSV,6,3,21,16,78,051,49,22,59,233,48,09,69,327,45,59,38,144,43,1\*73

\$GBGSV,6,4,21,03,42,188,39,04,25,124,36,40,48,180,45,45,41,261,40,1\*7D

\$GBGSV,6,5,21,60,28,227,36,02,33,224,32,46,25,059,35,21,32,308,35,1\*7F

\$GBGSV,6,6,21,06,79,008,47,1\*46

\$GBGSV,4,1,15,36,72,016,33,19,24,172,29,39,75,082,34,30,13,111,25,8\*7A

\$GBGSV,4,2,15,10,30,201,23,27,10,062,22,07,40,195,27,16,78,051,29,8\*71

\$GBGSV,4,3,15,22,59,233,32,09,69,327,28,40,48,180,31,45,41,261,27,8\*7E

\$GBGSV,4,4,15,46,25,059,24,21,32,308,22,06,79,008,30,8\*4E

\$GBGSV,3,1,10,10,30,201,40,01,34,140,45,07,40,195,44,16,78,051,49,B\*0E

\$GBGSV,3,2,10,09,69,327,48,03,42,188,45,04,25,124,42,02,33,224,41,B\*0D

\$GBGSV,3,3,10,05,16,248,37,06,79,008,48,B\*00

\$GAGSV,2,1,07,05,71,159,50,09,20,141,41,03,49,308,44,31,11,046,32,1\*74

\$GAGSV,2,2,07,02,10,226,38,24,59,047,47,25,60,226,48,1\*4D

\$GAGSV,2,1,07,05,71,159,52,09,20,141,42,03,49,308,47,31,11,046,34,2\*73

\$GAGSV,2,2,07,02,10,226,41,24,59,047,50,25,60,226,51,2\*4E

\$GAGSV,2,1,07,05,71,159,48,09,20,141,35,03,49,308,39,31,11,046,29,7\*78

\$GAGSV,2,2,07,02,10,226,27,24,59,047,45,25,60,226,45,7\*4A

\$GQGSV,1,1,02,02,70,095,46,07,42,163,35,1\*6F

\$GQGSV,1,1,02,02,70,095,46,07,42,163,40,6\*6A

\$GQGSV,1,1,02,02,70,095,50,07,42,163,47,8\*64

表 7-10 GSV 数据结构

| ID | 字段         | 数据描述                                                                                                                                     | 符号 |
|----|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|------|
| 1  | \$--GSV      | Log 头                                                                                                                                       |      |
| 2  | \# msgs      | GSV 消息总数，1\~9                                                                                                                           | x    |
| 3  | msg \#       | GSV 消息编号，1\~9                                                                                                                           | x    |
| 4  | \# sats      | 可视卫星数量                                                                                                                                 | xx   |
| 5  | Sat id       | 卫星 ID，详见[表7-36 NMEA 消息中的卫星 PRN](#_bookmark184)                                                                                   | xx   |
| 6  | Elevation    | 高度角，单位为度，整数，最大值 90                                                                                                            | xx   |
| 7  | Azi          | 方位角，与真北夹角，000\~359 之间的整数                                                                                                      | xxx  |
| 8  | CN0          | 载噪比（C/N0），0 \~ 99 dB-Hz，整数，不跟踪时为空                                                                                            | xx   |
| 9  |     Next sat |  第 2-3 位 SV，“卫星 ID-高度角-方位角-SNR”的集 和，字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。 | xx   |
| 10 |              |                                                                                                                                              | xx   |
| 11 |              |                                                                                                                                              | xxx  |
| 12 |              |                                                                                                                                              | xx   |
| 13 |              | 第 4 位 SV，“卫星 ID-高度角-方位角-SNR”的集和，                                                                                              | xx   |

| ID | 字段     | 数据描述                                                                                  | 符号 |
|----|----------|-------------------------------------------------------------------------------------------|------|
| 14 |          | 字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。 | xx   |
| 15 |          |                                                                                           | xxx  |
| 16 |          |                                                                                           | xx   |
| 17 | SignalID | GNSS 信号 ID。参考[表7-34 GNSS ID](#_bookmark181)                                         | h    |
| 18 | \*xx     | 校验和                                                                                    | \*hh |
| 19 | [CR][LF] | 语句结束符                                                                                |      |

##### GPTHS 航向信息

本指令用于输出航向、状态等信息。

简化ASCII 格式：

GPTHS 1 当前串口输出 1Hz 的 GPTHS 信息 GPTHS COM2 1 在com2 输出 1Hz 的 GPTHS 信息

适用产品：UM982、UMD982

消息输出：

\$GNTHS,341.3344,A\*1F

表 7-11 THS 数据结构

| ID    | 字段     | 数据描述                                                            | 符号  |
|-------|----------|---------------------------------------------------------------------|-------|
| 1     | \$--THS  | Log 头                                                              |       |
| 2     | Heading  | 航向，单位为度，保留 4 位小数                                       | x.x   |
|     3 |     Mode | 模式： A = 自主定位 E = 惯导 M = 手动输入 S = 模拟器 V = 数据不可用 |     a |

| ID | 字段     | 数据描述   | 符号 |
|----|----------|------------|------|
| 4  | \*xx     | 校验和     | \*hh |
| 5  | [CR][LF] | 语句结束符 |      |

##### GPRMC 卫星定位信息

本指令用于输出时间、日期、位置、速度等信息。

简化ASCII 格式：

GPRMC 1 当前串口输出 1Hz 的 GPRMC 信息 GPRMC COM2 1 在com2 输出 1Hz 的 GPRMC 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNRMC,054733.00,A,4004.73893635,N,11614.19823325,E,0.002,155.1,301221,6.9,

W,A,V\*4B

表 7-12 RMC 数据结构

| ID   | 字段         | 数据描述                                                  | 符号         |
|------|--------------|-----------------------------------------------------------|--------------|
| 1    | \$--RMC      | Log 头                                                    |              |
|    2 |    utc       | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|   3  |   pos status | 状态： A = 数据可用 V = 导航接收机警告                    |   A          |
|   4  |   lat        | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分       |   llll.ll    |

| ID          | 字段              | 数据描述                                                                                                                                                    | 符号       |
|-------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| 5           | lat dir           | 纬度方向（N = 北纬，S =南纬）                                                                                                                               | a          |
|   6         |   lon             | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                                                                                                        |   yyyyy.yy |
| 7           | lon dir           | 经度方向（E = 东经，W = 西经）                                                                                                                              | a          |
| 8           | speed Kn          | 地面速率，单位为节，保留 3 位小数                                                                                                                           | x.x        |
|  9          |  track true       | 地面航向，单位为度，从北向起顺时针计算，保留 1 位小数                                                                                                       |  x.x       |
| 10          | date              | 日期：ddmmyy                                                                                                                                                | xxxxxx     |
| 11          | mag var           | 磁偏角，单位：度，保留 1 位小数                                                                                                                             | x.x        |
| 12          | var dir           | 磁偏角方向                                                                                                                                                  | a          |
|          13 |          mode ind | 模式： A=自主模式 D = 差分模式 E = 惯导模式 F = RTK Float M = 手动输入模式 N = 无定位 P = 高精度模式 R = RTK int S = 模拟器模式 V = 模式无效（不包括 A, D） |          a |
|    14       |    mode status    | 定位状态： S = 安全 C = 注意 U = 危险 V = 定位状态不可用                                                                                                    |    a       |
| 15          | \*xx              | 校验和                                                                                                                                                      | \*hh       |

| ID | 字段     | 数据描述   | 符号 |
|----|----------|------------|------|
| 16 | [CR][LF] | 语句结束符 |      |

##### GPROT 旋转速度和方向信息

本指令用于输出旋转速度和方向信息。

简化ASCII 格式：

GPROT 1 当前串口输出 1Hz 的 GPROT 信息 GPROT COM2 1 在 com2 输出 1Hz 的 GPROT 信息

适用产品：UM982、UMD982

消息输出：

\$GNROT,0.0,V\*38

表 7-13 ROT 数据结构

| ID  | 字段     | 数据描述                             | 符号 |
|-----|----------|--------------------------------------|------|
| 1   | \$--ROT  | Log 头                               |      |
| 2   | rate     | 旋转速率，单位：度/分，保留 1 位小数 | x.x  |
|   3 |   status | 状态： A = 数据可用 V = 数据无效     |   A  |
| 4   | \*xx     | 校验和                               | \*hh |
| 5   | [CR][LF] | 语句结束符                           |      |

##### GPVTG 地面航向与速度信息

本指令用于输出地面航向、速度等信息。

简化ASCII 格式：

GPVTG 1 当前串口输出 1Hz 的 GPVTG 信息 GPVTG COM2 1 在 com2 输出 1Hz 的 GPVTG 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNVTG,335.750,T,342.678,M,0.00437,N,0.00810,K,A\*3F

表 7-14 VTG 数据结构

| ID       | 字段           | 数据描述                                                                                                  | 符号         |
|----------|----------------|-----------------------------------------------------------------------------------------------------------|--------------|
| 1        | \$--VTG        | Log 头                                                                                                    |              |
|  2       |  Course true   | 地面航向，单位为度，相对于真北，保留 3 位小 数                                                            |  x.x         |
| 3        | Course ind     | 航向标志，固定填 T                                                                                        | T            |
|  4       |  Course mag    | 地面航向，单位为度，相对于磁北，保留 3 位小 数                                                            |  x.x         |
| 5        | Course ind     | 航向标志，固定填 M                                                                                        | M            |
| 6        | speed Kn       | 地面速率，单位为节，保留 5 位小数                                                                         | x.x          |
| 7        | N              | 速率单位，固定填 N                                                                                        | N            |
| 8        | speed Km       | 地面速率，单位为 km/h，保留 5 位小数                                                                      | x.x          |
| 9        | K              | 速率单位，固定填 K                                                                                        | K            |
|       10 |       Mode ind | 模式： A=自主模式 D = 差分模式 E = 惯导模式 M = 手动输入模式 N = 数据不可用 P = 高精度模式 S = 模拟器模式 |       xxxxxx |
| 11       | \*xx           | 校验和                                                                                                    | \*hh         |
| 12       | [CR][LF]       | 语句结束符                                                                                                |              |

##### GPZDA 日期和时间

本指令用于输出UTC 时间和日期信息。

简化ASCII 格式：

GPZDA 1 当前串口输出 1Hz 的 GPZDA 信息 GPZDA COM2 1 在com2 输出 1Hz 的 GPZDA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNZDA,054931.00,30,12,2021,,\*73

表 7-15 ZDA 数据结构

| ID   | 字段              | 数据描述                                                  | 符号         |
|------|-------------------|-----------------------------------------------------------|--------------|
| 1    | \$--ZDA           | Log 头                                                    |              |
|    2 |    Utc            | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
| 3    | Day               | UTC 日，01\~31                                            | xx           |
| 4    | Month             | UTC 月，01\~12                                            | xx           |
| 5    | Year              | UTC 年                                                    | xxxx         |
| 6    | Local zone hour   | 本地时区的小时，00\~±13                                   | xx           |
| 7    | Local zone minute | 本地时区的分钟，00\~±59                                   | xx           |
| 8    | \*xx              | 校验和                                                    | \*hh         |
| 9    | [CR][LF]          | 语句结束符                                                |              |

#### NMEA V4.11

##### GPDTM 坐标信息

本指令用于输出大地坐标系信息。包含纬度、经度及偏移量等。

简化ASCII 格式：

GPDTM 1 当前串口输出 1Hz 的 GPDTM 信息 GPDTM COM2 1 在com2 输出 1Hz 的 GPDTM 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNDTM,W84,,0.0,N,0.0,E,0.0,W84\*71

表 7-16 DTM 数据结构

| ID     | 字段            | 数据描述                                                                                         | 符号     |
|--------|-----------------|--------------------------------------------------------------------------------------------------|----------|
| 1      | \$--DTM         | Log 头                                                                                           |          |
|      2 |      Datum code | 本地坐标系代码： W84 = WGS84 W72 = WGS72 S85 = SGS85 P90 = PE90 999 = 用户自定义 IHO datum code1 |      ccc |
|  3     |  Sub code       | 坐标系子代码，占一个字符。 用户自定义坐标系的参考字符，或为空                                    |  a       |
| 4      | Lat offset      | 纬度偏移量，单位分，N/S，保留 1 位小数                                                           | x.x      |
| 5      | Lat dir         | 纬度偏移标记(N, S)                                                                               | a        |
| 6      | Lon offset      | 经度偏移量，单位分，E/W，保留 1 位小数                                                           | x.x      |
| 7      | Lon dir         | 经度偏移标记(E, W)                                                                               | a        |

| ID   | 字段             | 数据描述                                                        | 符号   |
|------|------------------|-----------------------------------------------------------------|--------|
| 8    | Alt offset       | 海拔偏移量，单位米，保留 1 位小数                               |        |
|    9 |    Rf datum code | 参考坐标系代码： W84 = WGS84 W72 = WGS72 S85 = SGS85 P90 = PE90 |    ccc |
| 10   | \*xx             | 校验和                                                          |        |
| 11   | [CR][LF]         | 语句结束符                                                      |        |

1 若使用的坐标系不在上述列表中，使用 IHO 坐标代码；若坐标系未知，此字段为空

##### GPGBS 卫星故障检测

本指令用于卫星故障检测（支持 RAIM）。

简化ASCII 格式：

GPGBS 1 当前串口输出 1Hz 的 GPGBS 信息 GPGBS COM2 1 在com2 输出 1Hz 的 GPGBS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGBS,055214.00,0.3,0.3,0.8,45,0.0,-1.2,8.4,4,1\*58

表 7-17 GBS 数据结构

| ID   | 字段    | 数据描述                                                             | 符号         |
|------|---------|----------------------------------------------------------------------|--------------|
| 1    | \$--GBS | Log 头                                                               |              |
|    2 |    Utc  | 已知位置的 UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |

| ID    | 字段      | 数据描述                                                                             | 符号    |
|-------|-----------|--------------------------------------------------------------------------------------|---------|
| 3     | Lat exp   | 纬度预期误差，单位米，保留 1 位小数                                                  | x.x     |
| 4     | Lon exp   | 经度预期误差，单位米，保留 1 位小数                                                  | x.x     |
| 5     | Alt exp   | 海拔预期误差，单位米，保留 1 位小数                                                  | x.x     |
|     6 |     ID    | 故障卫星 ID GPS:1\~32 BDS: 1\~64 GLONASS: 65\~96 Galileo: 1\~36, 37\~64 SBAS: 33\~64 |     x.x |
| 7     | pro       | 故障卫星漏检概率，保留 1 位小数                                                      | x.x     |
| 8     | est       | 故障卫星估计偏差，单位米，保留 1 位小数                                              | x.x     |
| 9     | Dev std   | 偏差估计标准差，保留 1 位小数                                                        | x.x     |
| 10    | Sys id    | GNSS 系统 ID，参考[表7-34 GNSS ID](#_bookmark181)                                    | h       |
| 11    | Signal id | GNSS 信号 ID，参考[表7-34 GNSS ID](#_bookmark181)                                    | h       |
| 12    | \*xx      | 校验和                                                                               |         |
| 13    | [CR][LF]  | 语句结束符                                                                           |         |

##### GPGGA 卫星定位信息

本指令用于输出卫星系统定位数据。

简化ASCII 格式：

GPGGA 1 当前串口输出 1Hz 的 GPGGA 信息 GPGGA COM2 1 在 com2 输出 1Hz 的 GPGGA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGGA,055234.00,4004.73879510,N,11614.19821957,E,1,28,0.7,61.8089,M,-

8.4923,M,,\*50

表 7-18 GGA 数据结构

| ID       | 字段        | 数据描述                                                                                                                           | 符号         |
|----------|-------------|------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1        | \$--GGA     | Log 头                                                                                                                             |              |
|    2     |    utc      | 位置对应的 UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                               |    hhmmss.ss |
|   3      |   lat       | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm：分                                                                                 |   IIII.II    |
| 4        | lat dir     | 纬度方向（N = 北纬，S =南纬）                                                                                                      | a            |
|   5      |   lon       | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm：分                                                                               |   yyyyy.yy   |
| 6        | lon dir     | 经度方向（E = 东经，W = 西经）                                                                                                     | a            |
|        7 |        qual | GPS 状态 0 = 定位不可用或无效 1 = 单点定位 2 = 差分定位 3 = GPS PPS 模式 4 = RTK INT 5 = RTK Float 7 = 手动输入模式 8 = 模拟器模式 |        x     |
| 8        | \# sats     | 使用中的卫星数。可能与所见数不一致                                                                                                 | xx           |
| 9        | hdop        | 水平精度因子，保留 1 位小数                                                                                                        | x.x          |

| ID   | 字段         | 数据描述                                                                                                           | 符号  |
|------|--------------|--------------------------------------------------------------------------------------------------------------------|-------|
|  10  |  alt         | 海拔高度，参考 MSL（大地水准面），保留 4 位小数                                                                    |  x.x  |
| 11   | a-units      | 海拔高度单位（M = m）                                                                                              | M     |
|   12 |   undulation | 地球椭球面相对大地水准面的高度。大地水准面高于椭球面为正值，否则，为负值。保留 4 位小数。                          |   x.x |
|  13  |  u-units     | 地球椭球面相对大地水准面的高度单位（M = m）                                                                        |  M    |
|   14 |   age        | 差分数据龄期，单位秒（从最近一次接收到差 分信号 SC104 Type1 或 9 开始的秒数），保留 2 位小数。不是差分定位时，为空 |   x.x |
| 15   | stn ID       | 差分基站 ID，0000-1023                                                                                             | xxxx  |
| 16   | \*xx         | 校验和                                                                                                             | \*hh  |
| 17   | [CR][LF]     | 语句结束符                                                                                                         |       |

##### GPGLL 地理位置信息

本指令用于输出地理位置经度/纬度信息。

简化ASCII 格式：

GPGLL 1 当前串口输出 1Hz 的 GPGLL 信息 GPGLL COM2 1 在com2 输出 1Hz 的 GPGLL 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGLL,4004.73879998,N,11614.19807677,E,055322.00,A,A\*7C

表 7-19 GLL 数据结构

| ID    | 字段         | 数据描述                                                                    | 符号        |
|-------|--------------|-----------------------------------------------------------------------------|-------------|
| 1     | \$--GLL      | Log 头                                                                      |             |
|   2   |   lat        | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm：分                          |   IIII.II   |
| 3     | lat dir      | 纬度方向（N = 北纬，S =南纬）                                               | a           |
|   4   |   lon        | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm：分                        |   yyyyy.yy  |
| 5     | lon dir      | 经度方向（E = 东经，W = 西经）                                              | a           |
|    6  |    Utc       | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                   |   hhmmss.ss |
|    7  |    status    | 状态： A = 数据有效 V = 数据无效 D = 差分                                   |    A        |
|     8 |     mode ind | 定位系统模式： N = 未定位 A = 自主定位 D = 差分定位 M = 手动输入 S = 模拟器 |     a       |
| 9     | \*xx         | 校验和                                                                      | \*hh        |
| 10    | [CR][LF]     | 语句结束符                                                                  |             |

##### GPGNS 定位数据输出

本指令用于输出GNSS 定位数据。

简化ASCII 格式：

GPGNS 1 当前串口输出 1Hz 的 GPGNS 信息 GPGNS COM2 1 在 com2 输出 1Hz 的 GPGNS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGNS,060920.00,4004.73891567,N,11614.19148292,E,AAAAA,28,0.7,62.5759,- 8.4925,,,S\*4C

表 7-20 GNS 数据结构

| ID   | 字段    | 数据描述                                                  | 符号         |
|------|---------|-----------------------------------------------------------|--------------|
| 1    | \$--GNS | Log 头                                                    |              |
|    2 |    Utc  | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|   3  |   Lat   | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm：分        |   IIII.II    |
| 4    | Lat dir | 纬度方向（N = 北纬，S =南纬）                             | a            |
|   5  |   Lon   | 经度，格式为 dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm：分      |   yyyyy.yy   |
| 6    | Lon dir | 经度方向（E = 东经，W = 西经）                            | a            |

| ID          | 字段           | 数据描述                                                                                                                                                                                                                                     | 符号           |
|-------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
|           7 |           Mode | 模式标识。字符长度可变，前 6 个字符依次为 GPS、GLONASS、Galileo、BDS、 QZSS、NavIC (IRNSS) 卫星系统 每个卫星系统包含以下模式： A = 自主模式 D = 差分模式 F = RTK Float M = 手动输入模式 N = 未定位 P = 高精度模式 R = RTK Int S = 模拟器模式 |           c--c |
| 8           | Use sat        | 使用中的卫星数，00-99                                                                                                                                                                                                                        | xx             |
| 9           | Hdop           | 水平精度因子 HDOP，保留 1 位小数                                                                                                                                                                                                             | x.x            |
|  10         |  Ant alt       | 天线高，单位米，保留 4 位小数。 参考 MSL（大地水准面）                                                                                                                                                                                       |  x.x           |
|   11        |   Geo sep      | 地球椭球面相对大地水准面的高度，单位米。大地水准面高于椭球面为正值，否 则，为负值。保留 4 位小数。                                                                                                                                           |   x.x          |
|  12         |  Age           | 1 差分数据龄期，单位秒，保留 2 位小数。 非差分定位时为空                                                                                                                                                                                     |  x.x           |
| 13          | Station id     | 2 差分基站 ID。非差分定位时为空                                                                                                                                                                                                              | x.x            |
|    14       |    status      | 导航状态指示 S = 安全 C = 注意 U = 危险 V = 导航状态不可用                                                                                                                                                                                   |    a           |

| ID | 字段     | 数据描述   | 符号 |
|----|----------|------------|------|
| 15 | \*xx     | 校验和     | \*hh |
| 16 | [CR][LF] | 语句结束符 |      |

1,2 若 log 头为\$GNGNS 且多个卫星系统为差分模式，差分数据龄期（字段 12）和差分站 ID（字段 13）为空

##### GPGRS 定位解算的卫星残差

本指令用于输出定位解算的卫星的残差，支持 RAIM。

简化ASCII 格式：

GPGRS 1 当前串口输出 1Hz 的 GPGRS 信息 GPGRS COM2 1 在com2 输出 1Hz 的 GPGRS 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGRS,055557.00,0,1.5,0.0,0.4,0.1,0.1,,,,,,,,1,1\*78

\$GNGRS,055557.00,0,,0.2,0.5,0.1,0.2,,,,,,,,1,4\*57

\$GNGRS,055557.00,0,,0.0,,,0.1,,,,,,,,1,8\*5E

\$GNGRS,055557.00,0,0.3,0.1,0.2,0.1,,,,,,,,,3,7\*53

\$GNGRS,055557.00,0,0.1,0.0,0.1,0.1,,,,,,,,,3,1\*55

\$GNGRS,055557.00,0,0.0,0.0,0.0,0.0,,,,,,,,,3,2\*57

\$GNGRS,055557.00,0,0.2,0.5,0.5,0.1,0.4,0.3,0.5,0.2,0.4,0.2,0.2,0.2,4,1\*56

\$GNGRS,055557.00,0,0.4,0.8,1.6,0.6,1.4,,,,,,,,4,1\*75

\$GNGRS,055557.00,0,,,,2.4,,1.5,1.7,1.1,1.7,0.7,1.0,0.6,4,8\*58

\$GNGRS,055557.00,0,1.3,1.2,1.8,,,,,,,,,,4,8\*7C

\$GNGRS,055557.00,0,0.1,0.2,0.2,0.1,0.2,0.0,0.4,0.1,,,,,4,11\*65

\$GNGRS,055557.00,0,0.1,0.6,,,,,,,,,,,5,1\*55

\$GNGRS,055557.00,0,0.1,0.4,,,,,,,,,,,5,6\*50

\$GNGRS,055557.00,0,0.1,0.0,,,,,,,,,,,5,8\*5A

表 7-21 GRS 数据结构

| ID   | 字段          | 数据描述                                                                                                                                  | 符号         |
|------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1    | \$--GRS       | Log 头                                                                                                                                    |              |
|    2 |    Utc        | GGA/GNS UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                                         |    hhmmss.ss |
|    3 |    Mode       | 模式： 0 = 用于计算匹配 GGA /GNS 中给定位置的残差 1 = 在计算 GGA/GNS 位置后重新计算的残 差                                                |    x         |
| 4    |           Res |        参与定位解算的卫星的范围残差，单位米。范围：±999。保留 1 位小数。 如果范围残差超过±99.9，则舍弃小数部分，取整数（如-103.7 取-103） | x.x          |
| 5    |               |                                                                                                                                           | x.x          |
| 6    |               |                                                                                                                                           | x.x          |
| 7    |               |                                                                                                                                           | x.x          |
| 8    |               |                                                                                                                                           | x.x          |
| 9    |               |                                                                                                                                           | x.x          |
| 10   |               |                                                                                                                                           | x.x          |
| 11   |               |                                                                                                                                           | x.x          |
| 12   |               |                                                                                                                                           | x.x          |
| 13   |               |                                                                                                                                           | x.x          |
| 14   |               |                                                                                                                                           | x.x          |
| 15   |               |                                                                                                                                           | x.x          |
| 16   | Sys id        | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                                                         | h            |
| 17   | Signal id     | 信号 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                                                              | h            |
| 18   | \*xx          | 校验和                                                                                                                                    | \*hh         |
| 19   | [CR][LF]      | 语句结束符                                                                                                                                |              |

##### GPGSA 参与定位解算的卫星信息

本指令用于输出接收机工作模式、参与定位解算的卫星及 DOP 等信息。

简化ASCII 格式：

GPGSA 1 当前串口输出 1Hz 的 GPGSA 信息 GPGSA COM2 1 在 com2 输出 1Hz 的 GPGSA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGSA,M,3,03,16,26,29,31,32,,,,,,,1.4,0.7,1.2,1\*34

\$GNGSA,M,3,03,05,24,25,,,,,,,,,1.4,0.7,1.2,3\*39

\$GNGSA,M,3,01,03,04,06,07,09,10,16,21,22,36,39,1.4,0.7,1.2,4\*3D

\$GNGSA,M,3,40,45,59,60,,,,,,,,,1.4,0.7,1.2,4\*36

\$GNGSA,M,3,02,07,,,,,,,,,,,1.4,0.7,1.2,5\*3D

表 7-22 GSA 数据结构

| ID   | 字段        | 数据描述                                                                                    | 符号 |
|------|-------------|---------------------------------------------------------------------------------------------|------|
| 1    | \$--GSA     | Log 头                                                                                      |      |
|   2  |   mode MA   | 卫星工作模式： M = 手动设置 2D/3D 模式 A = 自动切换 2D/3D 模式                              |   a  |
|    3 |    mode 123 | 定位模式： 1 = 未定位 2 = 2D 3 = 3D                                                         |    x |
| 4    |    prn      |   参与定位解算的卫星 ID，详见[表7-36 NMEA 消](#_bookmark184)[息中的卫星 PRN](#_bookmark184) | xx   |
| 5    |             |                                                                                             | xx   |
| 6    |             |                                                                                             | xx   |
| 7    |             |                                                                                             | xx   |

| ID | 字段     | 数据描述                                          | 符号 |
|----|----------|---------------------------------------------------|------|
| 8  |          |                                                   | xx   |
| 9  |          |                                                   | xx   |
| 10 |          |                                                   | xx   |
| 11 |          |                                                   | xx   |
| 12 |          |                                                   | xx   |
| 13 |          |                                                   | xx   |
| 14 |          |                                                   | xx   |
| 15 |          |                                                   | xx   |
| 16 | pdop     | PDOP，保留 1 位小数                               | x.x  |
| 17 | hdop     | HDOP，保留 1 位小数                               | x.x  |
| 18 | vdop     | VDOP，保留 1 位小数                               | x.x  |
| 19 | SysID    | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181) | h    |
| 20 | \*xx     | 校验和                                            | \*hh |
| 21 | [CR][LF] | 语句结束符                                        |      |

##### GPGST 伪距观测误差信息

本指令用于输出伪距误差信息。

简化ASCII 格式：

GPGST 1 当前串口输出 1Hz 的 GPGST 信息 GPGST COM2 1 在com2 输出 1Hz 的 GPGST 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNGST,060458.00,0.71,1.62,1.44,9.1113,1.618,1.441,3.761\*42

表 7-23 GST 数据结构

| ID   | 字段     | 数据描述                                                  | 符号         |
|------|----------|-----------------------------------------------------------|--------------|
| 1    | \$--GST  | Log 头                                                    |              |
|    2 |    utc   | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|  3   |  rms     | 伪距、DGNSS 改正数标准差（RMS 值），保留 2 位 小数        |  x.x         |
| 4    | smjr std | 误差椭圆长半轴的标准差，单位米，保留 2 位小数             | x.x          |
| 5    | smnr std | 误差椭圆短半轴的标准差，单位米，保留 2 位小数             | x.x          |
| 6    | orient   | 误差椭圆长半轴方向，与真北夹角，保留 4 位小数             | x.x          |
| 7    | lat std  | 纬度误差标准差，单位米，保留 3 位小数                     | x.x          |
| 8    | lon std  | 经度误差标准差，单位米，保留 3 位小数                     | x.x          |
| 9    | alt std  | 高程误差标准差，单位米，保留 3 位小数                     | x.x          |
| 10   | \*xx     | 校验和                                                    | \*hh         |
| 11   | [CR][LF] | 语句结束符                                                |              |

##### GPGSV 可视卫星信息

本指令用于输出可视卫星数量、ID 等信息。

简化ASCII 格式：

GPGSV 1 当前串口输出 1Hz 的 GPGSV 信息 GPGSV COM2 1 在 com2 输出 1Hz 的 GPGSV 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GPGSV,2,1,08,03,29,287,33,04,14,313,23,32,37,141,44,31,65,039,46,1\*63

\$GPGSV,2,2,08,25,14,047,30,29,28,068,39,26,72,222,48,16,31,218,36,1\*6F

\$GPGSV,2,1,08,03,29,287,34,04,14,313,29,32,37,141,40,31,65,039,43,4\*6A

\$GPGSV,2,2,08,25,14,047,30,29,28,068,33,26,72,222,44,16,31,218,29,4\*62

\$GPGSV,2,1,05,03,29,287,41,04,14,313,31,32,37,141,46,25,14,047,37,8\*6F

\$GPGSV,2,2,05,26,72,222,51,8\*5F

\$GLGSV,2,1,05,71,21,169,38,65,47,313,38,73,17,049,36,74,57,013,45,1\*7C

\$GLGSV,2,2,05,72,65,211,47,1\*4A

\$GLGSV,1,1,04,71,21,169,40,65,47,313,35,73,17,049,37,72,65,211,45,3\*78

\$GBGSV,6,1,22,36,65,034,48,19,14,172,33,39,74,101,49,29,04,152,31,1\*7A

\$GBGSV,6,2,22,30,19,103,38,10,34,206,36,27,11,053,31,01,34,140,39,1\*7F

\$GBGSV,6,3,22,07,44,200,39,16,79,073,48,22,51,219,46,09,73,329,44,1\*74

\$GBGSV,6,4,22,59,38,145,43,03,41,188,39,04,25,124,35,40,53,185,45,1\*74

\$GBGSV,6,5,22,45,48,272,43,60,28,227,34,02,32,224,32,46,18,064,32,1\*7A

\$GBGSV,6,6,22,21,38,299,37,06,82,023,46,1\*77

\$GBGSV,5,1,19,36,65,034,34,19,14,172,26,39,74,101,35,29,04,152,26,8\*7A

\$GBGSV,5,2,19,30,19,103,26,10,34,206,26,01,34,140,27,07,44,200,29,8\*73

\$GBGSV,5,3,19,16,79,073,30,22,51,219,32,09,73,329,28,59,38,145,32,8\*79

\$GBGSV,5,4,19,04,25,124,21,40,53,185,33,45,48,272,30,60,28,227,27,8\*78

\$GBGSV,5,5,19,46,18,064,23,21,38,299,25,06,82,023,31,8\*4D

\$GBGSV,3,1,10,10,34,206,41,01,34,140,45,07,44,200,44,16,79,073,50,B\*0E

\$GBGSV,3,2,10,09,73,329,48,03,41,188,44,04,25,124,42,02,32,224,41,B\*0B

\$GBGSV,3,3,10,05,16,247,38,06,82,023,49,B\*0C

\$GAGSV,2,1,08,05,61,163,49,09,12,145,31,03,57,301,44,08,07,318,30,1\*78

\$GAGSV,2,2,08,31,04,049,30,02,17,232,39,24,51,046,45,25,68,240,48,1\*7A

\$GAGSV,2,1,08,05,61,163,51,09,12,145,33,03,57,301,48,08,07,318,34,2\*78

\$GAGSV,2,2,08,31,04,049,32,02,17,232,40,24,51,046,48,25,68,240,50,2\*71

\$GAGSV,2,1,07,05,61,163,48,09,12,145,27,03,57,301,42,31,04,049,26,7\*78

\$GAGSV,2,2,07,02,17,232,31,24,51,046,43,25,68,240,46,7\*4B

\$GQGSV,1,1,03,02,71,088,46,07,42,163,36,03,14,145,30,1\*55

\$GQGSV,1,1,03,02,71,088,45,07,42,163,40,03,14,145,28,6\*59

\$GQGSV,1,1,03,02,71,088,50,07,42,163,47,03,14,145,33,8\*5E

表 7-24 GSV 数据结构

| ID | 字段           | 数据描述                                                                                                                                     | 符号 |
|----|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|------|
| 1  | \$--GSV        | Log 头                                                                                                                                       |      |
| 2  | \# msgs        | GSV 消息总数，最小值 1                                                                                                                       | x    |
| 3  | msg \#         | GSV 消息编号，最小值 1                                                                                                                       | x    |
| 4  | \# sats        | 可视卫星数量                                                                                                                                 | xx   |
| 5  | Sat id         | 卫星 ID，详见[表7-36 NMEA 消息中的卫星 PRN](#_bookmark184)                                                                                   | xx   |
| 6  | Elevation      | 高度角，单位为度，整数，最大值 90                                                                                                            | xx   |
| 7  | Azi            | 方位角，与真北夹角，000\~359 之间的整数                                                                                                      | xxx  |
| 8  | CN0            | 载噪比（C/N0），0 \~ 99 dB-Hz，整数，不跟踪时为空                                                                                            | xx   |
| 9  |       Next sat |  第 2-3 位 SV，“卫星 ID-高度角-方位角-SNR”的集 和，字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。 | xx   |
| 10 |                |                                                                                                                                              | xx   |
| 11 |                |                                                                                                                                              | xxx  |
| 12 |                |                                                                                                                                              | xx   |
| 13 |                |  第 4 位 SV，“卫星 ID-高度角-方位角-SNR”的集和，字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。    | xx   |
| 14 |                |                                                                                                                                              | xx   |
| 15 |                |                                                                                                                                              | xxx  |
| 16 |                |                                                                                                                                              | xx   |
| 17 | SysID          | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                                                            | h    |
| 18 | \*xx           | 校验和                                                                                                                                       | \*hh |
| 19 | [CR][LF]       | 语句结束符                                                                                                                                   |      |

##### GPTHS 航向信息

本指令用于输出航向、状态等信息。

简化ASCII 格式：

GPTHS 1 当前串口输出 1Hz 的 GPTHS 信息 GPTHS COM2 1 在com2 输出 1Hz 的 GPTHS 信息

适用产品：UM982、UMD982

消息输出：

\$GNTHS,341.3065,A\*1F

表 7-25 THS 数据结构

| ID   | 字段     | 数据描述                                                   | 符号 |
|------|----------|------------------------------------------------------------|------|
| 1    | \$--THS  | Log 头                                                     |      |
| 2    | Heading  | 航向，单位为度，保留 4 位小数                              | x.x  |
|    3 |    Mode  | 模式： A = 自主定位 M = 手动输入 S = 模拟器 V = 数据不可用 |    a |
| 4    | \*xx     | 校验和                                                     | \*hh |
| 5    | [CR][LF] | 语句结束符                                                 |      |

##### GPRMC 卫星定位信息

本指令用于输出时间、日期、位置、速度等信息。

简化ASCII 格式：

GPRMC 1 当前串口输出 1Hz 的 GPRMC 信息 GPRMC COM2 1 在com2 输出 1Hz 的 GPRMC 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNRMC,061402.00,A,4004.73846648,N,11614.19829285,E,0.003,12.5,301221,6.9,

W,A,V\*78

表 7-26 RMC 数据结构

| ID   | 字段         | 数据描述                                                  | 符号         |
|------|--------------|-----------------------------------------------------------|--------------|
| 1    | \$--RMC      | Log 头                                                    |              |
|    2 |    utc       | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|   3  |   pos status | 状态： A = 数据可用 V = 导航接收机警告                    |   A          |
|   4  |   lat        | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分       |   llll.ll    |
| 5    | lat dir      | 纬度方向（N = 北纬，S =南纬）                             | a            |
|   6  |   lon        | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分      |   yyyyy.yy   |
| 7    | lon dir      | 经度方向（E = 东经，W = 西经）                            | a            |
| 8    | speed Kn     | 地面速率，单位为节，保留 3 位小数                         | x.x          |
|  9   |  track true  | 地面航向，单位为度，从北向起顺时针计算，保留 1 位小数     |  x.x         |
| 10   | date         | 日期：ddmmyy                                              | xxxxxx       |
| 11   | mag var      | 磁偏角，单位：度，保留 1 位小数                           | x.x          |
| 12   | var dir      | 磁偏角方向                                                | a            |

| ID         | 字段             | 数据描述                                                                                                                                       | 符号      |
|------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
|         13 |         mode ind | 模式： A=自主模式 D = 差分模式 F = RTK Float M = 手动输入模式 N = 无定位 P = 高精度模式 R = RTK Int S = 模拟器模式 V = 模式无效（不包括 A, D） |         a |
|    14      |    mode status   | 定位状态： S = 安全 C = 注意 U = 危险 V = 定位状态不可用                                                                                       |    a      |
| 15         | \*xx             | 校验和                                                                                                                                         | \*hh      |
| 16         | [CR][LF]         | 语句结束符                                                                                                                                     |           |

##### GPROT 旋转速度和方向信息

本指令用于输出旋转速度和方向信息。

简化ASCII 格式：

GPROT 1 当前串口输出 1Hz 的 GPROT 信息 GPROT COM2 1 在 com2 输出 1Hz 的 GPROT 信息

适用产品：UM982、UMD982

消息输出：

\$GNROT,0.0,V\*38

表 7-27 ROT 数据结构

| ID  | 字段     | 数据描述                             | 符号 |
|-----|----------|--------------------------------------|------|
| 1   | \$--ROT  | Log 头                               |      |
| 2   | rate     | 旋转速率，单位：度/分，保留 1 位小数 | x.x  |
|   3 |   status | 状态： A = 数据可用 V = 数据无效     |   A  |
| 4   | \*xx     | 校验和                               | \*hh |
| 5   | [CR][LF] | 语句结束符                           |      |

##### GPVTG 地面航向与速度信息

本指令用于输出地面航向、速度等信息。

简化ASCII 格式：

GPVTG 1 当前串口输出 1Hz 的 GPVTG 信息 GPVTG COM2 1 在 com2 输出 1Hz 的 GPVTG 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNVTG,123.119,T,130.046,M,0.00444,N,0.00822,K,A\*38

表 7-28 VTG 数据结构

| ID | 字段         | 数据描述                                      | 符号 |
|----|--------------|-----------------------------------------------|------|
| 1  | \$--VTG      | Log 头                                        |      |
|  2 |  Course true | 地面航向，单位为度，相对于真北，保留 3 位小数 |  x.x |
| 3  | Course ind   | 航向标志，固定填 T                            | T    |
|  4 |  Course mag  | 地面航向，单位为度，相对于磁北，保留 3 位小数 |  x.x |

| ID      | 字段          | 数据描述                                                                                     | 符号        |
|---------|---------------|----------------------------------------------------------------------------------------------|-------------|
| 5       | Course ind    | 航向标志，固定填 M                                                                           | M           |
| 6       | speed Kn      | 地面速率，单位为节，保留 5 位小数                                                            | x.x         |
| 7       | N             | 速率单位，固定填 N                                                                           | N           |
| 8       | speed Km      | 地面速率，单位为 km/h，保留 5 位小数                                                         | x.x         |
| 9       | K             | 速率单位，固定填 K                                                                           | K           |
|      10 |      Mode ind | 模式： A=自主模式 D = 差分模式 M = 手动输入模式 N = 数据不可用 P = 高精度模式 S = 模拟器模式 |      xxxxxx |
| 11      | \*xx          | 校验和                                                                                       | \*hh        |
| 12      | [CR][LF]      | 语句结束符                                                                                   |             |

##### GPZDA 日期与时间

本指令用于输出UTC 时间和日期信息。

简化ASCII 格式：

GPZDA 1 当前串口输出 1Hz 的 GPZDA 信息 GPZDA COM2 1 在com2 输出 1Hz 的 GPZDA 信息

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\$GNZDA,061555.00,30,12,2021,,\*7B

表 7-29 ZDA 数据结构

| ID   | 字段              | 数据描述                                                  | 符号         |
|------|-------------------|-----------------------------------------------------------|--------------|
| 1    | \$--ZDA           | Log 头                                                    |              |
|    2 |    Utc            | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
| 3    | Day               | UTC 日，01\~31                                            | xx           |
| 4    | Month             | UTC 月，01\~12                                            | xx           |
| 5    | Year              | UTC 年                                                    | xxxx         |
| 6    | Local zone hour   | 本地时区的小时，00\~±13                                   | xx           |
| 7    | Local zone minute | 本地时区的分钟，00\~±59                                   | xx           |
| 8    | \*xx              | 校验和                                                    | \*hh         |
| 9    | [CR][LF]          | 语句结束符                                                |              |

### Unicore 扩展的 NMEA 数据输出指令

#### GPGGAH 从天线计算的卫星定位信息

本指令用于输出从天线计算的卫星系统定位数据。

简化ASCII 格式：

GPGGAH 1 当前串口输出 1Hz 的 GPGGAH 信息 GPGGAH COM2 1 在 com2 输出 1Hz 的 GPGGAH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGGAH,073346.00,4004.73874301,N,11614.19077585,E,1,28,0.6,64.2831,M,- 8.4925,M,,\*18

表 7-30 GGAH 数据结构

| ID        | 字段         | 数据描述                                                                                                                                        | 符号         |
|-----------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1         | \$--GGAH     | Log 头                                                                                                                                          |              |
|    2      |    utc       | 位置对应的 UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                                            |    hhmmss.ss |
|   3       |   lat        | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分                                                                                             |   IIII.II    |
| 4         | lat dir      | 纬度方向（N = 北纬，S =南纬）                                                                                                                   | a            |
|   5       |   lon        | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                                                                                            |   yyyyy.yy   |
| 6         | lon dir      | 经度方向（E = 东经，W = 西经）                                                                                                                  | a            |
|         7 |         qual | GPS 状态 0 = 定位不可用或无效 1 = 单点定位 2 = 差分定位 3 = GPS PPS 模式 4 = RTK Int 5 = RTK Float 6 = 惯导模式 7 = 手动输入模式 8 = 模拟器模式 |         x    |
| 8         | \# sats      | 使用中的卫星数。可能与所见数不一致                                                                                                              | xx           |
| 9         | hdop         | 水平精度因子，保留 1 位小数                                                                                                                     | x.x          |

| ID   | 字段         | 数据描述                                                                                       | 符号  |
|------|--------------|------------------------------------------------------------------------------------------------|-------|
|  10  |  alt         | 海拔高度，参考 MSL（大地水准面），保 留 4 位小数                                               |  x.x  |
| 11   | a-units      | 海拔高度单位（M = m）                                                                          | M     |
|   12 |   undulation | 地球椭球面相对大地水准面的高度。大地水准面高于椭球面为正值，否则，为负 值。保留 4 位小数。     |   x.x |
|  13  |  u-units     | 地球椭球面相对大地水准面的高度单位（M = m）                                                    |  M    |
|   14 |   age        | 差分数据龄期，指最近使用的差分改正数 的平均龄期，单位秒，保留 2 位小数。不是差分定位时，为空。 |   x.x |
| 15   | stn ID       | 差分基站 ID，0000-1023                                                                         | xxxx  |
| 16   | \*xx         | 校验和                                                                                         | \*hh  |
| 17   | [CR][LF]     | 语句结束符                                                                                     |       |

#### GPGLLH 从天线计算的地理位置信息

本指令用于输出从天线计算的地理位置经度/纬度信息。

简化ASCII 格式：

GPGLLH 1 当前串口输出 1Hz 的 GPGLLH 信息 GPGLLH COM2 1 在com2 输出 1Hz 的 GPGLLH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGLLH,4004.73814597,N,11614.19908275,E,054501.00,A,D\*37

表 7-31 GLLH 数据结构

| ID | 字段     | 数据描述 | 符号 |
|----|----------|----------|------|
| 1  | \$--GLLH | Log 头   |      |

| ID     | 字段          | 数据描述                                                                                 | 符号        |
|--------|---------------|------------------------------------------------------------------------------------------|-------------|
|   2    |   lat         | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分                                      |   IIII.II   |
| 3      | lat dir       | 纬度方向（N = 北纬，S =南纬）                                                            | a           |
|   4    |   lon         | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                                     |   yyyyy.yy  |
| 5      | lon dir       | 经度方向（E = 东经，W = 西经）                                                           | a           |
|    6   |    Utc        | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                |   hhmmss.ss |
|    7   |    status     | 状态： V = 数据无效 A = 自适应 D = 差分                                                  |    A        |
|      8 |      mode ind | 定位系统模式： N = 未定位 A = 自主定位 D = 差分定位 E = 惯导模式 M = 手动输入 S = 模拟器 |      a      |
| 9      | \*xx          | 校验和                                                                                   | \*hh        |
| 10     | [CR][LF]      | 语句结束符                                                                               |             |

#### GPGNSH 从天线计算的定位数据输出

本指令用于输出从天线计算的 GNSS 定位数据。

简化ASCII 格式：

GPGNSH 1 当前串口输出 1Hz 的 GPGNSH 信息 GPGNSH COM2 1 在com2 输出 1Hz 的 GPGNSH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGNSH,074444.00,4004.73864213,N,11614.19082153,E,ANAAA,28,0.7,64.6536,- 8.4925,,,S\*08

表 7-32 GNSH 数据结构

| ID   | 字段     | 数据描述                                                  | 符号         |
|------|----------|-----------------------------------------------------------|--------------|
| 1    | \$--GNSH | Log 头                                                    |              |
|    2 |    utc   | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|   3  |   Lat    | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分       |   IIII.II    |
| 4    | Lat dir  | 纬度方向（N = 北纬，S =南纬）                             | a            |
|   5  |   Lon    | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分      |   yyyyy.yy   |
| 6    | Lon dir  | 经度方向（E = 东经，W = 西经）                            | a            |

| ID          | 字段           | 数据描述                                                                                                                                                                                                                      | 符号           |
|-------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
|           7 |           mode | 模式标识。字符长度可变，前 3 个字符依次为 GPS、GLONASS、Galileo 卫星系统每个卫星系统包含以下模式： A = 自主模式 D = 差分模式 E = 惯导模式 F = RTK Float M = 手动输入模式 N = 未定位 P = 高精度模式 R = RTK Int S = 模拟器模式 |           c--c |
| 8           | Use sat        | 使用中的卫星数，00-99                                                                                                                                                                                                         | xx             |
| 9           | Hdop           | 水平精度因子 HDOP，保留 1 位小数                                                                                                                                                                                              | x.x            |
|  10         |  Ant alt       | 天线高，单位米，保留 4 位小数， 参考 MSL（大地水准面）                                                                                                                                                                        |  x.x           |
|   11        |   Geo sep      | 地球椭球面相对大地水准面的高度，单位米。大地水准面高于椭球面为正值，否 则，为负值。保留 4 位小数。                                                                                                                            |   x.x          |
|  12         |  Age           | 1 差分数据龄期，单位秒，保留 2 位小数。 非差分定位时为空                                                                                                                                                                      |  x.x           |
| 13          | Station id     | 2 差分基站 ID。非差分定位时为空                                                                                                                                                                                               | x.x            |
|    14       |    status      | 导航状态指示 S = 安全 C = 注意 U = 危险 V = 导航状态不可用                                                                                                                                                                    |    a           |

| ID | 字段     | 数据描述   | 符号 |
|----|----------|------------|------|
| 15 | \*xx     | 校验和     | \*hh |
| 16 | [CR][LF] | 语句结束符 |      |

1,2 若 log 头为\$GNGNS 且多个卫星系统为差分模式，差分数据龄期（字段 12）和差分站 ID（字段 13）为空

#### GPGRSH 从天线定位解算的卫星残差

本指令用于输出从天线定位解算的卫星的残差，支持 RAIM。

简化ASCII 格式：

GPGRSH 1 当前串口输出 1Hz 的 GPGRSH 信息 GPGRSH COM2 1 在com2 输出 1Hz 的 GPGRSH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGRSH,055209.00,0,0.0,0.8,0.1,,0.1,2.2,0.2,,,,,,1,1\*18

\$GNGRSH,055209.00,0,0.1,0.4,0.1,,0.1,1.5,0.2,,,,,,1,4\*14

\$GNGRSH,055209.00,0,0.0,0.2,,,0.0,0.1,,,,,,,1,8\*18

\$GNGRSH,055209.00,0,0.1,0.4,0.1,0.1,,,,,,,,,2,1\*14

\$GNGRSH,055209.00,0,0.1,0.1,0.1,0.3,,,,,,,,,2,3\*11

\$GNGRSH,055209.00,0,0.6,0.7,0.3,0.8,0.1,0.1,,,,,,,3,7\*1C

\$GNGRSH,055209.00,0,0.2,0.2,0.1,0.2,0.0,0.0,,,,,,,3,1\*13

\$GNGRSH,055209.00,0,0.1,0.1,0.1,0.1,0.0,0.0,,,,,,,3,2\*13

\$GNGRSH,055209.00,0,0.3,0.2,0.6,0.1,0.4,0.8,1.2,0.9,0.4,0.4,1.0,2.0,4,1\*14

\$GNGRSH,055209.00,0,0.9,0.6,0.6,0.4,0.3,0.2,0.8,1.3,0.2,,,,4,1\*3D

\$GNGRSH,055209.00,0,0.2,0.1,0.1,0.1,0.1,0.2,0.2,0.2,0.1,0.1,0.2,0.2,4,8\*1E

\$GNGRSH,055209.00,0,0.2,0.2,0.2,0.1,0.1,0.1,0.2,0.2,0.1,,,,4,8\*32

\$GNGRSH,055209.00,0,,,0.1,0.0,,0.2,,,,,,,4,11\*0B

\$GNGRSH,055209.00,0,0.2,0.1,0.1,,,0.1,0.2,,0.1,,,,4,11\*26

\$GNGRSH,055209.00,0,0.3,0.2,0.1,,,,,,,,,,5,1\*38

\$GNGRSH,055209.00,0,1.2,0.4,0.1,,,,,,,,,,5,6\*39

\$GNGRSH,055209.00,0,0.2,0.0,0.1,,,,,,,,,,5,8\*32

表 7-33 GRSH 数据结构

| ID   | 字段          | 数据描述                                                                                                                                  | 符号         |
|------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1    | \$--GRSH      | Log 头                                                                                                                                    |              |
|    2 |    Utc        | GGA/GNS UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                                         |    hhmmss.ss |
|    3 |    Mode       | 模式： 0 = 用于计算匹配 GGA /GNS 中给定位置的残差 1 = 在计算 GGA/GNS 位置后重新计算的残 差                                                |    x         |
| 4    |           Res |        参与定位解算的卫星的范围残差，单位米。范围：±999。保留 1 位小数。 如果范围残差超过±99.9，则舍弃小数部分，取整数（如-103.7 取-103） | x.x          |
| 5    |               |                                                                                                                                           | x.x          |
| 6    |               |                                                                                                                                           | x.x          |
| 7    |               |                                                                                                                                           | x.x          |
| 8    |               |                                                                                                                                           | x.x          |
| 9    |               |                                                                                                                                           | x.x          |
| 10   |               |                                                                                                                                           | x.x          |
| 11   |               |                                                                                                                                           | x.x          |
| 12   |               |                                                                                                                                           | x.x          |
| 13   |               |                                                                                                                                           | x.x          |
| 14   |               |                                                                                                                                           | x.x          |
| 15   |               |                                                                                                                                           | x.x          |
| 16   | Sys id        | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                                                         | h            |

| ID | 字段      | 数据描述                                     | 符号 |
|----|-----------|----------------------------------------------|------|
| 17 | Signal id | 信号 ID。参考[表7-34 GNSS ID](#_bookmark181) | h    |
| 18 | \*xx      | 校验和                                       | \*hh |
| 19 | [CR][LF]  | 语句结束符                                   |      |

表 7-34 GNSS ID

| GNSS 系统   | 系统 ID        | 信号 ID | 信号通道         |
|-------------|----------------|---------|------------------|
|         GPS |         1 (GP) | 0       | All signals      |
|             |                | 1       | L1 C/A           |
|             |                | 2       | L1 P(Y)          |
|             |                | 3       | L1 M             |
|             |                | 4       | L2 P(Y)          |
|             |                | 5       | L2C-M            |
|             |                | 6       | L2C-L            |
|             |                | 7       | L5-I             |
|             |                | 8       | L5-Q             |
|             |                | 9-F     | Reserved         |
|     GLONASS |     2 (GL)     | 0       | All signals      |
|             |                | 1       | G1 C/A           |
|             |                | 2       | G1 P             |
|             |                | 3       | G2 C/A           |
|             |                | 4       | GLONASS (M) G2 P |
|             |                | 5-F     | Reserved         |
|     Galileo |     3 (GA)     | 0       | All signals      |
|             |                | 1       | E5a              |
|             |                | 2       | E5b              |
|             |                | 3       | E5 a+b           |
|             |                | 4       | E6-A             |
|             |                | 5       | E6-BC            |

| GNSS 系统       | 系统 ID            | 信号 ID | 信号通道    |
|-----------------|--------------------|---------|-------------|
|                 |                    | 6       | L1-A        |
|                 |                    | 7       | L1-BC       |
|                 |                    | 8-F     | Reserved    |
|             BDS |             4 (GB) | 0       | All signals |
|                 |                    | 1       | B1I         |
|                 |                    | 2       | B1Q         |
|                 |                    | 3       | B1C         |
|                 |                    | 4       | B1A         |
|                 |                    | 5       | B2-a        |
|                 |                    | 6       | B2-b        |
|                 |                    | 7       | B2 a+b      |
|                 |                    | 8       | B3I         |
|                 |                    | 9       | B3Q         |
|                 |                    | A       | B3A         |
|                 |                    | B       | B2I         |
|                 |                    | C       | B2Q         |
|                 |                    | D-F     | Reserved    |
|         QZSS    |         5 (GQ)     | 0       | All signals |
|                 |                    | 1       | L1 C/A      |
|                 |                    | 2       | L1C (D)     |
|                 |                    | 3       | L1C (P)     |
|                 |                    | 4       | LIS         |
|                 |                    | 5       | L2C-M       |
|                 |                    | 6       | L2C-L       |
|                 |                    | 7       | L5-I        |
|                 |                    | 8       | L5-Q        |
|                 |                    | 9       | L6D         |

| GNSS 系统          | 系统 ID     | 信号 ID | 信号通道    |
|--------------------|-------------|---------|-------------|
|                    |             | A       | L6E         |
|                    |             | B-F     | Reserved    |
|      NavIC (IRNSS) |      6 (GI) | 0       | All signals |
|                    |             | 1       | L5-SPS      |
|                    |             | 2       | S-SPS       |
|                    |             | 3       | L5-RS       |
|                    |             | 4       | S-RS        |
|                    |             | 5       | L1-SPS      |
|                    |             | 6-F     | Reserved    |
| RESERVED           | 7 to F      |         |             |

#### GPGSAH 从天线参与定位解算的卫星信息

本指令用于输出接收机工作模式、从天线参与定位解算的卫星及 DOP 等信息。

简化ASCII 格式：

GPGSAH 1 当前串口输出 1Hz 的 GPGSAH 信息 GPGSAH COM2 1 在 com2 输出 1Hz 的 GPGSAH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGSAH,M,3,26,29,31,32,,,,,,,,,1.1,0.6,0.9,1\*76

\$GNGSAH,M,3,01,04,09,19,21,31,,,,,,,1.1,0.6,0.9,3\*7D

\$GNGSAH,M,3,01,03,04,06,07,09,16,19,20,22,28,36,1.1,0.6,0.9,4\*73

\$GNGSAH,M,3,37,39,40,46,59,60,,,,,,,1.1,0.6,0.9,4\*7D

表 7-35 GSAH 数据结构

| ID | 字段     | 数据描述 | 符号 |
|----|----------|----------|------|
| 1  | \$--GSAH | Log 头   |      |

| ID   | 字段          | 数据描述                                                                                           | 符号 |
|------|---------------|----------------------------------------------------------------------------------------------------|------|
|   2  |   mode MA     | 卫星工作模式： M = 手动设置 2D/3D 模式 A = 自动切换 2D/3D 模式                                     |   a  |
|    3 |    mode 123   | 定位模式： 1 = 未定位 2 = 2D 3 = 3D                                                                |    x |
| 4    |           prn |          参与定位解算的卫星 ID，详见[表7-36 NMEA 消](#_bookmark184)[息中的卫星 PRN](#_bookmark184) | xx   |
| 5    |               |                                                                                                    | xx   |
| 6    |               |                                                                                                    | xx   |
| 7    |               |                                                                                                    | xx   |
| 8    |               |                                                                                                    | xx   |
| 9    |               |                                                                                                    | xx   |
| 10   |               |                                                                                                    | xx   |
| 11   |               |                                                                                                    | xx   |
| 12   |               |                                                                                                    | xx   |
| 13   |               |                                                                                                    | xx   |
| 14   |               |                                                                                                    | xx   |
| 15   |               |                                                                                                    | xx   |
| 16   | pdop          | PDOP，保留 1 位小数                                                                                | x.x  |
| 17   | hdop          | HDOP，保留 1 位小数                                                                                | x.x  |
| 18   | vdop          | VDOP，保留 1 位小数                                                                                | x.x  |
| 19   | SysID         | GNSS 系统 ID。参考[表7-34 GNSS ID](#_bookmark181)                                                  | h    |
| 20   | \*xx          | 校验和                                                                                             | \*hh |
| 21   | [CR][LF]      | 语句结束符                                                                                         |      |

表 7-36 NMEA 消息中的卫星 PRN

| 卫星导航系统    | 星基增强系统     |
|-----------------|------------------|
| GPS: 1\~32      | WAAS 33\~64      |
| BDS：1\~64      | BDSBAS 65\~75    |
| GLONASS: 65\~96 | SDCM 33\~64      |
| Galileo：1\~36  | EGNOS 37\~64     |
| QZSS：1\~10     | QZSS-SAIF 55\~63 |
| IRNSS：1\~15    | GAGAN 33\~64     |
| —               | KASS 47          |

#### GPGSTH 从天线计算的伪距观测误差信息

本指令用于输出从天线计算的伪距误差信息。

简化ASCII 格式：

GPGSTH 1 当前串口输出 1Hz 的 GPGSTH 信息 GPGSTH COM2 1 在com2 输出 1Hz 的 GPGSTH 信息

适用产品：UM982、UMD982

消息输出：

\$GNGSTH,055543.00,0.45,0.01,0.01,127.6430,0.010,0.010,0.019\*0F

表 7-37 GSTH 数据结构

| ID   | 字段     | 数据描述                                                          | 符号         |
|------|----------|-------------------------------------------------------------------|--------------|
| 1    | \$--GSTH | Log 头                                                            |              |
|    2 |    utc   | GGA/GNS UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
|  3   |  rms     | 伪距、DGNSS 改正数标准差（RMS 值），保留 2 位 小数                |  x.x         |

| ID | 字段     | 数据描述                                      | 符号 |
|----|----------|-----------------------------------------------|------|
| 4  | smjr std | 误差椭圆长半轴的标准差，单位米，保留 2 位小数 | x.x  |
| 5  | smnr std | 误差椭圆短半轴的标准差，单位米，保留 2 位小数 | x.x  |
| 6  | orient   | 误差椭圆长半轴方向，与真北夹角，保留 4 位小数 | x.x  |
| 7  | lat std  | 纬度误差标准差，单位米，保留 3 位小数         | x.x  |
| 8  | lon std  | 经度误差标准差，单位米，保留 3 位小数         | x.x  |
| 9  | alt std  | 高程误差标准差，单位米，保留 3 位小数         | x.x  |
| 10 | \*xx     | 校验和                                        | \*hh |
| 11 | [CR][LF] | 语句结束符                                    |      |

#### GPGSVH 从天线的可视卫星信息输出

本指令用于输出从天线的可视卫星数量、ID 等信息。

简化ASCII 格式：

GPGSVH 1 当前串口输出 1Hz 的 GPGSVH 信息 GPGSVH COM2 1 在 com2 输出 1Hz 的 GPGSVH 信息

适用产品：UM982、UMD982

消息输出：

\$GPGSVH,2,1,08,16,28,217,38,32,39,140,45,03,29,290,32,31,66,033,50,1\*2F

\$GPGSVH,2,2,08,04,12,313,34,26,69,220,46,25,16,046,34,29,28,071,37,1\*2A

\$GPGSVH,2,1,07,32,39,140,41,03,29,290,37,31,66,033,46,04,12,313,35,4\*21

\$GPGSVH,2,2,07,26,69,220,46,25,16,046,35,29,28,071,41,4\*11

\$GLGSVH,2,1,05,74,15,049,37,66,38,321,45,76,41,264,42,72,21,168,35,1\*3F

\$GLGSVH,2,2,05,65,63,206,44,1\*07

\$GLGSVH,1,1,04,66,38,321,42,76,41,264,43,72,21,168,36,65,63,206,43,3\*31

\$GBGSVH,6,1,21,27,15,113,36,46,73,006,50,06,81,019,49,07,43,199,36,1\*36

\$GBGSVH,6,2,21,16,79,068,51,19,55,235,42,10,33,205,34,28,13,062,34,1\*3A

\$GBGSVH,6,3,21,36,40,265,35,59,38,145,43,40,52,184,43,20,24,178,35,1\*3B

\$GBGSVH,6,4,21,22,31,308,40,04,25,124,36,03,42,188,35,01,34,140,41,1\*37

\$GBGSVH,6,5,21,60,28,227,38,39,74,097,51,09,72,329,46,02,32,224,35,1\*3A

\$GBGSVH,6,6,21,37,24,062,35,1\*0D

\$GBGSVH,6,1,21,27,15,113,39,46,73,006,52,06,81,019,49,07,43,199,41,8\*32

\$GBGSVH,6,2,21,16,79,068,48,19,55,235,47,10,33,205,36,28,13,062,39,8\*31

\$GBGSVH,6,3,21,36,40,265,45,59,38,145,43,40,52,184,46,20,24,178,37,8\*32

\$GBGSVH,6,4,21,22,31,308,41,04,25,124,37,03,42,188,38,01,34,140,39,8\*3C

\$GBGSVH,6,5,21,60,28,227,40,39,74,097,53,09,72,329,47,02,32,224,35,8\*3F

\$GBGSVH,6,6,21,37,24,062,44,8\*02

\$GBGSVH,3,1,09,06,81,019,50,07,43,199,43,16,79,068,50,10,33,205,40,B\*42

\$GBGSVH,3,2,09,04,25,124,40,03,42,188,42,01,34,140,40,09,72,329,49,B\*49

\$GBGSVH,3,3,09,02,32,224,39,B\*79

\$GAGSVH,2,1,06,19,27,146,38,04,79,220,51,09,34,312,39,31,44,232,43,2\*32

\$GAGSVH,2,2,06,21,25,048,44,01,76,038,52,2\*3C

\$GAGSVH,2,1,06,19,27,146,34,04,79,220,48,09,34,312,40,31,44,232,38,7\*31

\$GAGSVH,2,2,06,21,25,048,36,01,76,038,50,7\*3E

\$GQGSVH,1,1,03,03,13,146,35,02,71,090,49,07,42,163,35,1\*19

\$GQGSVH,1,1,03,03,13,146,32,02,71,090,49,07,42,163,42,6\*19

表 7-38 GSVH 数据结构

| ID | 字段      | 数据描述                                                   | 符号 |
|----|-----------|------------------------------------------------------------|------|
| 1  | \$--GSVH  | Log 头                                                     |      |
| 2  | \# msgs   | GSV 消息总数，1\~9                                         | x    |
| 3  | msg \#    | GSV 消息编号，1\~9                                         | x    |
| 4  | \# sats   | 可视卫星数量                                               | xx   |
| 5  | Sat id    | 卫星 ID，详见[表7-36 NMEA 消息中的卫星 PRN](#_bookmark184) | xx   |
| 6  | Elevation | 高度角，单位为度，整数，最大值 90                          | xx   |
| 7  | Azi       | 方位角，与真北夹角，000\~359 之间的整数                    | xxx  |
| 8  | CN0       | 载噪比（C/N0），0 \~ 99 dB-Hz，整数，不跟踪时为空          | xx   |

| ID  | 字段               | 数据描述                                                                                                                                     | 符号 |
|-----|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|------|
| 9   |       Next sat     |  第 2-3 位 SV，“卫星 ID-高度角-方位角-SNR”的集 和，字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。 | xx   |
| 10  |                    |                                                                                                                                              | xx   |
| 11  |                    |                                                                                                                                              | xxx  |
| 12  |                    |                                                                                                                                              | xx   |
| 13  |                    |  第 4 位 SV，“卫星 ID-高度角-方位角-SNR”的集和，字符数可变。每条消息最多支持 4 个集和。当传输少于四个集合时，未使用的集合字段不需要为空。    | xx   |
| 14  |                    |                                                                                                                                              | xx   |
| 15  |                    |                                                                                                                                              | xxx  |
| 16  |                    |                                                                                                                                              | xx   |
|  17 | SignalID/ SystemID | NMEA 0183 Version 4.10 该字段为 Signal ID； NMEA 0183 Version 4.11 该字段为 System ID。参考[表](#_bookmark181) [7-34 GNSS ID](#_bookmark181) |  h   |
| 18  | \*xx               | 校验和                                                                                                                                       | \*hh |
| 19  | [CR][LF]           | 语句结束符                                                                                                                                   |      |

#### GPRMCH 从天线的卫星定位信息

本指令用于输出从天线的时间、日期、位置、速度等信息。

简化ASCII 格式：

GPRMCH 1 当前串口输出 1Hz 的 GPRMCH 信息 GPRMCH COM2 1 在com2 输出 1Hz 的 GPRMCH 信息

适用产品：UM982、UMD982

消息输出：

\$GNRMCH,055808.00,A,4004.73817916,N,11614.19891207,E,0.004,99.7,311221,6.9

,W,D,V\*3A

表 7-39 RMCH 数据结构

| ID | 字段     | 数据描述 | 符号 |
|----|----------|----------|------|
| 1  | \$--RMCH | Log 头   |      |

| ID      | 字段          | 数据描述                                                                              | 符号         |
|---------|---------------|---------------------------------------------------------------------------------------|--------------|
|    2    |    utc        | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                             |    hhmmss.ss |
|   3     |   pos status  | 状态： A = 数据可用 V = 导航接收机警告                                                |   A          |
|   4     |   lat         | 纬度，格式为 ddmm.mmmmmmmm dd： 度 mm.mmmmmmmm： 分                                   |   llll.ll    |
| 5       | lat dir       | 纬度方向（N = 北纬，S =南纬）                                                         | a            |
|   6     |   lon         | 经度，格式为dddmm.mmmmmmmm ddd： 度 mm.mmmmmmmm： 分                                  |   yyyyy.yy   |
| 7       | lon dir       | 经度方向（E = 东经，W = 西经）                                                        | a            |
| 8       | speed Kn      | 地面速率，单位为节，保留 3 位小数                                                     | x.x          |
|  9      |  track true   | 地面航向，单位为度，从北向起顺时针计算，保留 1 位小数                                 |  x.x         |
| 10      | date          | 日期：ddmmyy                                                                          | xxxxxx       |
| 11      | mag var       | 磁偏角，单位：度，保留 1 位小数                                                       | x.x          |
| 12      | var dir       | 磁偏角方向                                                                            | a            |
|      13 |      mode ind | 模式： A=自主模式 D = 差分模式 E = 惯导模式 F = RTK Float M = 手动输入模式 N = 无定位 |      a       |

| ID    | 字段           | 数据描述                                                              | 符号 |
|-------|----------------|-----------------------------------------------------------------------|------|
|       |                | P = 高精度模式 R = RTK int S = 模拟器模式 V = 模式无效（不包括 A, D） |      |
|    14 |    mode status | 定位状态： S = 安全 C = 注意 U = 危险 V = 定位状态不可用              |    a |
| 15    | \*xx           | 校验和                                                                | \*hh |
| 16    | [CR][LF]       | 语句结束符                                                            |      |

#### GPVTGH 从天线的地面航向与速度信息

本指令用于输出从天线计算的地面航向、速度等信息。

简化ASCII 格式：

GPVTGH 1 当前串口输出 1Hz 的 GPVTG 信息 GPVTGH COM2 1 在com2 输出 1Hz 的 GPVTG 信息

适用产品：UM982、UMD982

消息输出：

\$GNVTGH,113.125,T,120.041,M,0.01474,N,0.02730,K,D\*73

表 7-40 VTGH 数据结构

| ID | 字段         | 数据描述                                       | 符号 |
|----|--------------|------------------------------------------------|------|
| 1  | \$--VTGH     | Log 头                                         |      |
|  2 |  Course true | 地面航向，单位为度，相对于真北，保留 3 位小 数 |  x.x |
| 3  | Course ind   | 航向标志，固定填 T                             | T    |

| ID       | 字段           | 数据描述                                                                                                  | 符号         |
|----------|----------------|-----------------------------------------------------------------------------------------------------------|--------------|
|  4       |  Course mag    | 地面航向，单位为度，相对于磁北，保留 3 位小 数                                                            |  x.x         |
| 5        | Course ind     | 航向标志，固定填 M                                                                                        | M            |
| 6        | speed Kn       | 地面速率，单位为节，保留 5 位小数                                                                         | x.x          |
| 7        | N              | 速率单位，固定填 N                                                                                        | N            |
| 8        | speed Km       | 地面速率，单位为 km/h，保留 5 位小数                                                                      | x.x          |
| 9        | K              | 速率单位，固定填 K                                                                                        | K            |
|       10 |       Mode ind | 模式： A=自主模式 D = 差分模式 E = 惯导模式 M = 手动输入模式 N = 数据不可用 P = 高精度模式 S = 模拟器模式 |       xxxxxx |
| 11       | \*xx           | 校验和                                                                                                    | \*hh         |
| 12       | [CR][LF]       | 语句结束符                                                                                                |              |

#### GPTHS2 航向信息

本消息包含以度为单位基准站与移动站组成的基线向量（方向为从基准站指向移动站）相对真北方向的航向信息。该信息的输出需要接收机支持 HEADING2 定向工作模式。指令 只支持 ONCHANGED 输出。

简化ASCII 格式：

GPTHS2 ONCHANGED 在当前串口输出 GPTHS2 信息

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0

消息输出：

\$GNTHS2,88.3640,T\*0F

表 7-41 THS2 数据结构

| ID | 字段     | 数据描述                      | 符号 |
|----|----------|-------------------------------|------|
| 1  | \$--THS2 | Log 头                        |      |
| 2  | Heading  | 航向，单位为度，保留 4 位小数 | x.x  |
|  3 |  Mode    | 模式： 固定填 T               |  a   |
| 4  | \*xx     | 校验和                        | \*hh |
| 5  | [CR][LF] | 语句结束符                    |      |

#### GPHPR 姿态参数

该 Log 包含双天线载体的航向角、俯仰角、横滚角等信息。

简化ASCII 格式：

GPHPR 1

适用产品：UM982、UMD982消息输出：

\$GNHPR,074615.00,320.9610,-66.1712,000.0000,4,47,0.00,0999\*45

表 7-42 HPR 数据结构

| ID   | 字段    | 数据描述                                                  | 符号         |
|------|---------|-----------------------------------------------------------|--------------|
| 1    | \$--HPR | Log 头                                                    |              |
|    2 |    utc  | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒 |    hhmmss.ss |
| 3    | heading | 航向角，0～360°，保留 4 位小数                            | hhh.hhhh     |
| 4    | pitch   | 俯仰角，-90～90°，保留 4 位小数                           | ppp.pppp     |
| 5    | roll    | 横滚角，-90～90°，保留 4 位小数                           | rrr.rrrr     |
| 6    | QF      | 解状态：                                                  | q            |

| ID | 字段     | 数据描述                                                                                                    | 符号  |
|----|----------|-------------------------------------------------------------------------------------------------------------|-------|
|    |          | 0=定位无效 1=单点定位 2=码差分 4=RTK 固定解 5=RTK 浮点解 6=航位推算解 7=人工输入固定值 8=超宽巷解 9=SBAS 解 |       |
| 7  | sat No.  | 卫星号                                                                                                      | n     |
| 8  | age      | 差分龄期，单位：秒，保留 2 位小数                                                                           | dd.dd |
| 9  | stn ID   | 基准站 ID                                                                                                   | xxxx  |
| 10 | \*xx     | 校验值                                                                                                      | \*hh  |
| 11 | [CR][LF] | 语句结束符                                                                                                  |       |

#### GPHPR2 姿态参数

本指令用于模组 Heading2 模式下输出 Heading2 解算的航向角、俯仰角、横滚角等信息。指令只支持 ONCHANGED 输出。

简化ASCII 格式：

GPHPR2 ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\$GNHPR2,013025.00,006.2031,000.6226,000.0000,4,38,0.00,3223\*63

表 7-43 HPR2 数据结构

| ID        | 字段       | 数据描述                                                                                                             | 符号         |
|-----------|------------|----------------------------------------------------------------------------------------------------------------------|--------------|
| 1         | \$--HPR2   | Log 头                                                                                                               |              |
|    2      |    utc     | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                            |    hhmmss.ss |
| 3         | heading    | 航向角，0～360°，保留 4 位小数                                                                                       | hhh.hhhh     |
| 4         | pitch      | 俯仰角，-90～90°，保留 4 位小数                                                                                      | ppp.pppp     |
| 5         | roll       | 横滚角，-90～90°，保留 4 位小数                                                                                      | rrr.rrrr     |
|         6 |         QF | 解状态： 0=定位无效 1=单点定位 2=码差分 4=RTK 固定解 5=RTK 浮点解 6=航位推算解 7=人工输入固定值 8=超宽巷解 9=SBAS 解 |         q    |
| 7         | sat No.    | 卫星号                                                                                                               | n            |
| 8         | age        | 差分龄期，单位：秒，保留 2 位小数                                                                                    | dd.dd        |
| 9         | stn ID     | 基准站 ID                                                                                                            | xxxx         |
| 10        | \*xx       | 校验值                                                                                                               | \*hh         |
| 11        | [CR][LF]   | 语句结束符                                                                                                           |              |

#### GPTRA2 方向角输出

本指令用于模组Heading2 模式下输出的Heading2 解算的航向、俯仰、横滚等信息。

指令只支持 ONCHANGED 输出。

简化ASCII 格式：

GPTRA2 ONCHANGED 当前串口输出 1Hz 的 GPTRA2 信息 GPTRA2 COM2 ONCHANGED 在com2 输出 1Hz 的 GPTRA2 信息

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\$GNTRA2,090415.00,88.36,-0.09,0.00,4,30,0.00,0000\*7D

表 7-44 TRA2 数据结构

| ID     | 字段            | 数据描述                                                                                                            | 符号         |
|--------|-----------------|---------------------------------------------------------------------------------------------------------------------|--------------|
| 1      | \$--TRA2        | Log 头                                                                                                              |              |
|    2   |    utc          | UTC 时间，格式为 hhmmss.ss hh： 小时 mm： 分钟 ss.ss： 秒                                                           |    hhmmss.ss |
| 3      | heading         | 方向角，0\~360 度，保留 2 位小数                                                                                    | hhh.hh       |
| 4      | pitch           | 俯仰角：-90\~90 度，保留 2 位小数                                                                                   | ppp.pp       |
| 5      | roll            | 横滚角：-90\~90 度，保留 2 位小数                                                                                   | rrr.rr       |
|      6 |      Sol status | GPS 质量指示符 0 = 定位不可用或无效 1 = 单点定位 2 = 伪距差分或 SBAS 定位 4 = RTK 固定解 5 =RTK 浮点解 6 = 惯导定位 |      q       |
| 7      | Sat num         | 卫星数                                                                                                              | n            |

| ID | 字段       | 数据描述                          | 符号  |
|----|------------|-----------------------------------|-------|
| 8  | Age        | 差分延迟，单位：秒，保留 2 位小数 | dd.dd |
| 9  | Station ID | 基站号                            | xxxx  |
| 10 | \*xx       | 校验和                            | \*hh  |
| 11 | [CR][LF]   | 语句结束符                        |       |

#### GPROT2 旋转速度和方向信息

本指令用于模组 Heading2 模式下输出的 Heading2 解算的旋转速度和方向信息。指令只支持 ONCHANGED 输出。

简化ASCII 格式：

GPROT2 ONCHANGED 当前串口输出 1Hz 的 GPROT2 信息 GPROT2 COM2 ONCHANGED 在com2 输出 1Hz 的 GPROT2 信息

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\$GNROT2,-0.0,A\*30

表 7-45 ROT2 数据结构

| ID  | 字段     | 数据描述                                                | 符号 |
|-----|----------|---------------------------------------------------------|------|
| 1   | \$--ROT2 | Log 头                                                  |      |
|  2  |  rate    | 旋转速率，单位：度/分，保留 1 位小数 “-” = 载体转向左舷 |  x.x |
|   3 |   status | 状态： A = 数据可用 V = 数据无效                        |   A  |
| 4   | \*xx     | 校验和                                                  | \*hh |
| 5   | [CR][LF] | 语句结束符                                              |      |

#### GPHPD 定位定向信息

本指令用于输出时间、方向、位置、速度等信息。

简化ASCII 格式：

GPHPD 1 当前串口输出 1Hz 的 GPHPD 信息 GPHPD COM2 1 在com2 输出 1Hz 的 GPHPD 信息

适用产品：UM982、UMD982

-   该指令后续版本支持

消息输出：

\$GPHPD,2319,462170.00,251.77,-48.16,178.48,40.0789783,116.2365145,63.03,- 0.001,0.000,-0.003,-0.001,-0.002,-0.001,0.000,48,48\*5ac824c3

表 7-46 HPD 数据结构

| ID | 字段      | 数据描述                                                    | 符号        |
|----|-----------|-------------------------------------------------------------|-------------|
| 1  | \$GPHPD   | Log 头，固定输出 GPHPD                                      |             |
| 2  | GPSWeek   | 自 1980-01-06 至当前的星期数（接收机时间）                  | xxxx        |
| 3  | GPSTime   | 星期内的毫秒数（接收机时间），保留 2 位小数                 | xxxxxx.xx   |
| 4  | Heading   | 偏航角，0\~360，单位：度，保留 2 位小数                     | xx.xx       |
| 5  | Pitch     | 俯仰角，-90\~90，单位：度，保留 2 位小数                    | x.xxx       |
|  6 |  Track    | 地速相对真北方向的夹角，0\~359.99，单位：度，保留 2 位 小数 |  xx.xx      |
| 7  | Latitude  | 纬度（WGS84），单位：度，保留 7 位小数                      | xx.xxxxxxx  |
| 8  | Longitude | 经度（WGS84），单位：度，保留 7 位小数                      | xxx.xxxxxxx |
| 9  | Altitude  | 高度（WGS84），单位：米，保留 2 位小数                      | xxx.xx      |
| 10 | Ve        | 东向速度，单位：米/秒，保留 3 位小数                        | x.xxx       |
| 11 | Vn        | 北向速度，单位：米/秒，保留 3 位小数                        | x.xxx       |
| 12 | Vu        | 天向速度，单位：米/秒，保留 3 位小数                        | x.xxx       |

| ID | 字段     | 数据描述                                              | 符号  |
|----|----------|-------------------------------------------------------|-------|
| 13 | Ae       | 两次测量值之间的东向速度差，单位：米/秒，保留3 位小数 | x.xxx |
| 14 | An       | 两次测量值之间的北向速度差，单位：米/秒，保留3 位小数 | x.xxx |
| 15 | Au       | 两次测量值之间的天向速度差，单位：米/秒，保留3 位小数 | x.xxx |
| 16 | Baseline | 基线长度，单位：米，保留 3 位小数                     | x.xxx |
| 17 | NSV1     | 前天线可用星数                                        | xx    |
| 18 | NSV2     | 后天线可用星数                                        | xx    |
| 19 | \*xx     | 校验和                                                | \*hh  |
| 20 | [CR][LF] | 语句结束符                                            |       |

#### QZQSM 灾害告警信息

日本 QZSS 在 L1 SAIF 信号上提供灾害告警（DC Report）信息服务，在地震海啸等灾害发生时，可通过 QZSS 卫星广播预警信息。

该消息提供了基于 L1S DCR 信息，按照 is-qzss-dcr ICD 标准进行定义。该消息只支持 ASCII 输出，QZQSM 的请求会使能 DCR 信息的输出。

ASCII 输出语法：

QZQSM 1

适用产品：UM980、UM982、UB9A0、UM981

消息输出：

\$QZQSM,56,53AD54A4FB0001AF2FD8000000000000000000000000000000000013E CA2C98\*0F

表 7-47 QZQSM 数据结构

| ID | 字段     | 数据描述 | 符号 |
|----|----------|----------|------|
|  1 |  \$QZQSM |  消息头  |      |

| ID  | 字段       | 数据描述                                                    | 符号 |
|-----|------------|-------------------------------------------------------------|------|
|   2 |   PRN      | 56，57，61（PRN 184，185，189） 55（PRN 183） 58（PRN 186） |   XX |
| 3   | DC Message | 十六进制显示                                                | HEX  |
| 4   | \*xx       | 校验和                                                      |      |
| 5   | [CR][LF]   | 语句结束符(仅 ASCII)                                        | -    |

### Unicore 数据输出指令

Unicore 数据格式支持ASCII 和二进制格式输出。二进制信息是一种有严格约定的机器可读格式，适合用于包含大量数据传输的应用。由于固有的压缩格式，二进制信息与ASCII相比数据量要小得多，因此接收机的通讯端口能够发送或接收更多的数据。ASCII 数据格式以“\#”开头。ASCII 数据格式中的“\#”不参与 CRC 校验。Unicore 数据格式结构定义如下：

基本格式：

Header（头） 3 个同步字节，一共 24 个头信息字节。请务必检查头的长度。 Data（数据） 变量

CRC（校验） 4 个字节

表 7-48 Unicore ASCII 及 Binary 数据结构

| 结构编号 | 结构体     | 结构体说明                                                                                                                                                                                                                                                                                      |
|----------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     1    |     Header | Unicore 数据格式都带有 header 信息。二进制数据格式的 Header 信息有 3 个同步字节，一共 24 个头信息字节。详细请参考：[表 7-50 二进制数据格式 Header](#_bookmark210) [（头）结构](#_bookmark210)。解析二进制时，请务必检查 Header 的长 度。ASCII 数据格式的 Header 信息参见[表7-51](#_bookmark211) |
|  2       |  Data      | 数据体，数据体长度根据不同的消息类型长度不同。详 细请见对应的消息类型。                                                                                                                                                                                                                         |

| 结构编号 | 结构体 | 结构体说明                                                                                                                                                             |
|----------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    3     |    CRC | Unicore 数据格式以 32 位的 CRC 校验值结尾。二进制数据格式的 CRC 是一个应用于所有数据，包括头的 32位(bit)的 CRC；ASCII 数据格式的 CRC 校验应用于所有 数据（除“\#”外）。 |

表 7-49 二进制数据格式 Header 的三个同步字节

| Byte   | Hex  | Decimal |
|--------|------|---------|
| First  | 0xAA | 170     |
| Second | 0x44 | 68      |
| Third  | 0xB5 | 181     |

表 7-50 二进制数据格式 Header（头）结构

| ID | 字段          | 类型   | 描述                                  | 字节数 | 字节偏移 |
|----|---------------|--------|---------------------------------------|--------|----------|
| 1  | Sync          | UCHAR  | 十六进制 0xAA.                        | 1      | 0        |
| 2  | Sync          | UCHAR  | 十六进制 0x44.                        | 1      | 1        |
| 3  | Sync          | UCHAR  | 十六进制 0xB5.                        | 1      | 2        |
| 4  | CPUIDle       | UCHAR  | CPU idle 0-100                        | 1      | 3        |
| 5  | Message ID    | USHORT | Message ID                            | 2      | 4        |
| 6  | MessageLength | USHORT | Message Length                        | 2      | 6        |
|  7 |  TimeRef      |  UCHAR | 接收机工作的时间系统 （GPST or BDST） |  1     |  8       |
| 8  | TimeStatus    | UCHAR  | Time Status                           | 1      | 9        |
| 9  | Wn            | USHORT | 时间周                                | 2      | 10       |
| 10 | Ms            | ULONG  | 周内秒（毫秒）                        | 4      | 12       |
| 11 | Version       | ULONG  | Release version                       | 4      | 16       |
| 12 | Reserved      | UCHAR  | 保留                                  | 1      | 20       |
| 13 | Leap sec      | UCHAR  | 闰秒                                  | 1      | 21       |
| 14 | DelayMs       | USHORT | 数据输出延迟                          | 2      | 22       |

表 7-51 ASCII 数据格式 Header（头）结构

| ID  | 字段          | 类型    | 描述                                                                               |
|-----|---------------|---------|------------------------------------------------------------------------------------|
| 1   | Sync          | CHAR    | 同步字符，ASCII 信息始终以一个“\#”字符开始                                         |
| 2   | Message       | CHAR    | 本手册中 log 或命令的 ASCII 名称                                                   |
| 3   | CPUIDle       | UCHAR   | 处理器空闲时间的最小百分比，每秒计算 1 次。                                        |
| 4   | TimeRef       | UCHAR   | 接收机工作的时间系统（GPST or BDST）                                               |
|  5  |  TimeStatus   |  UCHAR  | GPS 时间质量。当前取值Unknown 或Fine，前者表明 接收机还未能计算出准确的 GPS 时间。 |
| 6   | Wn            | USHORT  | GPS 周数                                                                           |
| 7   | Ms            | ULONG   | GPS 周内秒，精确到 ms。                                                            |
| 8   | Version       | ULONG   | Unicore 格式版本号                                                                 |
| 9   | Reserved      | UCHAR   | 保留                                                                               |
| 10  | Leap sec      | UCHAR   | 闰秒                                                                               |
|  11 |  Output Delay |  USHORT | 数据输出时间延迟（数据输出与 GNSS 卫星信号采样时 间差），单位：ms                  |

#### VERSION 版本及授权信息

Version 信息中包含接收机的产品名称、功能授权、序列号、硬件版本、固件版本等信息。其中授权日期格式为：年/月/日。

Message ID: 37

ASCII 输出语法:

VERSIONA

BINARY 输出语法:

VERSIONB

消息输出:

\#VERSIONA,79,GPS,FINE,2326,378237000,15434,0,18,889;"UM982","R4.10Build15

434","HRPT00-S10C-P","2310415000012-LR23A2225208904","ff2740966a10124c","202

4/08/08"\*769fd54f

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 7-52 VERSION 数据结构

| ID          | 字段             | 数据描述                                                                                                                                | 类型           | 字节数      | 字节偏移    |
|-------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|----------------|-------------|-------------|
|   1         |  VERSIONA header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211)                                   |                |   H         |   0         |
|           2 |           Type   | 产品类型 0 = UNKNOWN 17 = UM982 18 = UM980 19 = UM960 24 = UM960L 26 = UM981 40 = UMD982 52 = UB9A0 53 = UBD9A0 62 = UMD960 63 = UMD980 |           Enum |           4 |           H |
| 3           | sw version       | 固件版本                                                                                                                                | Char[33]       | 33          | H+4         |
| 4           | Auth             | 授权类型，当授权码过期显示无效                                                                                                          | Char[129]      | 129         | H+37        |
|  5          |  Psn             | 产品 PN 号和序列号，“-”前为 13 位的 PN 号，后为 15 位的 SN 号                                                                           |  Char[66]      |  66         |  H+166      |
| 6           | efuse ID         | 板卡 ID                                                                                                                                 | Char[33]       | 33          | H+232       |

| ID | 字段       | 数据描述                         | 类型      | 字节数 | 字节偏移 |
|----|------------|----------------------------------|-----------|--------|----------|
|  7 |  comp time | 固件编译日期 YYYY/MM/DD          |  Char[43] |  43    |  H+265   |
| 8  | Xxxx       | 32 位CRC 校验(仅 ASCII 或二进制) | Hex       | 4      | H+308    |
| 9  | [CR][LF]   | 语句结束符(仅 ASCII)             | -         |        |          |

#### OBSVM 观测量

OBSVM 包含当前接收机跟踪通道的测量信息。对于双天线接收机 OBSVM 输出的是主天线的原始观测数据。

Message ID: 12

ASCII 输出语法:

OBSVMA COM1 1

BINARY 输出语法:

OBSVMB COM1 1

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出:

\#OBSVMA,94,GPS,FINE,2190,117395000,0,0,18,17;18,0,26,21720097.812,- 114139892.254585,52,181,-2263.222,4270,0,6262.010,00181c23,0,4,21162081.928,-

111207490.841520,349,1600,-225.810,2010,0,0.000,0018104b,0,31,23853967.973,-

125353430.240712,16,89,-2865.568,4666,0,6267.010,00181c63,0,27,20924379.679,-

109958370.210834,547,1390,2341.516,2953,0,4.010,00181c83,0,16,20322104.147,-

106793385.550616,59,216,-518.194,3848,0,970.010,00181ca3,0,18,24441329.785,-

128440030.962618,15,106,850.996,4281,0,3268.010,00181cc3,0,34,39461753.070,-

207372954.189817,294,679,60.342,3964,0,6267.010,00181da3,0,35,37928367.004,-

199314917.709832,436,1004,77.257,3491,0,5037.010,00181dc3,7,52,23348014.480,-

124764670.630508,74,237,-2702.620,4022,0,254.010,00191c23,11,54,22454359.660,-

120157814.237355,165,1600,-2435.304,2260,0,0.000,0019104b,10,56,22207432.072,-

118794787.240679,108,1600,3984.848,2660,0,0.000,001910ab,4,55,20768970.641,-

110866113.369865,12,87,1123.037,4537,0,1748.010,00191ce3,0,18,20791545.038,-

109260348.040017,22,113,717.752,4422,0,6267.010,005b1c23,0,24,25006179.764,-

131408344.422726,34,160,-1447.680,3982,0,6268.010,005b1c43,0,31,28623544.586,-

150417707.949574,15,121,-2204.498,3966,0,346.010,005b1c63,0,33,28224656.356,-

148321530.956877,529,1240,-1071.997,3280,0,91.010,005b1ca3,0,12,25003241.058,-

131392963.047669,71,246,1277.601,3765,0,4137.010,005b1cc3,0,11,25867003.553,-

135931981.151064,86,301,2863.429,3516,0,89.010,005b1d03\*db2fc208

表 7-53 OBSVM 数据结构

| ID  | 字段          | 数据描述                                                                                              | 类型     | 字节数 | 字节偏移 |
|-----|---------------|-------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1 |  OBSVM header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |          |   H    |   0      |
|  2  | obs Number    |  对应的观测信息个数                                                                                   |  Ulong   |  4     |  H       |
|   3 |  System Freq  | GLONASS 卫星频点号。 （GLONASS 频率+ 7），GPS、 BDS、Galileo 不使用。                                 |   UShort |   2    |   H+4    |
|  4  | PRN/ slot     | 卫星 PRN 号，详见[表7-54](#_bookmark216) [Unicore 消息中的卫星 PRN](#_bookmark216)                    |  UShort  |  2     |  H+6     |
| 5   | psr           | 码伪距测量值，单位：m                                                                                 | Double   | 8      | H+8      |
|  6  |  adr          | 载波相位（积分多普勒），单位： 周                                                                     |  Double  |  8     |  H+16    |
| 7   | psr std       | 码伪距标准差\*100                                                                                     | UShort   | 2      | H+24     |
| 8   | adr std       | 载波相位标准差\*10000                                                                                 | UShort   | 2      | H+26     |
| 9   | dopp          | 瞬时多普勒，单位：Hz                                                                                  | Float    | 4      | H+28     |

| ID    | 字段                                                                                                                                                   | 数据描述                                                               | 类型    | 字节数 | 字节偏移          |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------|--------|-------------------|
|  10   |  C/N0                                                                                                                                                  | 载噪比 C/N0 = 10[log10(S/N0)] （dB-Hz）；载噪比\*100                   |  UShort |  2     |  H+32             |
| 11    | reserved                                                                                                                                               | 保留                                                                   | UShort  | 2      | H+34              |
|  12   |  locktime                                                                                                                                              | 连续跟踪时间（无周跳），单位： s                                       |  Float  |  4     |  H+36             |
|  13   | ch-tr- status                                                                                                                                          | 跟踪状态，参考：[表7-56 通道跟](#_bookmark218) [踪状态](#_bookmark218) |         |  4     |  H+40             |
|   14… | Next OBS offset = H+4+ (\#obs x 40) 一个历元含有观测到的所有卫星所有频点的观测量，每一个频点观测量占 40 个字 节，每一个频点观测量从第 3 到第 13 循环。 |                                                                        |         |        |                   |
|  可变 |  xxxx                                                                                                                                                  |  32 位 CRC 校验                                                        |  Hex    |  4     | H+4+ (\#obs x 40) |
| 可变  | [CR][LF]                                                                                                                                               | 语句结束符(仅 ASCII)                                                   | -       | -      | -                 |

表 7-54 Unicore 消息中的卫星 PRN

| 卫星系统 | PRN      |
|----------|----------|
| BDS      | 1\~63    |
| GPS      | 1\~32    |
| GLONASS  | 38\~61   |
| Galileo  | 1\~36    |
| SBAS     | 120\~158 |
| QZSS     | 193\~202 |
| IRNSS    | 1\~15    |

表 7-55 Unicore 消息中的卫星 PRN 偏移

| 卫星系统 | PRN    |
|----------|--------|
| GPS      | 1\~32  |
| QZSS     | 33\~42 |
| GLONASS  | 43\~66 |

| 卫星系统 | PRN              |
|----------|------------------|
| Galileo  | 75\~110          |
| SBAS     | 120\~158         |
| BDS      | 161\~223         |
| IRNSS    | 67\~74，111\~117 |

表 7-56 通道跟踪状态

| Nibble \# | Bit \# | Mask         | 描述             | Range Value                                                                  |
|-----------|--------|--------------|------------------|------------------------------------------------------------------------------|
|  N0       | 0      | 0x00000001   |   保留           |                                                                              |
|           | 1      | 0x00000002   |                  |                                                                              |
|           | 2      | 0x00000004   |                  |                                                                              |
|           | 3      | 0x00000008   |                  |                                                                              |
|  N1       | 4      | 0x00000010   |                  |                                                                              |
|           | 5      | 0x00000020   |   SV 通道号      |  0-n (0 = 第一个, n = 最后一个) n 视具体接收机                               |
|           | 6      | 0x00000040   |                  |                                                                              |
|           | 7      | 0x00000080   |                  |                                                                              |
|   N2      | 8      | 0x00000100   |                  |                                                                              |
|           | 9      | 0x00000200   |                  |                                                                              |
|           | 10     | 0x00000400   | 载波相位有效标志 | 0 = 无效, 1 = 有效                                                           |
|           | 11     | 0x00000800   | 保留             |                                                                              |
|   N3      | 12     | 0x00001000   | 伪距有效标志     | 0 = 无效, 1 = 有效                                                           |
|           | 13     | 0x00002000   |  保留            |                                                                              |
|           | 14     | 0x00004000   |                  |                                                                              |
|           | 15     | 0x00008000   |                  |                                                                              |
|      N4   | 16     | 0x00010000   |     卫星系统     | 0 = GPS 1 = GLONASS 2 = SBAS 3 = GAL 4 = BDS 5 = QZSS 6 = IRNSS 7 = Reserved |
|           | 17     | 0x00020000   |                  |                                                                              |
|           |   18   |   0x00040000 |                  |                                                                              |
|           | 19     | 0x00080000   | 保留             |                                                                              |
| N5        | 20     | 0x00100000   | 保留             |                                                                              |
|           | 21     | 0x00200000   |                  |                                                                              |

| Nibble \#          | Bit \#          | Mask                    | 描述                       | Range Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------|-------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    |    22           |    0x00400000           |                   信号类型 | 依赖于所支持的卫星系统: GPS: BDS: 0 = L1 C/A 0 = B1I 9 = L2P (Y)8 4 = B1Q 3 = L1C pilot 8 = B1C (Pilot) 11 = L1C data 23 = B1C (Data) semicodeless 5 = B2Q 6 = L5 data 17 = B2I 14 = L5 pilot 12 = B2a (Pilot) 17 = L2C (L) 28 = B2a (Data) 6 = B3Q GLONASS: 21 = B3I 0 = L1 C/A 13= B2b (I) 5 = L2 C/A 6 = G3I GAL: 7 = G3Q 1 = E1B 2 = E1C QZSS: 12 = E5A pilot 0 = L1 C/A 17 = E5B pilot 1 = L1C/B 18 = E6B 3 = L1C pilot 22 = E6C 4 = L1S 6 = L5 data SBAS: 11 = L1C data 0 = L1 C/A 14 = L5 pilot 6 = L5 (I) 17 = L2C (L) 21 = L6D 27 = L6E  IRNSS 6 = L5 data 14 = L5 pilot |
|                    | 23              | 0x00800000              |                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                 N6 | 24              | 0x01000000              |                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                    |              25 |              0x02000000 |                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                    |  26             |  0x04000000             |  L2C 标志位                | 0：L2P (Y)； 1：L2C                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|                    | 27              | 0x08000000              | 保留                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|   N7               | 28              | 0x10000000              | 保留                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                    | 29              | Reserved                | 保留                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                    | 30              | 0x40000000              | 保留                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

8 当 Bit26 标志为 1 时，Bit25 中的 L2P(Y) 实则为 L2C 信号

| Nibble \# | Bit \# | Mask       | 描述 | Range Value |
|-----------|--------|------------|------|-------------|
|           | 31     | 0x80000000 | 保留 |             |

#### OBSVH 从天线的观测量

OBSVH 包含当前接收机从天线跟踪通道的测量信息。

Message ID: 13 ASCII 输出语法:

OBSVHA COM1 1

BINARY 输出语法:

OBSVHB COM1 1

适用产品：UM982、UMD982消息输出:

\#OBSVHA,97,GPS,FINE,2190,359897000,0,0,18,14;0\*9d38304c

表 7-57 OBSVH 数据结构

| ID  | 字段          | 数据描述                                                                                                               | 类型     | 字节数 | 字节偏移 |
|-----|---------------|------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1 |  OBSVH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |          |   H    |   0      |
|  2  | obs Number    |  对应的观测信息个数                                                                                                    |  Ulong   |  4     |  H       |
|   3 |  System Freq  | GLONASS 卫星频点号。 （GLONASS 频率+ 7），GPS 、 BDS、Galileo 不使用。                                                 |   UShort |   2    |   H+4    |
|  4  |  PRN/ slot    | 卫星 PRN 号，详见[表7-54 Unicore](#_bookmark216) [消息中的卫星 PRN](#_bookmark216)                                     |  UShort  |  2     |  H+6     |
| 5   | psr           | 码伪距测量值，单位：m                                                                                                  | Double   | 8      | H+8      |

| ID     | 字段                                                                                                                                                   | 数据描述                                                               | 类型    | 字节数 | 字节偏移          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------|--------|-------------------|
|  6     |  adr                                                                                                                                                   | 载波相位（积分多普勒），单位： 周                                      |  Double |  8     |  H+16             |
| 7      | psr std                                                                                                                                                | 码伪距标准差\*100                                                      | UShort  | 2      | H+24              |
| 8      | adr std                                                                                                                                                | 载波相位标准差\*10000                                                  | UShort  | 2      | H+26              |
| 9      | dopp                                                                                                                                                   | 瞬时多普勒，单位：Hz                                                   | Float   | 4      | H+28              |
|  10    |  C/N0                                                                                                                                                  | 载噪比 C/N0 = 10[log10(S/N0)] （dB-Hz）；载噪比\*100                   |  UShort |  2     |  H+32             |
| 11     | reserved                                                                                                                                               | 保留                                                                   | UShort  | 2      | H+34              |
| 12     | locktime                                                                                                                                               | 连续跟踪时间（无周跳），单位：s                                        | Float   | 4      | H+36              |
|  13    | ch-tr- status                                                                                                                                          | 跟踪状态，参考：[表7-56 通道跟踪](#_bookmark218) [状态](#_bookmark218) |         |  4     |  H+40             |
|   14…  | Next OBS offset = H+4+ (\#obs x 40) 一个历元含有观测到的所有卫星所有频点的观测量，每一个频点观测量占 40 个字 节，每一个频点观测量从第 3 到第 13 循环。 |                                                                        |         |        |                   |
|   可变 |   xxxx                                                                                                                                                 |   32 位 CRC 校验                                                       |   Hex   |   4    | H+4+ (\#obs x 40) |
| 可变   | [CR][LF]                                                                                                                                               | 语句结束符(仅 ASCII)                                                   | -       | -      | -                 |

#### OBSVMCMP 压缩格式原始观测数据信息

OBSVMCMP 包含了压缩格式的 OBSVM 数据信息。

Message ID：138 ASCII 输出语法：

OBSVMCMPA COM1 1

BINARY 输出语法：

OBSVMCMPB COM1 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM960、UMD960、UM982、 UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\#OBSVMCMPA,97,GPS,FINE,2244,271100000,0,0,18,14;15,231c38056534f76f3f3982 0a747fff9e7519c015e0020000,231cd0012392f75f2639820a8f905fd82019c01560030000

,431c380562a20030e916b20965478889431fc01560030000,631c3805c35cf43fad949a0b

0e037f8f850ac01560020000,631cd001bad8f42f9e949a0bbfcbd9ce420ac015e0020000, 831c380598dcf4cf102cd30b9e9687f2190cc015e0010000,a31c300109070260ace7bb09

3919828463162015c0020000,e31c3805f873fb6f0dadfe0926ca54e23220c01580030000,

e31cd0018aa4fbcfe2acfe09f5ace6982020c015c0030000,071d300129740cd017ca160c7 457ebcf7a10200040010000,231d3805014609f0e7165f0aba44fbb0651ac01520030000,2

31dd001fce208b0c0165f0a5d8c9be9201ac015a0030000,431d3805df6f06d090925e0ba c1a36ae621dc01560020000,631d3805026f06305463350bb9bd4ac3e703c015a0020000, 631dd001562a06d03a63350bd5057d803003c01540030000\*d04eae82

表 7-58 OBSVMCMP 压缩说明

| 数据         | Bit 低位到高位 | 位长(Bits) | 比例因子                                 | 单位   |
|--------------|----------------|------------|------------------------------------------|--------|
| 通道跟踪状态 | 0-31           | 32         | 参考[表7-56 通道跟踪状态](#_bookmark218) | -      |
| 多普勒       | 32-59          | 28         | 1/256                                    | Hz     |
| PSR 伪距     | 60-95          | 36         | 1/128                                    | m      |
| ADR 载波相位 | 96-127         | 32         | 1/256                                    | Cycles |
| Psr Std      | 128-131        | 4          | 见下表                                   | m      |
| Adr Std      | 132-135        | 4          | (n+1)/512                                | Cycles |
| PRN          | 136-143        | 8          | 1                                        | -      |
| Lock time    | 144-164        | 21         | 1/32                                     | S      |
| C/N0         | 165-169        | 5          | 20+n                                     | dB-Hz  |

| 数据           | Bit 低位到高位 | 位长(Bits) | 比例因子 | 单位 |
|----------------|----------------|------------|----------|------|
| GLONASS 频率号 | 170-175        | N+7        | 1        | -    |
| 保留           | 176-191        | 16         |          |      |

表 7-59 Psrstd Index 表

| Index | Data    |
|-------|---------|
| 0     | 0.050   |
| 1     | 0.075   |
| 2     | 0.113   |
| 3     | 0.169   |
| 4     | 0.253   |
| 5     | 0.380   |
| 6     | 0.570   |
| 7     | 0.854   |
| 8     | 1.281   |
| 9     | 2.375   |
| 10    | 4.750   |
| 11    | 9.500   |
| 12    | 19.000  |
| 13    | 38.000  |
| 14    | 76.000  |
| 15    | 152.000 |

表 7-60 OBSVMCMP 数据结构

| ID   | 字段              | 数据描述                                                                                                                                   | 类型 | 字节数 | 字节偏移 |
|------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|------|--------|----------|
|    1 |   OBSVMCMP header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211)，Header 中的时间为基准 站观测值的时间 |      |    H   |    0     |

| ID     | 字段                                | 数据描述                                                                       | 类型  | 字节数 | 字节偏移          |
|--------|-------------------------------------|--------------------------------------------------------------------------------|-------|--------|-------------------|
| 2      | obs Number                          | 对应的观测信息个数                                                             | Ulong | 4      | H                 |
|  3     |  Cmp record                         | OBSVM 压缩信息，参考[表7-58](#_bookmark222) [OBSVMCMP 压缩说明](#_bookmark222) |  Hex  |  24    |  H+4              |
| 4      | Next Cmp offset = H+4+ (\#obs x 24) |                                                                                |       |        |                   |
|   可变 |   xxxx                              |   32 位 CRC 校验                                                               |   Hex |   4    | H+4+ (\#obs x 24) |
| 可变   | [CR][LF]                            | 语句结束符(仅 ASCII)                                                           | -     | -      | -                 |

#### OBSVHCMP 压缩格式的从天线的原始观测量

OBSVHCMP 包含了压缩格式的 OBSVH 数据信息。

Message ID：139 ASCII 输出语法：

OBSVHCMPA COM1 1

BINARY 输出语法：

OBSVHCMPB COM1 1

适用产品：UM982、UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\#OBSVHCMPA,97,GPS,FINE,2244,271111000,0,0,18,14;8,231c3805d95bf4cfc78e9b 0be8f5fe8ed90a201640020000,431c3805b86906904ad9340b8f6b91c395034016a00200

00,631c3805b86ffbbfee0eff093daf22e22020c01660030000,831c3805c09e00d06d09b20 97e358f89541f601660030000,a31c3805c06c06205c085e0be7d77caee71d40166002000

0,c31c380514420910c84f5e0a333561b1311a601620030000,e31c38057430f78f6af6820

ae5ab9e9e53192016c0020000,231d380560daf4ff561bd40b33ec0cf27a0c2016c001000 0\*24135d12

表 7-61 OBSVHCMP 压缩说明

| 数据           | Bit 低位到高位 | 位长(Bits) | 比例因子                                  | 单位   |
|----------------|----------------|------------|-------------------------------------------|--------|
| 通道跟踪状态   | 0-31           | 32         | 参考[表7-56 通道跟踪状态](#_bookmark218)  | -      |
| 多普勒         | 32-59          | 28         | 1/256                                     | Hz     |
| PSR 伪距       | 60-95          | 36         | 1/128                                     | m      |
| ADR 载波相位   | 96-127         | 32         | 1/256                                     | Cycles |
| Psr Std        | 128-131        | 4          | 见[表7-59 Psrstd Index 表](#_bookmark223) | m      |
| Adr Std        | 132-135        | 4          | (n+1)/512                                 | Cycles |
| PRN            | 136-143        | 8          | 1                                         | -      |
| Lock time      | 144-164        | 21         | 1/32                                      | S      |
| C/N0           | 165-169        | 5          | 20+n                                      | dB-Hz  |
| GLONASS 频率号 | 170-175        | N+7        | 1                                         | -      |
| 保留           | 176-191        | 16         |                                           |        |

表 7-62 OBSVHCMP 数据结构

| ID   | 字段                                | 数据描述                                                                                                                                   | 类型  | 字节数 | 字节偏移 |
|------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|-------|--------|----------|
|    1 |   OBSVHCMP header                   | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211)，Header 中的时间为基准 站观测值的时间 |       |    H   |    0     |
| 2    | obs Number                          | 对应的观测信息个数                                                                                                                         | Ulong | 4      | H        |
|  3   |  Cmp record                         | OBSVH 压缩信息，参考[表7-61](#_bookmark226) [OBSVHCMP 压缩说明](#_bookmark226)                                                             |  Hex  |  24    |  H+4     |
| 4    | Next Cmp offset = H+4+ (\#obs x 24) |                                                                                                                                            |       |        |          |

| ID     | 字段     | 数据描述             | 类型  | 字节数 | 字节偏移          |
|--------|----------|----------------------|-------|--------|-------------------|
|   可变 |   xxxx   |   32 位 CRC 校验     |   Hex |   4    | H+4+ (\#obs x 24) |
| 可变   | [CR][LF] | 语句结束符(仅 ASCII) | -     | -      | -                 |

#### OBSVBASE 基准站观测量

OBSVBASE 包含当前接收机接收到的基准站的观测量。该消息仅支持ONCHANGED 请求方式。

Message ID: 284

ASCII 输出语法:

OBSVBASEA COM1 ONCHANGED

BINARY 输出语法:

OBSVBASEB COM1 ONCHANGED

适用产品：UM982、UMD982、UM980、UMD980、UB9A0、UBD9A0、UM960L、 UM960、UMD960

消息输出:

\#OBSVBASEA,92,GPS,FINE,2249,205089000,0,0,18,74;24,0,1,19949528.980,-10483 5482.170960,0,0,0.000,4500,0,0.001,00001c00,0,1,19949532.536,-81689986.637729,0,0,

0.000,4900,0,0.001,02201c00,0,1,19949531.929,-78286236.510802,0,0,0.000,5300,0,0.0

01,01c01c00,0,3,24393288.815,-128187597.395405,0,0,0.000,3100,0,0.001,00001c00,0,

3,24393312.277,-99886437.505261,0,0,0.000,2900,0,0.001,02201c00,0,3,24393311.741,-

95724503.606254,0,0,0.000,3200,0,0.001,01c01c00,0,7,22345353.436,-117425624.5378

71,0,0,0.000,4200,0,0.001,00001c00,0,7,22345357.939,-91500486.474533,0,0,0.000,410

0,0,0.001,02201c00,0,8,23355052.211,-122731627.217417,0,0,0.000,3500,0,0.001,00001

c00,0,8,23355058.822,-95635036.671759,0,0,0.000,4100,0,0.001,02201c00,0,8,2335505 8.125,-91650242.898597,0,0,0.000,4500,0,0.001,01c01c00,0,14,21044513.242,-1105896

63.518782,0,0,0.000,4300,0,0.001,00001c00,0,14,21044514.689,-86173762.987424,0,0,

0.000,4700,0,0.001,02201c00,0,14,21044519.746,-82583190.254938,0,0,0.000,5200,0,0.

001,01c01c00,0,14,21044513.135,-110589662.770497,0,0,0.000,4400,0,0.001,00601c00,

0,17,22264289.041,-116999629.117075,0,0,0.000,4100,0,0.001,00001c00,0,17,2226429

0.650,-91168542.230887,0,0,0.000,4200,0,0.001,02201c00,0,19,25085746.602,-1318264

87.397418,0,0,0.000,3600,0,0.001,00001c00,0,19,25085754.035,-102721938.513004,0,0,

0.000,3100,0,0.001,01201c00,0,21,21374822.792,-112325452.257686,0,0,0.000,4500,0,

0.001,00001c00,0,21,21374822.721,-87526326.180750,0,0,0.000,4200,0,0.001,01201c0

0,0,30,21595580.723,-113485542.603204,0,0,0.000,4400,0,0.001,00001c00,0,30,215955

85.190,-88430293.120489,0,0,0.000,4500,0,0.001,02201c00,0,30,21595584.940,-847456

97.365627,0,0,0.000,4900,0,0.001,01c01c00\*e25781b8

表 7-63 OBSVBASE 数据结构

| ID   | 字段              | 数据描述                                                                                                                                                     | 类型     | 字节数 | 字节偏移 |
|------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|    1 |   OBSVBASE header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211)，Header 中的时间为基准站观 测值的时间 |          |    H   |    0     |
|  2   | obs Number        |  对应的观测信息个数                                                                                                                                          |  Ulong   |  4     |  H       |
|   3  |  System Freq      | GLONASS 卫星频点号。 （GLONASS 频率+ 7），GPS 、 BDS、Galileo 不使用。                                                                                       |   UShort |   2    |   H+4    |
|  4   |  PRN/ slot        | 卫星 PRN 号，详见[表7-54 Unicore](#_bookmark216) [消息中的卫星 PRN](#_bookmark216)                                                                           |  UShort  |  2     |  H+6     |
| 5    | psr               | 码伪距测量值，单位：m                                                                                                                                        | Double   | 8      | H+8      |

| ID     | 字段                                                                                                                                                   | 数据描述                                                               | 类型    | 字节数 | 字节偏移          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------|--------|-------------------|
|  6     |  adr                                                                                                                                                   | 载波相位（积分多普勒），单位： 周                                      |  Double |  8     |  H+16             |
| 7      | psr std                                                                                                                                                | 码伪距标准差\*100                                                      | UShort  | 2      | H+24              |
| 8      | adr std                                                                                                                                                | 载波相位标准差\*10000                                                  | UShort  | 2      | H+26              |
| 9      | dopp                                                                                                                                                   | 瞬时多普勒，单位：Hz                                                   | Float   | 4      | H+28              |
|  10    |  C/N0                                                                                                                                                  | 载噪比 C/N0 = 10[log10(S/N0)] （dB-Hz）；载噪比\*100                   |  UShort |  2     |  H+32             |
| 11     | reserved                                                                                                                                               | 保留                                                                   | UShort  | 2      | H+34              |
| 12     | locktime                                                                                                                                               | 连续跟踪时间（无周跳），单位：s                                        | Float   | 4      | H+36              |
|  13    | ch-tr- status                                                                                                                                          | 跟踪状态，参考：[表7-56 通道跟踪](#_bookmark218) [状态](#_bookmark218) |         |  4     |  H+40             |
|   14…  | Next OBS offset = H+4+ (\#obs x 40) 一个历元含有观测到的所有卫星所有频点的观测量，每一个频点观测量占 40 个字 节，每一个频点观测量从第 3 到第 13 循环。 |                                                                        |         |        |                   |
|   可变 |   xxxx                                                                                                                                                 |   32 位 CRC 校验                                                       |   Hex   |   4    | H+4+ (\#obs x 40) |
| 可变   | [CR][LF]                                                                                                                                               | 语句结束符(仅 ASCII)                                                   | -       | -      | -                 |

#### BASEINFO 基准站信息

基准站的位置、ID 与健康信息。该消息支持ONCHANGED 请求方式。

Message ID: 176 ASCII 输出语法:

BASEINFOA 1 BASEINFOA ONCHANGED

BINARY 输出语法:

BASEINFOB 1 BASEINFOB ONCHANGED

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\#BASEINFOA,56,GPS,FINE,2190,376748000,0,0,18,153;00000000,-2160493.199,438 3620.763,4084734.120,"0000",0\*2edbd87a

表 7-64 BASEINFO 数据结构

| ID  | 字段              | 数据描述                                                                                               | 类型    | 字节数 | 字节偏移 |
|-----|-------------------|--------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |   BASEINFO Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |         |   H    |   0      |
|   2 |   Status          | 基准站的状态： 0 = valid 1 = invalid                                                                   |   Ulong |   4    |   H      |
| 3   | X                 | ECEF X 轴坐标值                                                                                        | Double  | 8      | H+4      |
| 4   | Y                 | ECEF Y 轴坐标值                                                                                        | Double  | 8      | H+12     |
| 5   | Z                 | ECEF Z 轴坐标值                                                                                        | Double  | 8      | H+20     |
| 6   | Station id        | 基准站 ID                                                                                              | Char[5] | 8      | H+28     |
| 7   | reserved          | 保留                                                                                                   | Ulong   | 4      | H+36     |
| 8   | xxxx              | 32 位 CRC 校验                                                                                         | Hex     | 4      | H+40     |
| 9   | [CR][LF]          | 语句结束符(仅 ASCII)                                                                                   | -       | -      | -        |

#### GPSION 电离层参数

该信息提供 GPS 卫星系统播发的电离层模型参数。支持ONCHANGED 请求方式。

Message ID: 8 ASCII 输出语法:

GPSIONA 1

GPSIONA ONCHANGED

BINARY 输出语法:

GPSIONB 1

GPSIONB ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GPSIONA,90,GPS,FINE,2190,371250000,0,0,18,21;1.490116119384766e-08,-7.450 580596923828e-09,-5.960464477539062e-08,1.192092895507812e-07,1.290240000000

000e+05,-1.966080000000000e+05,6.553600000000000e+04,3.276800000000000e+05,

0,0,0,0\*c5974f70

表 7-65 GPSION 数据结构

| ID  | 字段     | 数据描述                                                                                               | 类型   | 字节数 | 字节偏移 |
|-----|----------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |   GPSION | 消息头，二进制消息头结构请参 考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | a0       | Alpha 参数常数项                                                                                       | Double | 8      | H        |
| 3   | a1       | Alpha 参数的 1 阶项                                                                                    | Double | 8      | H+8      |
| 4   | a2       | Alpha 参数的 2 阶项                                                                                    | Double | 8      | H+16     |
| 5   | a3       | Alpha 参数的 3 阶项                                                                                    | Double | 8      | H+24     |
| 6   | b0       | Beta 参数的常数项                                                                                      | Double | 8      | H+32     |
| 7   | b1       | Beta 参数的 1 阶项                                                                                     | Double | 8      | H+40     |
| 8   | b2       | Beta 参数的 2 阶项                                                                                     | Double | 8      | H+48     |
| 9   | b3       | Beta 参数的 3 阶项                                                                                     | Double | 8      | H+56     |
| 10  | usSVID   | 解析电离层参数的卫星号                                                                                 | Ushort | 2      | H+64     |

| ID  | 字段     | 数据描述                                      | 类型    | 字节数 | 字节偏移 |
|-----|----------|-----------------------------------------------|---------|--------|----------|
|  11 |  usWeek  | 解析电离层参数时的时间对应的 GPS 周           |  Ushort |  2     |  H+66    |
|  12 |  ulSec   | 解析电离层参数时的时间对应的 GPS 秒，单位毫秒 |  ULong  |  4     |  H+68    |
| 13  | reserved | 保留                                          | Ulong   | 4      | H+72     |
| 14  | xxxx     | 32 位 CRC 校验                                | Hex     | 4      | H+76     |
| 15  | [CR][LF] | 语句结束符(仅 ASCII)                          | -       | -      | -        |

#### BD3ION 电离层参数

该信息提供北斗卫星系统BD3 播发的电离层模型参数。支持ONCHANGED 请求方式。

Message ID: 21 ASCII 输出语法:

BD3IONA 1

BD3IONA ONCHANGED

BINARY 输出语法:

BD3IONB 1

BD3IONB ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM960、UMD960、UM982、 UMD982

消息输出：

\#BD3IONA,89,GPS,FINE,2190,371265000,0,0,18,22;0.000000000000000e+00,0.000 000000000000e+00,0.000000000000000e+00,0.000000000000000e+00,0.000000000000

000e+00,0.000000000000000e+00,0.000000000000000e+00,0.000000000000000e+00,0.

000000000000000e+00,0\*cd77c4ca

表 7-66 BD3ION 数据结构

| ID  | 字段     | 数据描述                                                                                               | 类型  | 字节数 | 字节偏移 |
|-----|----------|--------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |   BD3ION | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | A1       | 电离层延迟改正模型参数 1                                                                               | FLOAT | 4      | H        |
| 3   | A2       | 电离层延迟改正模型参数 2                                                                               | FLOAT | 4      | H+4      |
| 4   | A3       | 电离层延迟改正模型参数 3                                                                               | FLOAT | 4      | H+8      |
| 5   | A4       | 电离层延迟改正模型参数 4                                                                               | FLOAT | 4      | H+12     |
| 6   | A5       | 电离层延迟改正模型参数 5                                                                               | FLOAT | 4      | H+16     |
| 7   | A6       | 电离层延迟改正模型参数 6                                                                               | FLOAT | 4      | H+20     |
| 8   | A7       | 电离层延迟改正模型参数 7                                                                               | FLOAT | 4      | H+24     |
| 9   | A8       | 电离层延迟改正模型参数 8                                                                               | FLOAT | 4      | H+28     |
| 10  | A9       | 电离层延迟改正模型参数 9                                                                               | FLOAT | 4      | H+32     |
| 11  | reserved | 保留                                                                                                   | ULONG | 4      | H+40     |
| 12  | xxxx     | 32 位 CRC 校验                                                                                         | Hex   | 4      | H+44     |
| 13  | [CR][LF] | 语句结束符(仅 ASCII)                                                                                   | -     | -      | -        |

#### BDSION 电离层参数

该信息提供北斗卫星系统播发的电离层模型参数。支持ONCHANGED 请求方式。

Message ID: 4 ASCII 输出语法:

BDSIONA 1

BDSIONA ONCHANGED

BINARY 输出语法:

BDSIONB 1

BDSIONB ONCHANGED

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\#BDSIONA,97,GPS,FINE,2190,362233000,0,0,18,15;1.396983861923218e-08,4.4703 48358154297e-08,-5.364418029785156e-07,8.940696716308594e-07,1.4336000000000

00e+05,-3.768320000000000e+05,4.587520000000000e+05,5.242880000000000e+05,3

6,0,0,0\*94da1274

表 7-67 BDSION 数据结构

| ID  | 字段     | 数据描述                                                                                               | 类型    | 字节数 | 字节偏移 |
|-----|----------|--------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |   BDSION | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |         |   H    |   0      |
| 2   | a0       | Alpha 参数常数项                                                                                       | Double  | 8      | H        |
| 3   | a1       | Alpha 参数的 1 阶项                                                                                    | Double  | 8      | H+8      |
| 4   | a2       | Alpha 参数的 2 阶项                                                                                    | Double  | 8      | H+16     |
| 5   | a3       | Alpha 参数的 3 阶项                                                                                    | Double  | 8      | H+24     |
| 6   | b0       | Beta 参数的常数项                                                                                      | Double  | 8      | H+32     |
| 7   | b1       | Beta 参数的 1 阶项                                                                                     | Double  | 8      | H+40     |
| 8   | b2       | Beta 参数的 2 阶项                                                                                     | Double  | 8      | H+48     |
| 9   | b3       | Beta 参数的 3 阶项                                                                                     | Double  | 8      | H+56     |
| 10  | usSVID   | 解析电离层参数的卫星号                                                                                 | Ushort  | 2      | H+64     |
|  11 |  usWeek  | 解析电离层参数时的时间对应的 GPS 周                                                                    |  Ushort |  2     |  H+66    |
|  12 |  ulSec   | 解析电离层参数时的时间对应的 GPS 秒，单位毫秒                                                          |  ULong  |  4     |  H+68    |
| 13  | reserved | 保留                                                                                                   | Ulong   | 4      | H+72     |
| 14  | xxxx     | 32 位 CRC 校验                                                                                         | Hex     | 4      | H+76     |
| 15  | [CR][LF] | 语句结束符(仅 ASCII)                                                                                   | -       | -      | -        |

#### GALION 电离层参数

该信息提供 Galileo 卫星系统播发的电离层模型参数。支持ONCHANGED 请求方式。

Message ID: 9 ASCII 输出语法:

GALIONA 1

GALIONA ONCHANGED

BINARY 输出语法:

GALIONB 1

GALIONB ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GALIONA,96,GPS,FINE,2218,465990000,0,0,18,21;1.240000000000000e+02,4.9218 75000000000e-01,1.293945312500000e-02,0,0,0,0,0,0\*9e349a84

表 7-68 GALION 数据结构

| ID  | 字段     | 数据描述                                                                                               | 类型   | 字节数 | 字节偏移 |
|-----|----------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |   GALION | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | a0       | Alpha 参数的 1 阶项                                                                                    | Double | 8      | H        |
| 3   | a1       | Alpha 参数的 2 阶项                                                                                    | Double | 8      | H+8      |
| 4   | a2       | Alpha 参数的 3 阶项                                                                                    | Double | 8      | H+16     |
| 5   | SF1      | Region 1 的电离层干扰标志                                                                              | UCHAR  | 1      | H+24     |
| 6   | SF2      | Region 2 的电离层干扰标志                                                                              | UCHAR  | 1      | H+25     |
| 7   | SF3      | Region3 的电离层干扰标志                                                                               | UCHAR  | 1      | H+26     |
| 8   | SF4      | Region 4 的电离层干扰标志                                                                              | UCHAR  | 1      | H+27     |

| ID | 字段     | 数据描述                  | 类型  | 字节数 | 字节偏移 |
|----|----------|---------------------------|-------|--------|----------|
| 9  | SF5      | Region 5 的电离层干扰标志 | UCHAR | 1      | H+28     |
| 10 | reserved | 保留                      | Ulong | 4      | H+29     |
| 11 | xxxx     | 32 位 CRC 校验            | Hex   | 4      | H+33     |
| 12 | [CR][LF] | 语句结束符(仅 ASCII)      | -     | -      | -        |

#### GPSUTC 协调世界时数据

该信息提供 GPST 与协调世界（UTC）的转换参数。支持 ONCHANGED 请求方式。

Message ID: 19 ASCII 输出语法:

GPSUTCA 1

GPSUTCA ONCHANGED

BINARY 输出语法:

GPSUTCB 1

GPSUTCB ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GPSUTCA,97,GPS,FINE,2190,362356000,0,0,18,15;2190,589824,- 1.862645149230957e-09,-5.329070518e-15,2185,7,18,18,0,0\*4a84abce

表 7-69 GPSUTC 数据结构

| ID  | 字段     | 数据描述                                                                                              | 类型  | 字节数 | 字节偏移 |
|-----|----------|-------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |   GPSUTC | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | utc wn   | UTC 参考周数                                                                                          | Ulong | 4      | H        |

| ID | 字段        | 数据描述                                                   | 类型   | 字节数 | 字节偏移 |
|----|-------------|------------------------------------------------------------|--------|--------|----------|
| 3  | tot         | UTC 参数的参考时间                                         | Ulong  | 4      | H+4      |
| 4  | A0          | GPST 相对于 UTC 的钟差                                     | Double | 8      | H+8      |
| 5  | A1          | GPST 相对于 UTC 的钟速                                     | Double | 8      | H+16     |
|  6 |  wn lsf     | 新的闰秒生效的周计数（基于 GPS 时间）                      |  Ulong |  4     |  H+24    |
|  7 |  dn         | 新的闰秒生效的周内日计数（范 围为 1 到 7，周日=1，周六=7） |  Ulong |  4     |  H+28    |
|  8 |  deltat ls  | 新的闰秒生效前 GPST 相对于 UTC 的累积闰秒改正数            |  Long  |  4     |  H+32    |
|  9 |  deltat lsf | 新的闰秒生效后 GPST 相对于 UTC 的累积闰秒改正数            |  Long  |  4     |  H+36    |
| 10 | deltat utc  | GPST 相对于 UTC 时间差                                     | Ulong  | 4      | H+40     |
| 11 | reserved    | 保留                                                       | Ulong  | 4      | H+44     |
| 12 | xxxx        | 32 位 CRC 校验                                             | Hex    | 4      | H+48     |
| 13 | [CR][LF]    | 语句结束符(仅 ASCII)                                       | -      | -      | -        |

#### BD3UTC 协调世界时数据

该信息提供 BDST 与协调世界时（UTC）的转换参数。支持 ONCHANGED 请求方式。

Message ID: 22 ASCII 输出语法:

BD3UTCA 1

BD3UTCA ONCHANGED

BINARY 输出语法:

BD3UTCB 1

BD3UTCB ONCHANGED

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

消息输出：

\#BD3UTCA,97,GPS,FINE,2190,362396000,0,0,18,14;0,0,0.000000000000000e+00,0.

000000000e+00,0.000000000000000e+00,0,0,0,0,0,0\*4bd9130e

表 7-70 BD3UTC 数据结构

| ID  | 字段        | 数据描述                                                                                                               | 类型   | 字节数 | 字节偏移 |
|-----|-------------|------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
|  1  |  BD3UTC     | 消息头，二进制消息头结构请参考[表](#_bookmark210) [7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |        |  H     |  0       |
| 2   | utc wn      | UTC 参考周数                                                                                                           | Ulong  | 4      | H        |
| 3   | tot         | UTC 参数的参考时间                                                                                                     | Ulong  | 4      | H+4      |
| 4   | A0          | BDST 相对于 UTC 的偏差系数                                                                                             | Double | 8      | H+8      |
| 5   | A1          | BDST 相对于 UTC 的漂移系数                                                                                             | Double | 8      | H+16     |
| 6   | A2          | BDST 相对于 UTC 的漂移率系数                                                                                           | Double | 8      | H+24     |
|  7  |  wn lsf     | 新的闰秒生效的周计数（基于 BDS 时 间）                                                                                 |  Ulong |  4     |  H+32    |
|  8  |  dn         | 新的闰秒生效的周内日计数（范围为 0 到 6，周日=0，周六=6）                                                              |  Ulong |  4     |  H+36    |
|  9  |  deltat ls  | 新的闰秒生效前 BDST 相对于 UTC 的 累积闰秒改正数                                                                       |  Long  |  4     |  H+40    |
|  10 |  deltat lsf | 新的闰秒生效后 BDST 相对于 UTC 的 累积闰秒改正数                                                                       |  Long  |  4     |  H+44    |
| 11  | reserved    | 保留                                                                                                                   | Ulong  | 4      | H+48     |
| 12  | reserved    | 保留                                                                                                                   | Ulong  | 4      | H+52     |
| 13  | xxxx        | 32 位 CRC 校验                                                                                                         | Hex    | 4      | H+456    |
| 14  | [CR][LF]    | 语句结束符(仅 ASCII)                                                                                                   | -      | -      | -        |

#### BDSUTC 协调世界时数据

该信息提供 BDST 与协调世界时(UTC)的转换参数。支持 ONCHANGED 请求方式。

Message ID: 2012 ASCII 输出语法:

BDSUTCA 1

BDSUTCA ONCHANGED

BINARY 输出语法:

BDSUTCB 1

BDSUTCB ONCHANGED

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\#BDSUTCA,97,GPS,FINE,2190,362435000,0,0,18,14;0,0,0.000000000000000e+00,- 2.042810365e-14,829,6,4,4,0,0\*c81b21f3

表 7-71 BDSUTC 数据结构

| ID  | 字段     | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|----------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |   BDSUTC | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参 考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | Reserved | 保留位                                                                                                | Ulong  | 4      | H        |
| 3   | Reserved | 保留位                                                                                                | Ulong  | 4      | H+4      |
| 4   | A0       | BDT 相对于 UTC 的钟差                                                                                 | Double | 8      | H+8      |
| 5   | A1       | BDT 相对于 UTC 的钟速                                                                                 | Double | 8      | H+16     |
|  6  |  wn lsf  | 新的闰秒生效的周计数（ 基于 BDST 时间）                                                               |  Ulong |  4     |  H+24    |

| ID | 字段        | 数据描述                                                   | 类型   | 字节数 | 字节偏移 |
|----|-------------|------------------------------------------------------------|--------|--------|----------|
|  7 |  Dn         | 新的闰秒生效的周内日计数（范 围为 0 到 6，周日=0，周六=6） |  Ulong |  4     |  H+28    |
|  8 |  deltat ls  | 新的闰秒生效前 BDT 相对于 UTC 的累积闰秒改正数             |  Long  |  4     |  H+32    |
|  9 |  deltat lsf | 新的闰秒生效后 BDT 相对于 UTC 的累积闰秒改正数             |  Long  |  4     |  H+36    |
| 10 | Reserved    | 保留                                                       | Ulong  | 4      | H+40     |
| 11 | Reserved    | 保留                                                       | Ulong  | 4      | H+44     |
| 12 | Xxxx        | 32 位 CRC 校验                                             | Hex    | 4      | H+48     |
| 13 | [CR][LF]    | 语句结束符(仅 ASCII)                                       | -      | -      | -        |

#### GALUTC 协调世界时数据

该信息提供 Galileo 时与协调世界时（UTC）的转换参数。支持 ONCHANGED 请求方式。

Message ID: 20

ASCII 输出语法:

GALUTCA 1

GALUTCA ONCHANGED

BINARY 输出语法:

GALUTCB 1

GALUTCB ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GALUTCA,97,GPS,FINE,2190,362475000,0,0,18,14;2.793967723846436e-09,- 1.776356839400250e-15,18,96,1166,1161,7,18,6.984919309616089e-10,-

1.865174681370263e-14,345600,14\*d266704b

表 7-72 GALUTC 数据结构

| ID  | 字段        | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|-------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |   GALUTC    | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参 考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | A0          | Galileo 时相对于 UTC 的钟差                                                                           | Double | 8      | H+0      |
| 3   | A1          | Galileo 时相对于 UTC 的钟速                                                                           | Double | 8      | H+8      |
|  4  |  deltat ls  | 新的闰秒生效前 Galileo 时相对于 UTC 的累积闰秒改正数                                                  |  long  |  4     |  H+16    |
| 5   | tot         | UTC 参数的参考时间                                                                                    | Ulong  | 4      | H+20     |
| 6   | utc wn      | UTC 参考周数                                                                                          | Ulong  | 4      | H+24     |
| 7   | ulWNlsf     | 新的闰秒值生效 Galileo 周计数                                                                         | Ulong  | 4      | H+28     |
|  8  |  dn         | 新的闰秒生效的周内日计数（范 围为 1 到 7，周日=1，周六=7）                                            |  Ulong |  4     |  H+32    |
|  9  |  deltat lsf | 新的闰秒生效后 Galileo 时相对于 UTC 的累积闰秒改正数                                                  |  Long  |  4     |  H+36    |
|  10 |  dA0g       | Galileo时间系统与GPST系统转换 参数常数项                                                              |  Long  |  8     |  H+40    |
|  11 |  dA1g       | Galileo时间系统与GPST系统转换 参数的1阶项                                                             |  Ulong |  8     |  H+48    |
|  12 |  ulT0g      | Galileo 时间系统与 GPST 系统转 换参考周内秒                                                           |  Ulong |  4     |  H+56    |
|  13 |  ulWN0g     | Galileo 时间系统与 GPST 系统转 换参考周计数                                                           |  Ulong |  4     |  H+60    |
| 14  | xxxx        | 32 位 CRC 校验                                                                                        | Hex    | 4      | H+64     |
| 15  | [CR][LF]    | 语句结束符(仅 ASCII)                                                                                  | -      | -      | -        |

#### GPSEPH GPS 星历数据

本消息包含 GPS 星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 106

ASCII 输出语法:

GPSEPHA COM1 60

GPSEPHA COM1 ONCHANGED

BINARY 输出语法:

GPSEPHB COM1 60

GPSEPHB COM1 ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出:

\#GPSEPHA,97,GPS,FINE,2190,362528000,0,0,18,1;10,360210.0,0,30,30,2190,2190,3 67200.0,2.656037435e+07,4.374825086e-09,4.615227840e-01,7.3941934388e-03,-2.548

7093877e+00,0.000000000e+00,9.177252650e-06,2.07281250e+02,-1.78125000e+00,-2.

048909664e-08,1.136213541e-07,9.7216383679e-01,4.053740283e-10,-2.969634463e-0

3,-7.97997526e-09,30,367200.0,2.328306437e-09,-2.8089155e-04,-9.3223207e-12,0.000

0000e+00,TRUE,1.458581356e-04,4.00000000e+00\*ef6608ff

表 7-73 GPSEPH 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型 | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|------|--------|----------|
|   1 |  GPSEPH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |      |   H    |   0      |

| ID  | 字段     | 数据描述                                                             | 类型    | 字节数 | 字节偏移 |
|-----|----------|----------------------------------------------------------------------|---------|--------|----------|
|   2 |   PRN    | 卫星 PRN 编号 GPS：1 到 32 QZSS：33 到 42                            |   Ulong |   4    |   H      |
| 3   | Tow      | 子帧 0 的时间戳，s                                                   | Double  | 8      | H+4      |
|  4  |  health  | 健康状态-ICD-GPS-200a 中定义的 6 位健康代码                          |  Ulong  |  4     |  H+12    |
| 5   | IODE1    | 星历数据 1 龄期                                                      | Ulong   | 4      | H+16     |
| 6   | IODE2    | 星历数据 2 龄期= GPS 的 IODE1                                        | Ulong   | 4      | H+20     |
| 7   | Week     | GPS 周数（GPS Week）                                                 | Ulong   | 4      | H+24     |
|   8 |   Z Week | Z 计数的周数，为星历表的子帧 1 的周数。“TOW 周”（字段\#7）来源于此。 |   Ulong |   4    |   H+28   |
| 9   | Toe      | 星历的参考时间，s                                                    | Double  | 8      | H+32     |
| 10  | A        | 卫星轨道长半轴，m                                                    | Double  | 8      | H+40     |
| 11  | ΔN       | 卫星平均角速度的改正值，rad/s                                        | Double  | 8      | H+48     |
| 12  | M0       | TOE 时间的平近点角，rad                                              | Double  | 8      | H+56     |
| 13  | Ecc      | 卫星轨道偏心率                                                       | Double  | 8      | H+64     |
| 14  | ω        | 近地点幅角，rad                                                      | Double  | 8      | H+72     |
| 15  | cuc      | 纬度幅角（余弦振幅，rad）                                            | Double  | 8      | H+80     |
| 16  | cus      | 纬度幅角（正弦振幅，rad）                                            | Double  | 8      | H+88     |
| 17  | crc      | 轨道半径（余弦振幅，m）                                              | Double  | 8      | H+96     |
| 18  | crs      | 轨道半径（正弦振幅，m）                                              | Double  | 8      | H+104    |
| 19  | cic      | 倾角（余弦振幅，rad）                                                | Double  | 8      | H+112    |
| 20  | cis      | 倾角（正弦振幅，rad）                                                | Double  | 8      | H+120    |
| 21  | I0       | TOE 时间轨道倾角，rad                                                | Double  | 8      | H+128    |
| 22  | IDOT     | 轨道倾角变化率，rad/s                                                | Double  | 8      | H+136    |
| 23  | Ω0       | 升交点赤经，rad                                                      | Double  | 8      | H+144    |

| ID    | 字段     | 数据描述                                                                                                                 | 类型      | 字节数 | 字节偏移 |
|-------|----------|--------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------|
| 24    | Ω dot    | 升交点赤经变化率，rad/s                                                                                                  | Double    | 8      | H+152    |
| 25    | iodc     | 时钟数据龄期                                                                                                             | Ulong     | 4      | H+160    |
| 26    | toc      | 卫星钟差参考时间，s                                                                                                      | Double    | 8      | H+164    |
| 27    | tgd      | 群延迟，s                                                                                                                | Double    | 8      | H+172    |
| 28    | af0      | 卫星钟差参数，s                                                                                                          | Double    | 8      | H+180    |
| 29    | af1      | 卫星钟速参数，s/s                                                                                                        | Double    | 8      | H+188    |
| 30    | af2      | 卫星钟漂参数，s/s/s                                                                                                      | Double    | 8      | H+196    |
|   31  |   AS     | 反欺骗： 0 = FALSE 1 = TRUE                                                                                              |   Enum    |   4    |   H+204  |
| 32    | N        | 改正平均角速度，rad/s                                                                                                    | Double    | 8      | H+208    |
|    33 |    URA   | 用户距离精度，m2。ICD 中给出了一种算法将原始星历中传输的 URAI指数转化为名义标准差值。此处输 出这一名义值的平方（方差）。 |    Double |    8   |    H+216 |
| 34    | xxxx     | 32 位 CRC 校验                                                                                                           | Hex       | 4      | H+224    |
| 35    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                     | -         | -      | -        |

#### QZSSEPH QZSS 星历

本消息包含 QZSS 星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 110

ASCII 输出语法:

QZSSEPHA COM1 60 QZSSEPHA COM1 ONCHANGED

BINARY 输出语法:

QZSSEPHB COM1 60 QZSSEPHB COM1 ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出:

\#QZSSEPHA,78,GPS,FINE,2262,368756700,0,0,18,16;4,368730.0,0,185,185,2262,22 62,370800.0,4.216498367e+07,2.569749898e-09,1.905190738e+00,7.5245622196e-02,-

1.5526664328e+00,1.514703035e-05,3.799796104e-06,-3.61250000e+01,4.70875000e+

02,3.501772881e-07,2.438202500e-06,6.1294064513e-01,4.364467512e-10,-2.35410799

9e+00,-1.81507561e-09,953,370800.0,-3.725290298e-09,9.4612129e-05,2.2737368e-13,

0.0000000e+00,FALSE,7.292162191e-05,7.84000000e+00\*7c79248b

表 7-74 QZSSEPH 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  QZSSEPH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |         |   H    |   0      |
|  2  |  PRN            | 卫星 PRN 编号 QZSS：1 到 10                                                                           |  Ulong  |  4     |  H       |
| 3   | Tow             | 子帧 0 的时间戳，s                                                                                    | Double  | 8      | H+4      |
|  4  |  health         | 健康状态-ICD-GPS-200a 中定义的 6 位健康代码                                                           |  Ulong  |  4     |  H+12    |
| 5   | IODE1           | 星历数据 1 龄期                                                                                       | Ulong   | 4      | H+16     |
| 6   | IODE2           | 星历数据 2 龄期= GPS 的 IODE1                                                                         | Ulong   | 4      | H+20     |
| 7   | Week            | GPS 周数（GPS Week）                                                                                  | Ulong   | 4      | H+24     |
|   8 |   Z Week        | Z 计数的周数，为星历表的子帧 1 的周数。“TOW 周”（字段\#7）来源于此。                                  |   Ulong |   4    |   H+28   |
| 9   | Toe             | 星历的参考时间，s                                                                                     | Double  | 8      | H+32     |

| ID   | 字段  | 数据描述                      | 类型   | 字节数 | 字节偏移 |
|------|-------|-------------------------------|--------|--------|----------|
| 10   | A     | 卫星轨道长半轴，m             | Double | 8      | H+40     |
| 11   | ΔN    | 卫星平均角速度的改正值，rad/s | Double | 8      | H+48     |
| 12   | M0    | TOE 时间的平近点角，rad       | Double | 8      | H+56     |
| 13   | Ecc   | 卫星轨道偏心率                | Double | 8      | H+64     |
| 14   | ω     | 近地点幅角，rad               | Double | 8      | H+72     |
| 15   | cuc   | 纬度幅角（余弦振幅，rad）     | Double | 8      | H+80     |
| 16   | cus   | 纬度幅角（正弦振幅，rad）     | Double | 8      | H+88     |
| 17   | crc   | 轨道半径（余弦振幅，m）       | Double | 8      | H+96     |
| 18   | crs   | 轨道半径（正弦振幅，m）       | Double | 8      | H+104    |
| 19   | cic   | 倾角（余弦振幅，rad）         | Double | 8      | H+112    |
| 20   | cis   | 倾角（正弦振幅，rad）         | Double | 8      | H+120    |
| 21   | I0    | TOE 时间轨道倾角，rad         | Double | 8      | H+128    |
| 22   | IDOT  | 轨道倾角变化率，rad/s         | Double | 8      | H+136    |
| 23   | Ω0    | 升交点赤经，rad               | Double | 8      | H+144    |
| 24   | Ω dot | 升交点赤经变化率，rad/s       | Double | 8      | H+152    |
| 25   | iodc  | 时钟数据龄期                  | Ulong  | 4      | H+160    |
| 26   | toc   | 卫星钟差参考时间，s           | Double | 8      | H+164    |
| 27   | tgd   | 群延迟，s                     | Double | 8      | H+172    |
| 28   | af0   | 卫星钟差参数，s               | Double | 8      | H+180    |
| 29   | af1   | 卫星钟速参数，s/s             | Double | 8      | H+188    |
| 30   | af2   | 卫星钟漂参数，s/s/s           | Double | 8      | H+196    |
|   31 |   AS  | 反欺骗： 0 = FALSE 1 = TRUE   |   Enum |   4    |   H+204  |
| 32   | N     | 改正平均角速度，rad/s         | Double | 8      | H+208    |

| ID    | 字段     | 数据描述                                                                                                                 | 类型      | 字节数 | 字节偏移 |
|-------|----------|--------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|    33 |    URA   | 用户距离精度，m2。ICD 中给出了一种算法将原始星历中传输的 URAI指数转化为名义标准差值。此处输 出这一名义值的平方（方差）。 |    Double |    8   |    H+216 |
| 34    | xxxx     | 32 位 CRC 校验                                                                                                           | Hex       | 4      | H+224    |
| 35    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                     | -         | -      | -        |

#### BD3EPH 北斗 3 代星历

本消息包含 BD3 星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 2999

ASCII 输出语法:

BD3EPHA COM1 60

BD3EPHA COM1 ONCHANGED

BINARY 输出语法:

BD3EPHB COM1 60

BD3EPHB COM1 ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM960、UMD960、UM982、 UMD982

消息输出:

\#BD3EPHA,77,GPS,FINE,2211,180091000,0,0,18,4;44,0,3,15,21,21,2211,2211,17640 0.0,176400.0,-1.423828125e+01,1.108884811e-02,3.726583799e-09,-1.069685670e-13,

1.309681137e+00,8.019023808e-04,6.109550176e-01,2.244487405e-07,8.259899914e-0

6,1.940156250e+02,6.187500000e+00,1.210719347e-08,7.450580597e-09,9.593903595 e-01,-4.500187451e-11,1.952617584e+00,-6.803497679e-09,176400.0,-2.153683454e-0 9,-1.199077815e-08,0.000000000e+00,0.000000000e+00,0.000000000e+00,-2.91038304

6e-10,6.693656906e-04,1.219113699e-11,0.000000000e+00,588,0,27,0,7,0,0,1\*b90d956

6

表 7-75 BD3EPH 数据结构

| ID   | 字段          | 数据描述                                                                                              | 类型     | 字节数 | 字节偏移 |
|------|---------------|-------------------------------------------------------------------------------------------------------|----------|--------|----------|
|  1   | BD3EPH header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |          |  H     |  0       |
| 2    | PRN           | 卫星 PRN 编号（BDS 1 到 63）                                                                          | UChar    | 1      | H        |
|  3   |  Health       | 卫星健康状态，0=healthy， 1=unhealthy                                                                 |  UChar   |  1     |  H+1     |
|    4 |    SatType    | 卫星类别（GEO/MEO/IGSO） “1” 代表 GEO “2” 代表 IGSO “3” 代表 MEO                                      |    UChar |    1   |    H+2   |
| 5    | SISMAI        | 空间信号监测精度                                                                                      | UChar    | 1      | H+3      |
|   6  |   IODE        | 当输出 B1C 或 B2A 星历时，该字 段为星历数据龄期；当输出 B2b星历时，该字段为保留位                     |   UShort |   2    |   H+4    |
|   7  |   IODC        | 当输出 B1C 或 B2A 星历时，该字段为时钟数据龄期；当输出 B2b 星历时，该字段为保留位                     |   UShort |   2    |   H+6    |
| 8    | Week          | GPS 周计数（GPS Week）                                                                                | UShort   | 2      | H+8      |
|  9   |  Zweek        | 基于 GPS 周的 Z 计数周期，为星 历子帧 1 的周数（TOE 周）                                              |  UShort  |  2     |  H+10    |
| 10   | Tow           | 子帧 1 的时间标识（秒）                                                                               | Double   | 8      | H+12     |
| 11   | Toe           | 星历参考时刻，单位 s                                                                                  | Double   | 8      | H+20     |

| ID   | 字段      | 数据描述                                                         | 类型     | 字节数 | 字节偏移 |
|------|-----------|------------------------------------------------------------------|----------|--------|----------|
|  12  |  DeltaA   | 参考时刻长半轴相对于参考值的偏 差（米）                          |  Double  |  8     |  H+28    |
| 13   | dDeltaA   | 长半轴变化率（米/秒）                                            | Double   | 8      | H+36     |
|  14  |  ΔN       | 参考时刻卫星平均角速度与计算值 之差（Radians/second）            |  Double  |  8     |  H+44    |
|   15 |   dΔN     | 参考时刻卫星平均角速度与计算值之差的变化率 （Radians/second\^2） |   Double |   8    |   H+52   |
| 16   | M0        | 参考时刻的平近点角（Radians）                                    | Double   | 8      | H+60     |
| 17   | Ecc       | 偏心率                                                           | Double   | 8      | H+68     |
| 18   | ω         | 近地点幅角，rad                                                  | Double   | 8      | H+76     |
| 19   | Cuc       | 纬度幅角（余弦振幅，rad）                                        | Double   | 8      | H+84     |
| 20   | Cus       | 纬度幅角（正弦振幅，rad）                                        | Double   | 8      | H+92     |
| 21   | crc       | 轨道半径（余弦振幅，m）                                          | Double   | 8      | H+100    |
| 22   | crs       | 轨道半径（正弦振幅，m）                                          | Double   | 8      | H+108    |
| 23   | cic       | 轨道倾角（余弦振幅，rad）                                        | Double   | 8      | H+116    |
| 24   | cis       | 轨道倾角（正弦振幅，rad）                                        | Double   | 8      | H+124    |
| 25   | I0        | 参考时时刻轨道倾角，rad                                          | Double   | 8      | H+132    |
| 26   | IDOT      | 轨道倾角变化率，rad/s                                            | Double   | 8      | H+140    |
| 27   | Ω0        | 升交点赤经，rad                                                  | Double   | 8      | H+148    |
| 28   | Ω dot     | 升交点赤经变化率，rad/s                                          | Double   | 8      | H+156    |
| 29   | toc       | 卫星钟差参考时间, seconds                                        | Double   | 8      | H+164    |
| 30   | Tgdb1cp   | B1C 导频分量时延差, seconds                                      | Double   | 8      | H+172    |
| 31   | Tgdb2ap   | B2A 导频分量时延差, seconds                                      | Double   | 8      | H+180    |
| 32   | Tgdb2bI\* | B2b I 支路时延差, seconds                                        | Double   | 8      | H+188    |
| 33   | Tgdb2bQ\* | B2b Q 支路时延差, seconds                                        | Double   | 8      | H+196    |

\* Build7160 与 Build7676 版本不支持

| ID   | 字段       | 数据描述                                                                                  | 类型    | 字节数 | 字节偏移 |
|------|------------|-------------------------------------------------------------------------------------------|---------|--------|----------|
|  34  |  ISCb2ad   | B2A 数据分量相对于 B2A 导频分 量的时延修正项, seconds                                     |  Double |  8     |  H+204   |
|  35  |  ISCb1cd   | B1C 数据分量相对于 B1C 导频分 量的时延修正项, seconds                                     |  Double |  8     |  H+212   |
| 36   | af0        | 卫星钟差参数，秒                                                                          | Double  | 8      | H+220    |
| 37   | af1        | 卫星钟漂参数，s/s                                                                         | Double  | 8      | H+228    |
| 38   | af2        | 卫星钟漂变化率参数，s/s2                                                                  | Double  | 8      | H+236    |
| 39   | iTop       | 数据预测的周内时刻                                                                        | INT     | 4      | H+244    |
| 40   | SISAIoe    | 卫星轨道的切向和法向精度指数                                                              | UChar   | 1      | H+248    |
|  41  |  SISAIocb  | 卫星轨道的径向及卫星钟固定偏差 精度指数                                                   |  UChar  |  1     |  H+249   |
| 42   | SISAIoc1   | 卫星钟频偏精度指数                                                                        | UChar   | 1      | H+250    |
| 43   | SISAIoc2   | 卫星钟频漂精度指数                                                                        | UChar   | 1      | H+251    |
| 44   | Reserved   | 保留位                                                                                    | INT     | 4      | H+252    |
| 45   | Reserved   | 保留位                                                                                    | INT     | 4      | H+256    |
|   46 |   FreqType | 为 0 时，该消息代表 B1C 星历；为 1 时，该消息代表 B2A 星历； 为 2 时，该消息代表 B2b 星历 |   UINT  |   4    |   H+260  |
|  47  |  xxxx      | 32 位 CRC 校验(仅 ASCII 和二进 制)                                                        |  Hex    |  4     |  H+264   |
| 48   | [CR][LF]   | 语句结束符（仅 ASCII）                                                                    | -       | -      | -        |

#### BDSEPH 北斗星历数据

本消息包含北斗星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 108

ASCII 输出语法:

BDSEPHA COM1 60

BDSEPHA COM1 ONCHANGED

BINARY 输出语法:

BDSEPHB COM1 60

BDSEPHB COM1 ONCHANGED

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出:

\#BDSEPHA,97,GPS,FINE,2190,362675000,0,0,18,5;60,360000.0,0,1,1,2190,2190,360 000.0,4.216441036e+07,-4.103028050e-09,2.042808580e+00,3.8967351429e-05,2.4660

025037e+00,-1.457566395e-05,-2.235500142e-05,6.85031250e+02,-4.52843750e+02,1.4

38893378e-07,-1.206062734e-07,1.2597663760e-01,1.132190017e-10,-1.993009969e+0

0,5.03270963e-09,1,360000.0,4.980000000e-08,4.980000000e-08,-1.45519e-07,8.26006 e-14,0.00000e+00,TRUE,7.291643104e-05,4.00000000e+00\*493bb7fb

表 7-76 BDSEPH 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  BDSEPH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |         |   H    |   0      |
| 2   | PRN            | 卫星 PRN 编号（BDS：1 到 63）                                                                         | Ulong   | 4      | H        |
|  3  |  Tow           | 子帧 1 的时间标识（基于 GPS 时 间），s                                                                |  Double |  8     |  H+4     |
|  4  |  Health        | 健康状态–在北斗 ICD 中定义的一 个 1 比特的健康代码                                                    |  Ulong  |  4     |  H+12    |
| 5   | AODE           | 星历数据龄期                                                                                          | Ulong   | 4      | H+16     |

| ID   | 字段      | 数据描述                                                                                     | 类型     | 字节数 | 字节偏移 |
|------|-----------|----------------------------------------------------------------------------------------------|----------|--------|----------|
| 6    | AODE      | 星历数据龄期（同字段 5）                                                                     | Ulong    | 4      | H+20     |
| 7    | Week      | GPS 周计数（GPS Week）                                                                       | Ulong    | 4      | H+24     |
|    8 |    Z Week | 基于 GPS 周的 Z 计数周数，为星历子帧 1 的周数。“TOE 周” （字段\#7）来源于此，用来说明 滚转。 |    Ulong |    4   |    H+28  |
| 9    | Toe       | 星历参考时刻，单位 s                                                                         | Double   | 8      | H+32     |
| 10   | A         | 轨道长半轴，m                                                                                | Double   | 8      | H+40     |
| 11   | ΔN        | 卫星平均角速度的改正值，rad/s                                                                | Double   | 8      | H+48     |
| 12   | M0        | 参考时间的平近点角，rad                                                                      | Double   | 8      | H+56     |
| 13   | Ecc       | 偏心率                                                                                       | Double   | 8      | H+64     |
| 14   | ω         | 近地点幅角，rad                                                                              | Double   | 8      | H+72     |
| 15   | Cuc       | 纬度幅角（余弦振幅，rad）                                                                    | Double   | 8      | H+80     |
| 16   | Cus       | 纬度幅角（正弦振幅，rad）                                                                    | Double   | 8      | H+88     |
| 17   | crc       | 轨道半径（余弦振幅，m）                                                                      | Double   | 8      | H+96     |
| 18   | crs       | 轨道半径（正弦振幅，m）                                                                      | Double   | 8      | H+104    |
| 19   | cic       | 倾角（余弦振幅，rad）                                                                        | Double   | 8      | H+112    |
| 20   | cis       | 倾角（正弦振幅，rad）                                                                        | Double   | 8      | H+120    |
| 21   | I0        | 参考时时刻轨道倾角，rad                                                                      | Double   | 8      | H+128    |
| 22   | IDOT      | 轨道倾角变化率，rad/s                                                                        | Double   | 8      | H+136    |
| 23   | Ω0        | 升交点赤经，rad                                                                              | Double   | 8      | H+144    |
| 24   | Ω dot     | 升交点赤经变化率，rad/s                                                                      | Double   | 8      | H+152    |
| 25   | AODC      | 时钟数据龄期                                                                                 | Ulong    | 4      | H+160    |
|  26  |  toc      | 卫星钟差参考时间（基于 GPS 时 间），s                                                        |  Double  |  8     |  H+164   |
|  27  |  tgd1     | B1 群延迟（B1 星上设备时延 差），s                                                           |  Double  |  8     |  H+172   |

| ID    | 字段     | 数据描述                                                                                                                  | 类型      | 字节数 | 字节偏移 |
|-------|----------|---------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|  28   |  tgd2    | B2 群延迟（B2 星上设备时延 差），s                                                                                        |  Double   |  8     |  H+180   |
| 29    | af0      | 卫星钟差参数，s                                                                                                           | Double    | 8      | H+188    |
| 30    | af1      | 卫星钟速参数，s/s                                                                                                         | Double    | 8      | H+196    |
| 31    | af2      | 卫星钟漂参数，s/s/s                                                                                                       | Double    | 8      | H+204    |
|   32  |   AS     | 反欺骗： 0 = FALSE 1 = TRUE                                                                                               |   Enum    |   4    |   H+212  |
| 33    | N        | 改正平均角速度，rad/s                                                                                                     | Double    | 8      | H+216    |
|    34 |    URA   | 用户距离精度，m2。ICD 中给出了一种算法将原始星历中传输的 URAI 指数转化为名义标准差值。此处输出这一名义值的平方（方 差）。 |    Double |    8   |    H+224 |
|  35   |  xxxx    | 32 位 CRC 校验(仅 ASCII 和二进 制)                                                                                        |  Hex      |  4     |  H+232   |
| 36    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                      | -         | -      | -        |

#### GLOEPH GLONASS 星历数据

本消息包含 GLONASS 星历数据。GLONASS 星历数据参考 PZ90.02 大地基准。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 107

ASCII 输出语法:

GLOEPHA COM1 60

GLOEPHA COM1 ONCHANGED

BINARY 输出语法:

GLOEPHB COM1 60

GLOEPHB COM1 ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GLOEPHA,88,GPS,FINE,2305,116282000,0,0,18,30;40,12,1,0,2305,114318000,1078 2,71,0,0,43,0,1.890321777343750e+06,-1.100072509765625e+07,2.298513378906250e+

07,3.121249198913574e+03,-2.802515029907227e+02,-3.969745635986328e+02,-0.000

000931322575,-2.793967723846436e-06,-2.793967723846436e-06,-9.61646437644958

5e-05,-2.793967724e-09,9.094947017729282e-13,38040,2,3,0,12\*2f2935b8

表 7-77 GLOEPH 数据结构

| ID    | 字段           | 数据描述                                                                                              | 类型      | 字节数 | 字节偏移 |
|-------|----------------|-------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|   1   |  GLOEPH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |           |   H    |   0      |
|  2    |  Sloto         | 通道编号，转换为 PRN 号是 （Slot + 37）                                                               |  Ushort   |  2     |  H       |
| 3     | freqo          | 频率编号，范围为 0 到 20                                                                              | Ushort    | 2      | H+2      |
|     4 |     sat type   | 卫星类型 0 = GLO_SAT 1 = GLO_SAT_M （M 型卫星） 2 = GLO_SAT_K（K 型卫 星）                            |     Uchar |     1  |     H+4  |
| 5     | Reserved       |                                                                                                       |           | 1      | H+5      |
|  6    |  e week        | 星历参考时刻，整周数 （GPS Week）                                                                     |  Ushort   |  2     |  H+6     |

| ID   | 字段        | 数据描述                                                               | 类型     | 字节数 | 字节偏移 |
|------|-------------|------------------------------------------------------------------------|----------|--------|----------|
|  7   |  e time     | 星历参考时刻，ms（相对于 GPS 时间）                                    |  Ulong   |  4     |  H+8     |
|    8 |    t offset | GPS 和 GLONASS 时间之间的整数秒。正值表明 GLONASS 时间先于 GPS 时 间。 |    Ulong |    4   |    H+12  |
|  9   |  Nt         | 当前天数，从每个闰年一月 的第一天开始的天计数。                        |  Ushort  |  2     |  H+16    |
| 10   | Reserved    | 保留                                                                   |          | 1      | H+18     |
| 11   | Reserved    | 保留                                                                   |          | 1      | H+19     |
|  12  |  issue      | 相对星历参考时刻的 15 分 钟间隔数                                      |  Ulong   |  4     |  H+20    |
|   13 |   health    | 星历健康 0 = healthy 1 = unhealthy                                     |   Ulong  |   4    |   H+24   |
|  14  |  pos x      | 参考时刻卫星的 X 坐标 （PZ-90.02），m                                  |  Double  |  8     |  H+28    |
|  15  |  pos y      | 参考时刻卫星的 Y 坐标 （PZ-90.02），m                                  |  Double  |  8     |  H+36    |
|  16  |  pos z      | 参考时刻卫星的 Z 坐标 （PZ-90.02），m                                  |  Double  |  8     |  H+44    |
|  17  |  vel x      | 参考时刻卫星速度的 X 坐标 （PZ-90.02），m/s                            |  Double  |  8     |  H+52    |
|  18  |  vel y      | 参考时刻卫星速度的 Y 坐标 （PZ-90.02），m/s                            |  Double  |  8     |  H+60    |
|  19  |  vel z      | 参考时刻卫星速度的 Z 坐标 （PZ-90.02），m/s                            |  Double  |  8     |  H+68    |

| ID   | 字段          | 数据描述                                                                    | 类型     | 字节数 | 字节偏移 |
|------|---------------|-----------------------------------------------------------------------------|----------|--------|----------|
|  20  |  LS acc x     | 参考时刻日月摄动加速度的 X 坐标（PZ-90.02），m/s2                           |  Double  |  8     |  H+76    |
|  21  |  LS acc y     | 参考时刻日月摄动加速度的 Y 坐标（PZ-90.02），m/s2                           |  Double  |  8     |  H+84    |
|  22  |  LS acc z     | 参考时刻日月摄动加速度的 Z 坐标（PZ-90.02），m/s2                           |  Double  |  8     |  H+92    |
|   23 |   tau_n       | 修正第 n 个相对于 GLONASS 时间 t_c 的卫星 时间 t_n，s                       |   Double |   8    |   H+100  |
|   24 |   delta_tau_n | 第 n 个卫星的 L2 RF 信号相对于 L1 RF 信号的传输延 迟，s                     |   Double |   8    |   H+108  |
| 25   | gamma         | 频率校正，s/s                                                               | Double   | 8      | H+116    |
|  26  |  Tk           | 帧起始时刻（从 GLONASS 日开始），s                                          |  Ulong   |  4     |  H+124   |
| 27   | P             | 技术参数                                                                    | Ulong    | 4      | H+128    |
| 28   | Ft            | 用户测距精度预测                                                            | Ulong    | 4      | H+132    |
| 29   | age           | 数据龄期，day                                                               | Ulong    | 4      | H+136    |
|  30  |  Flags        | 信息标识，参考[表7-78](#_bookmark258) [GLONASS 星历标志代码](#_bookmark258) |  Ulong   |  4     |  H+140   |
| 31   | xxxx          | 32 位 CRC 校验                                                              | Hex      | 4      | H+144    |
| 32   | [CR][LF]      | 语句结束符(仅 ASCII)                                                        | -        | -      | -        |

表 7-78 GLONASS 星历标志代码

| bit | 描述                              | 取值                                                           | 掩码     |
|-----|-----------------------------------|----------------------------------------------------------------|----------|
| 0   |  P1，两个相邻的 tb 参数的时间间隔 | 参考[表 7-79 P1 标志](#_bookmark259) [取值范围](#_bookmark259) | 00000001 |
| 1   |                                   |                                                                | 00000002 |
| 2   | P2，tb 参数的奇偶标志             | 0=even，1=odd                                                  | 00000004 |

| bit | 描述                             | 取值     | 掩码     |
|-----|----------------------------------|----------|----------|
| 3   | P3，当前帧的历书中所包含的卫星数 | 0=4，1=5 | 00000008 |
| 4   |   保留                           |          |          |
| …   |                                  |          |          |
| 31  |                                  |          |          |

表 7-79 P1 标志取值范围

| 状态 | 描述    |
|------|---------|
| 00   | 0 分钟  |
| 01   | 30 分钟 |
| 10   | 45 分钟 |
| 11   | 60 分钟 |

#### GALEPH 伽利略星历数据

本消息包含伽利略星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 109

ASCII 输出语法:

GALEPHA COM1 60

GALEPHA COM1 ONCHANGED

BINARY 输出语法:

GALEPHB COM1 60

GALEPHB COM1 ONCHANGED

适用产品：UM960、UM960L、UM980、UB9A0、UM982

消息输出：

\#GALEPHA,97,GPS,FINE,2190,363656000,0,0,18,3;36,TRUE,TRUE,0,0,0,0,0,0,107,0, 82,356400,5.44061113e+03,2.4787e-09,-1.46715796e+00,2.844742266e-04,-1.32564659

1e+00,-8.5607e-06,9.0413e-06,1.590e+02,-1.839e+02,9.3132e-09,-3.9116e-08,9.965504

471e-01,-2.6823e-10,-1.201660091e+00,-5.44451250e-09,356400,-3.108567325e-04,-5.3

57492e-12,0.0e+00,356400,-3.108558012e-04,-5.357492e-12,0.0e+00,5.821e-09,6.752e-

09\*e8487c09

表 7-80 GALEPH 数据结构

| ID  | 字段           | 数据描述                                                                                                | 类型   | 字节数 | 字节偏移 |
|-----|----------------|---------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  GALEPH header | 消息头，二进制消息头结构请参考 [表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表 7-51](#_bookmark211) |        |   H    |   0      |
|  2  |  SatId         | 卫星 ID 编号； （Galileo：1 到 36）                                                                     |  Ulong |  4     |  H       |
| 3   | FNAVReceived   | 接收到 FNAV 星历数据的标识                                                                              | Bool   | 4      | H+4      |
| 4   | INAVReceived   | 接收到 INAV 星历数据的标识                                                                              | Bool   | 4      | H+8      |
|  5  |  E1BHealth     | E1b 健康状态（当 INAVReceived 值为“真”时有效）                                                          |  Uchar |  1     |  H+12    |
|  6  |  E5aHealth     | E5a 健康状态（当 FNAVReceived 值为“真”时有效）                                                          |  Uchar |  1     |  H+13    |
|  7  |  E5bHealth     | E5b 健康状态（当 INAVReceived 值为“真”时有效）                                                          |  Uchar |  1     |  H+14    |
|  8  |  E1BDVS        | E1b 数据有效状态（当 INAVReceived 值为“真”时有效）                                                      |  Uchar |  1     |  H+15    |
|  9  |  E5aDVS        | E5a 数据有效状态（当 FNAVReceived 值为“真”时有效）                                                      |  Uchar |  1     |  H+16    |
|  10 |  E5bDVS        | E5b 数据有效状态（当 INAVReceived 值为“真”时有效）                                                      |  Uchar |  1     |  H+17    |
| 11  | SISA           | 空间信号精度                                                                                            | Uchar  | 1      | H+18     |

| ID  | 字段     | 数据描述                                                 | 类型    | 字节数 | 字节偏移 |
|-----|----------|----------------------------------------------------------|---------|--------|----------|
| 12  | Reserved | 保留                                                     | Uchar   | 1      | H+19     |
| 13  | IODNav   | 星历数据期号                                             | Ulong   | 4      | H+20     |
| 14  | Toe      | 星历的参考时间，单位：秒                                 | Ulong   | 4      | H+24     |
| 15  | RootA    | 卫星轨道长半轴（根数），m1/2                             | Double  | 8      | H+28     |
| 16  | DeltaN   | 卫星平均角速度的改正值，rad/s                            | Double  | 8      | H+36     |
| 17  | M0       | TOE 时间的平近点角，rad                                  | Double  | 8      | H+44     |
| 18  | Ecc      | 卫星轨道偏心率                                           | Double  | 8      | H+52     |
| 19  | Omega    | 近地点幅角，rad                                          | Double  | 8      | H+60     |
| 20  | Cuc      | 纬度幅角（余弦振幅，rad）                                | Double  | 8      | H+68     |
| 21  | Cus      | 纬度幅角（正弦振幅，rad）                                | Double  | 8      | H+76     |
| 22  | Crc      | 轨道半径（余弦振幅，m）                                  | Double  | 8      | H+84     |
| 23  | Crs      | 轨道半径（正弦振幅，m）                                  | Double  | 8      | H+92     |
| 24  | Cic      | 倾角（余弦振幅，rad）                                    | Double  | 8      | H+100    |
| 25  | Cis      | 倾角（正弦振幅，rad）                                    | Double  | 8      | H+108    |
| 26  | I0       | TOE 时间轨道倾角，rad                                    | Double  | 8      | H+116    |
| 27  | IDot     | 轨道倾角变化率，rad/s                                    | Double  | 8      | H+124    |
| 28  | Omega0   | 升交点赤经，rad                                          | Double  | 8      | H+132    |
| 29  | OmegaDot | 升交点赤经变化率，rad/s                                  | Double  | 8      | H+140    |
|  30 |  FNAVT0c | 卫星钟差参数，s，（当 FNAVReceived 值为“真”时有效）      |  Ulong  |  4     |  H+148   |
|  31 |  FNAVAf0 | 卫星钟差参数，s，（当 FNAVReceived 值为“真”时有效）      |  Double |  8     |  H+152   |
|  32 |  FNAVAf1 | 卫星钟速参数，s/s，（当 FNAVReceived 值为“真”时有效）    |  Double |  8     |  H+160   |
|  33 |  FNAVAf2 | 卫星钟漂参数，s/s\^2，（当 FNAVReceived 值为“真”时有效） |  Double |  8     |  H+168   |

| ID  | 字段      | 数据描述                                                 | 类型    | 字节数 | 字节偏移 |
|-----|-----------|----------------------------------------------------------|---------|--------|----------|
|  34 |  INAVT0c  | 卫星钟差参数，s，（当 INAVReceived 值为“真”时有效）      |  Ulong  |  4     |  H+176   |
|  35 |  INAVAf0  | 卫星钟差参数，s，（当 INAVReceived 值为“真”时有效）      |  Double |  8     |  H+180   |
|  36 |  INAVAf1  | 卫星钟速参数，s/s，（当 INAVReceived 值为“真”时有效）    |  Double |  8     |  H+188   |
|  37 |  INAVAf2  | 卫星钟漂参数，s/s\^2，（当 INAVReceived 值为“真”时有效） |  Double |  8     |  H+196   |
| 38  | E1E5aBGD  | E1, E5a 广播群延迟                                       | Double  | 8      | H+204    |
|  39 |  E1E5bBGD | E1, E5b 广播群延迟，（当 INAVReceived 值为“真”时有效）   |  Double |  8     |  H+212   |
| 40  | xxxx      | 32 位 CRC 校验                                           | Hex     | 4      | H+220    |
| 41  | [CR][LF]  | 语句结束符(仅 ASCII)                                     | -       |        | -        |

#### IRNSSEPH IRNSS 星历数据

本消息包含 IRNSS 星历数据。当使用固定频率输出时，由于星历信息数据量较大，配置输出时间间隔推荐大于 60 秒，不宜按 1Hz 输出。当配合 50Hz 观测值输出时，建议使用 ONCHANGED 请求方式。

Message ID: 112

ASCII 输出语法:

IRNSSEPHA COM1 60 IRNSSEPHA COM1 ONCHANGED

BINARY 输出语法:

IRNSSEPHB COM1 60 IRNSSEPHB COM1 ONCHANGED

适用产品：UM980、UB9A0

消息输出:

\#IRNSSEPHA,87,GPS,FINE,2305,116273000,0,0,18,31;2,9685.0,0,193,0,2305,0,1155 36.0,4.216456644e+07,4.968778398e-09,-1.455813652e+00,2.0113651408e-03,3.05230

21218e+00,2.138316631e-05,-2.254918218e-05,7.77500000e+02,6.59937500e+02,-2.34

6932888e-07,-2.123415470e-07,5.0866932453e-01,4.564475843e-10,1.506952289e+00,

\-4.93877715e-09,0,115536.0,-1.862645149e-09,6.0655642e-05,2.3760549e-11,0.000000 0e+00,0,7.292510329e-05,4.0\*298210c8

表 7-81 IRNSSEPH 数据结构

| ID  | 字段            | 数据描述                                                                                                               | 类型    | 字节数 | 字节偏移 |
|-----|-----------------|------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|  1  | IRNSSEPH header | 消息头，二进制消息头结构请参考[表](#_bookmark210) [7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |         |  H     |  0       |
| 2   | PRN             | 卫星 PRN 编号 IRNSS：1 到 15                                                                                           | Ulong   | 4      | H        |
|  3  |  TOWC           | 子帧 1 的时间戳，TOWC\*12 为下一子 帧起始时间，s                                                                       |  Double |  8     |  H+4     |
|  4  |  L5 health      | L5 SPS 信号导航数据的健康状态： 0=健康；1=不健康                                                                       |  Ulong  |  4     |  H+12    |
| 5   | IODEC           | 星历和时钟数据龄期                                                                                                     | Ulong   | 4      | H+16     |
|  6  |  S health       | S SPS 信号导航数据的健康状态： 0=健康；1=不健康                                                                        |  Ulong  |  4     |  H+20    |
| 7   | Week            | GPS 周数（GPS Week）                                                                                                   | Ulong   | 4      | H+24     |
| 8   | Reserved        | 保留位                                                                                                                 | Ulong   | 4      | H+28     |
| 9   | Toe             | 星历的参考时间，单位：s                                                                                                | Double  | 8      | H+32     |
| 10  | A               | 卫星轨道长半轴，单位：m                                                                                                | Double  | 8      | H+40     |
|  11 |  ΔN             | 卫星平均角速度的改正值， 单位： rad/s                                                                                  |  Double |  8     |  H+48    |
| 12  | M0              | TOE 时间的平近点角，单位：rad                                                                                          | Double  | 8      | H+56     |
| 13  | Ecc             | 卫星轨道偏心率                                                                                                         | Double  | 8      | H+64     |

| ID      | 字段      | 数据描述                                                                                                                                                                                                        | 类型      | 字节数 | 字节偏移   |
|---------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|------------|
| 14      | ω         | 近地点幅角，单位：rad                                                                                                                                                                                           | Double    | 8      | H+72       |
| 15      | cuc       | 纬度幅角（余弦振幅，单位：rad）                                                                                                                                                                                 | Double    | 8      | H+80       |
| 16      | cus       | 纬度幅角（正弦振幅，单位：rad）                                                                                                                                                                                 | Double    | 8      | H+88       |
| 17      | crc       | 轨道半径（余弦振幅，单位：m）                                                                                                                                                                                   | Double    | 8      | H+96       |
| 18      | crs       | 轨道半径（正弦振幅，单位：m）                                                                                                                                                                                   | Double    | 8      | H+104      |
| 19      | cic       | 倾角（余弦振幅，单位：rad）                                                                                                                                                                                     | Double    | 8      | H+112      |
| 20      | cis       | 倾角（正弦振幅，单位：rad）                                                                                                                                                                                     | Double    | 8      | H+120      |
| 21      | I0        | TOE 时间轨道倾角，单位：rad                                                                                                                                                                                     | Double    | 8      | H+128      |
| 22      | IDOT      | 轨道倾角变化率，单位：rad/s                                                                                                                                                                                     | Double    | 8      | H+136      |
| 23      | Ω0        | 升交点赤经，单位：rad                                                                                                                                                                                           | Double    | 8      | H+144      |
| 24      | Ω dot     | 升交点赤经变化率，单位：rad/s                                                                                                                                                                                   | Double    | 8      | H+152      |
| 25      | Reserved  | 保留位                                                                                                                                                                                                          | Ulong     | 4      | H+160      |
| 26      | toc       | 卫星钟差参考时间，单位：s                                                                                                                                                                                       | Double    | 8      | H+164      |
| 27      | tgd       | IRNSS S 信号群延迟，单位：s                                                                                                                                                                                     | Double    | 8      | H+172      |
| 28      | af0       | 卫星钟差参数，单位：s                                                                                                                                                                                           | Double    | 8      | H+180      |
| 29      | af1       | 卫星钟速参数，单位：s/s                                                                                                                                                                                         | Double    | 8      | H+188      |
| 30      | af2       | 卫星钟漂参数，单位：s/s2                                                                                                                                                                                        | Double    | 8      | H+196      |
|      31 |      Flag | Bit0: Alert Flag，警示标志，当设置为 1 时，导航数据的使用风险由用户自行承担 Bit1: AutoNav 模式，当设置为 1 时，卫星处于 AutoNav 模式。卫星播发 AutoNav 数据集中的主要导航参数， 无地面上行链路数据，最多 7 天。 |      Enum |      4 |      H+204 |
| 32      | N         | 改正平均角速度，单位：rad/s                                                                                                                                                                                     | Double    | 8      | H+208      |

| ID    | 字段     | 数据描述                                                                                                                 | 类型      | 字节数 | 字节偏移 |
|-------|----------|--------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|    33 |    URA   | 用户距离精度，m2。ICD 中给出了一种算法将原始星历中传输的URAI 指数转化为名义标准差值。此处输出这一 名义值的平方（方差）。 |    Double |    8   |    H+216 |
| 34    | xxxx     | 32 位 CRC 校验                                                                                                           | Hex       | 4      | H+224    |
| 35    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                     | -         | -      | -        |

#### AGRIC 信息

AGRIC 信息中包含接收机的位置、速度、序列号、航向、基线等信息。

Message ID: 11276 ASCII 输出语法:

AGRICA 1

AGRICA COM2 1

BINARY 输出语法:

AGRICB 1

AGRICB COM2 1

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

消息输出：

\#AGRICA,97,GPS,FINE,2190,363942000,0,0,18,12;GNSS,232,21,12,30,5,5,24,1,0,5,1 5,1,0.0000,0.0000,0.0000,0.0000,0.0000,0.0000,0.0000,0.0000,0.0000,0.005,-0.003,0.00

1,0.004,0.042,0.050,0.044,40.07898274722,116.23663152683,60.0036,-2160488.6213,43

83615.6655,4084732.9679,1.8493,1.8902,4.4654,0.0000,0.0000,0.0000,0.00000000000,

0.00000000000,0.0000,-0.00000000000,0.00000000000,0.0000,363942000,0.000,15.213

205,-8.492279,0.000000,0.000000,5,0,0,0\*0b2e294a

表 7-82 AGRIC 数据结构

| 序号     | 字段           | 描述                                                                                                                           | 数据类型    | 字节数  | 字节偏移   |
|----------|----------------|--------------------------------------------------------------------------------------------------------------------------------|-------------|---------|------------|
|   1      |   AGRIC header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210) ， ASCII 消息头结构请参考[表7-51](#_bookmark211)                        |             |   H     |   0        |
| 2        | GNSS           |                                                                                                                                | Char        | 4       | H          |
|    3     |    length      | 指令长度， 从 GNSS 到 CRC 校验，整包数据长度 （ 232 字节） ， 固定值 0XE8                                                      |    uchar    |    1    |    H+4     |
|   4      |   Year         | UTC 时间-年，举例： 2016 年，为 16； 2116 年，为 116                                                                           |   uchar     |   1     |   H+5      |
| 5        | Month          | UTC 时间-月                                                                                                                    | uchar       | 1       | H+6        |
| 6        | Day            | UTC 时间-日                                                                                                                    | uchar       | 1       | H+7        |
| 7        | Hour           | UTC 时间-时                                                                                                                    | uchar       | 1       | H+8        |
| 8        | Minute         | UTC 时间-分                                                                                                                    | uchar       | 1       | H+9        |
| 9        | Second         | UTC 时间-秒                                                                                                                    | uchar       | 1       | H+10       |
|       10 |       Postype  | 流动站定位状态： 0：无效解； 1：单点定位解； 2：伪距差分； 4：固定解； 5：浮动解； 7：外部输入固定位置（仅特定版本支持此字段） |       uchar |       1 |       H+11 |

| 序号  | 字段              | 描述                                                        | 数据类型 | 字节数 | 字节偏移 |
|-------|-------------------|-------------------------------------------------------------|----------|--------|----------|
|    11 |    Heading Status | 主从天线 Heading 解状态 0：无效解； 4：固定解； 5：浮动解； |    uchar |    1   |    H+12  |
| 12    | Num GPS Sta       | 参与解算 GPS 卫星数                                         | uchar    | 1      | H+13     |
| 13    | Num BDS Sta       | 参与解算北斗卫星数                                          | uchar    | 1      | H+14     |
|  14   |  Num GLO Sta      | 参与解算 GLONASS 卫星 数                                    |  uchar   |  1     |  H+15    |
|  15   |  Baseline_N       | 基站到流动站基线向量， 北方向分量                           |  float   |  4     |  H+16    |
|  16   |  Baseline_E       | 基站到流动站基线向量， 东方向分量                           |  float   |  4     |  H+20    |
|  17   |  Baseline_U       | 基站到流动站基线向量， 天顶方向分量                         |  float   |  4     |  H+24    |
|  18   |  Baseline_NStd    | 基站到流动站基线向量， 北方向分量标准差                     |  float   |  4     |  H+28    |
|  19   |  Baseline_EStd    | 基站到流动站基线向量， 东方向分量标准差                     |  float   |  4     |  H+32    |
|  20   |  Baseline_UStd    | 基站到流动站基线向量， 天顶方向分量标准差                   |  float   |  4     |  H+36    |
| 21    | Heading           | 航向角                                                      | float    | 4      | H+40     |
| 22    | Pitch             | 俯仰角                                                      | float    | 4      | H+44     |
| 23    | Roll              | 横滚角                                                      | float    | 4      | H+48     |
| 24    | Speed             | 速度大小，标量                                              | float    | 4      | H+52     |
| 25    | Velocity of North | 北方向速度                                                  | float    | 4      | H+56     |
| 26    | Velocity of East  | 东方向速度                                                  | float    | 4      | H+60     |
| 27    | Velocity of Up    | 天顶方向速度                                                | float    | 4      | H+64     |

| 序号 | 字段             | 描述                                            | 数据类型 | 字节数 | 字节偏移 |
|------|------------------|-------------------------------------------------|----------|--------|----------|
| 28   | Xigema_Vx        | 北方向速度标准差                                | float    | 4      | H+68     |
| 29   | Xigema_Vy        | 东方向速度标准差                                | float    | 4      | H+72     |
| 30   | Xigema_Vz        | 天顶方向速度标准差                              | float    | 4      | H+76     |
|  31  |  lat             | 流动站纬度：-90\~90 度， 北半球正，南半球负     |  double  |  8     |  H+80    |
|   32 |   lon            | 流动站经度： -180\~180度，东经为正值，西经为 负 |   double |   8    |   H+88   |
| 33   | alt              | 流动站高程                                      | double   | 8      | H+96     |
| 34   | ECEF_X           | ECEF 坐标系下的 X                               | double   | 8      | H+104    |
| 35   | ECEF_Y           | ECEF 坐标系下的 Y                               | double   | 8      | H+112    |
| 36   | ECEF_Z           | ECEF 坐标系下的 Z                               | double   | 8      | H+120    |
| 37   | Xigema_lat       | 纬度标准差                                      | float    | 4      | H+128    |
| 38   | Xigema_lon       | 经度标准差                                      | float    | 4      | H+132    |
| 39   | Xigema_alt       | 高程标准差                                      | float    | 4      | H+136    |
| 40   | Xigema_ECEF_X    | ECEF_X 标准差                                   | float    | 4      | H+140    |
| 41   | Xigema_ECEF_Y    | ECEF_Y 标准差                                   | float    | 4      | H+144    |
| 42   | Xigema_ECEF_Z    | ECEF_Z 标准差                                   | float    | 4      | H+148    |
| 43   | BASE_lat         | 基准站纬度：-90\~90 度                          | double   | 8      | H+152    |
| 44   | BASE_lon         | 基准站经度：-180\~180 度                        | double   | 8      | H+160    |
| 45   | BASE_alt         | 基准站高程                                      | double   | 8      | H+168    |
| 46   | SEC_lat          | 从天线纬度：-90\~90 度                          | double   | 8      | H+176    |
| 47   | SEC_lon          | 从天线经度：-180\~180 度                        | double   | 8      | H+184    |
| 48   | SEC_alt          | 从天线高程                                      | double   | 8      | H+192    |
|  49  | GPS_WEEK_SECO ND |  GPS 周内毫秒                                   |  int     |  4     |  H+200   |
| 50   | Diffage          | 差分龄期                                        | float    | 4      | H+204    |
| 51   | Speed_Heading    | 速度的方向                                      | float    | 4      | H+208    |

| 序号 | 字段           | 描述                                | 数据类型 | 字节数 | 字节偏移 |
|------|----------------|-------------------------------------|----------|--------|----------|
| 52   | Undulation     | 高程异常值                          | float    | 4      | H+212    |
| 53   | Remain_float_3 | 保留                                | float    | 4      | H+216    |
| 54   | Remain_float_4 | 保留                                | float    | 4      | H+220    |
| 55   | Num GAL Sta    | Galileo 卫星数                      | uchar    | 1      | H+224    |
|  56  |  Speed_Type    | 0：速度解状态有效 1：速度解状态无效 |  uchar   |  1     |  H+225   |
| 57   | Remain_char_3  | 保留                                | uchar    | 1      | H+226    |
| 58   | Remain_char_4  | 保留                                | uchar    | 1      | H+227    |
| 59   | xxxx           | 32 位 CRC 校验                      | HEX      | 4      | H+228    |
| 60   | [CR][LF]       | 语句结束符(仅 ASCII)                | -        | -      | -        |

#### PVTSLN 定位定向信息

本指令将接收机计算出的最佳位置、最佳速度以及定向信息整合为一个完整的消息包，解决终端解析多条 message 的繁琐问题。

Message ID: 1021

ASCII 输出语法:

PVTSLNA 1

BINARY 输出语法:

PVTSLNB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#PVTSLNA,97,GPS,FINE,2190,364536000,0,0,18,13;SINGLE,60.5060,40.0789813052 2,116.23663134427,4.3353,1.8063,1.8796,0.000,SINGLE,60.5060,40.07898130522,116.2

3663134427,-8.4923,46,28,46,28,0.0009,-0.0031,-0.0032,NONE,0.0000,0.0000,0.0000,0,

0,0,0,2.1753,1.3480,0.6840,1.8392,1.7072,5.0,28,25,26,29,31,32,34,39,77,79,83,98,99,16

1,162,163,166,167,169,176,179,182,196,199,200,205,206,219,220\*1e33c8cb

表 7-83 PVTSLN 数据结构

| ID   | 字段            | 数据描述                                                                                                | 类型    | 字节数 | 字节偏移 |
|------|-----------------|---------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |   PVTSLN header | 消息头， 二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消 息头结构请参考[表7-51](#_bookmark211) |   H     |   H    |   0      |
| 2    | bestpos_type    | 位置类型，参考[表0- 4 位置](#_bookmark434) [或速度类型](#_bookmark434)                                  | Enum    | 4      | H        |
| 3    | bestpos_hgt     | 海拔高，单位：米                                                                                        | FLOAT   | 4      | H+4      |
|  4   |  bestpos_lat    | 纬度， 单位： 度（ 输出小 数点后 11 位）                                                                |  DOUBLE |  8     |  H+8     |
|  5   |  bestpos_lon    | 经度， 单位： 度（ 输出小 数点后 11 位）                                                                |  DOUBLE |  8     |  H+16    |
| 6    | bestpos_hgtstd  | 高程标准差                                                                                              | FLOAT   | 4      | H+24     |
| 7    | bestpos_latstd  | 纬度标准差                                                                                              | FLOAT   | 4      | H+28     |
| 8    | bestpos_lonstd  | 经度标准差                                                                                              | FLOAT   | 4      | H+32     |
| 9    | bestpos_diffage | 定位时 BESTNAV 差分龄期                                                                                 | FLOAT   | 4      | H+36     |
|  10  |  psrpos_type    | 位置类型，参考[表0- 4 位置](#_bookmark434) [或速度类型](#_bookmark434)                                  |  Enum   |  4     |  H+40    |
| 11   | psrpos_hgt      | 平均海平面高度                                                                                          | FLOAT   | 4      | H+44     |
| 12   | psrpos_lat      | 纬度                                                                                                    | DOUBLE  | 8      | H+48     |
| 13   | psrpos_lon      | 经度                                                                                                    | DOUBLE  | 8      | H+56     |
|   14 |   undulation    | 大地水准面差距- 大地水准 面和 WGS84 椭球面之间的距离（米）                                              |   FLOAT |   4    |   H+64   |
| 15   | bestpos_svs     | 跟踪卫星数                                                                                              | UCHAR   | 1      | H+68     |
| 16   | bestpos_solnsvs | 参与解算卫星数                                                                                          | UCHAR   | 1      | H+69     |

| ID  | 字段               | 数据描述                                                         | 类型    | 字节数 | 字节偏移 |
|-----|--------------------|------------------------------------------------------------------|---------|--------|----------|
| 17  | psrpos_svs         | 跟踪卫星数                                                       | UCHAR   | 1      | H+70     |
| 18  | psrpos_solnsvs     | 参与解算卫星数                                                   | UCHAR   | 1      | H+71     |
| 19  | psrvel_north       | 北向速度，m/s                                                    | DOUBLE  | 8      | H+72     |
| 20  | psrvel_east        | 东向速度，m/s                                                    | DOUBLE  | 8      | H+80     |
| 21  | psrvel_ground      | 对地水平速度，m/s                                                | DOUBLE  | 8      | H+88     |
|  22 |  heading_type      | 定向类型，参考[表0- 5 解的](#_bookmark435) [状态](#_bookmark435) |  Enum   |  4     |  H+96    |
| 23  | heading_length     | 基线长(0 到 3000 m)                                              | FLOAT   | 4      | H+100    |
| 24  | heading_degree     | 航向(0 到 360.0 deg)                                             | FLOAT   | 4      | H+104    |
| 25  | heading_pitch      | 俯仰(±90 deg)                                                    | FLOAT   | 4      | H+108    |
| 26  | heading_trackedsvs | 主天线跟踪卫星数                                                 | UCHAR   | 1      | H+112    |
| 27  | heading_solnsvs    | 参与定向解算卫星数                                               | UCHAR   | 1      | H+113    |
|  28 |  heading_ggl1      | 参与定向解算的 L1 频点的 卫星数                                  |  UCHAR  |  1     |  H+114   |
|  29 |  heading_ggl1l2    | 参与定向解算的 L1 L2 频点 的卫星数                               |  UCHAR  |  1     |  H+115   |
| 30  | gdop               | 几何精度因子                                                     | FLOAT   | 4      | H+116    |
| 31  | pdop               | 位置精度因子                                                     | FLOAT   | 4      | H+120    |
| 32  | hdop               | 水平精度因子                                                     | FLOAT   | 4      | H+124    |
| 33  | htdop              | 水平和时间精度因子                                               | FLOAT   | 4      | H+128    |
| 34  | tdop               | 时间精度因子                                                     | FLOAT   | 4      | H+132    |
| 35  | cutoff             | 截止高度角                                                       | FLOAT   | 4      | H+136    |
| 36  | PRN No             | 要跟踪卫星的 PRN 数                                              | USHORT  | 2      | H+140    |
|  37 |  PRN_list[41]      | 跟踪卫星的 PRN，位置解 算不可用时为空                            |  USHORT |  41\*2 |  H+142   |
|  38 |  xxxx              | 32 位 CRC 校验(仅 ASCII 和 二进制)                               |  Hex    |  4     |  H+224   |

| ID | 字段     | 数据描述             | 类型 | 字节数 | 字节偏移 |
|----|----------|----------------------|------|--------|----------|
| 39 | [CR][LF] | 语句结束符(仅 ASCII) | -    | -      | -        |

#### UNILOGLIST 请求log 列表输出

该 Log 列出当前系统运行的log 信息。该指令不支持二进制信息格式。

ASCII 输出语法:

UNILOGLIST

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

消息输出：

\#UNILOGLIST,66,GPS,FINE,2203,447089000,0,0,18,33;

\< 3

\< PSRPOSA COM1 1

\< GPGGA COM1 1

\< HWSTATUSA COM1 1

表 7-84 UNILOGLIST 数据结构

| ID   | 字段                     | 数据描述                                                                               | 类型      |
|------|--------------------------|----------------------------------------------------------------------------------------|-----------|
|  1   | UNILOGLIST (ASCII)header | 消息头，详见[表 7-51 ASCII 数据格式 Header（头）](#_bookmark211) [结构](#_bookmark211) |           |
| 2    | \#port                   | 跟随的信息数，最大值= 30                                                               | Long      |
| 3    | LOG                      | “LOG”字符串                                                                            |           |
| 4    | port                     | 输出端口，参考[表7-85 端口标识符](#_bookmark270)                                       | Enum      |
|  5   |  message                 | Log 的信息名称，简化 ASCII 无后缀，ASCII 有后缀 A，二进制有后缀 B。                    |  Char [ ] |
| 6    | trigger                  | 信息输出的触发器模式，可以是 ONTIME 或 ONCE。                                          |           |
| 7    | period                   | Log 周期（对于 ONTIME 触发器）秒数。                                                   |           |
| 8... | Next port                |                                                                                        |           |

| ID    | 字段      | 数据描述       | 类型 |
|-------|-----------|----------------|------|
| 可 变 |  xxxx     |  32 字节的 CRC |  Hex |
| 可 变 |  [CR][LF] |  语句结束符    |  -   |

表 7-85 端口标识符

| 接口名称 | 描述       |
|----------|------------|
| COM1     | COM 端口 1 |
| COM2     | COM 端口 2 |
| COM3     | COM 端口 3 |

#### BESTNAV 最佳位置和速度

本指令包含接收机主天线计算出的最佳可用的 GPS 和惯性导航系统（INS，若可用）位置（米）、速度。此外，接收机还报告了几个状态指示符，其中包括差分龄期。差分龄期对预测由差分改正中断造成的异常非常有用。若龄期为 0，则表示未使用差分改正。

Message ID: 2118

ASCII 输出语法:

BESTNAVA 1

BINARY 输出语法:

BESTNAVB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#BESTNAVA,97,GPS,FINE,2294,472312000,0,0,18,16;SOL_COMPUTED,SINGLE,40.0 7895888272,116.23651029820,65.8312,-8.4925,WGS84,1.2221,1.1053,2.1970,"0",0.000,

0.000,50,28,28,0,1,12,12,41,SOL_COMPUTED,DOPPLER_VELOCITY,0.000,0.000,0.0046,

335.592288,0.0045,0.0194,0.0123\*c1b4f7fe

表 7-86 BESTNAV 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  BESTNAV header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |         |   H    |   0      |
|  2  | p-sol status    |  解状态，参考[表0- 5 解的状态](#_bookmark435)                                                         |  Enum   |  4     |  H       |
|  3  |  pos type       | 位置类型（参考[表 0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                             |  Enum   |  4     |  H+4     |
| 4   | lat             | 纬度，deg                                                                                             | Double  | 8      | H+8      |
| 5   | lon             | 经度，deg                                                                                             | Double  | 8      | H+16     |
| 6   | hgt             | 海拔高，m                                                                                             | Double  | 8      | H+24     |
|  7  |  undulation     | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离（米）                                             |  Float  |  4     |  H+32    |
|  8  |  datum id\#     | 坐标系 ID 号，当前仅支持 WGS84 （二进制为 61）                                                        |  Enum   |  4     |  H+36    |
| 9   | lat σ           | 纬度标准差，m                                                                                         | Float   | 4      | H+40     |
| 10  | lon σ           | 经度标准差，m                                                                                         | Float   | 4      | H+44     |
| 11  | hgt σ           | 高度标准差，m                                                                                         | Float   | 4      | H+48     |
| 12  | stn id          | 基站 ID，缺省值为 0                                                                                   | Char[4] | 4      | H+52     |
| 13  | diff_age        | 差分龄期，s                                                                                           | Float   | 4      | H+56     |
| 14  | sol_age         | 解的龄期，s                                                                                           | Float   | 4      | H+60     |
| 15  | \#SVs           | 跟踪的卫星数                                                                                          | Uchar   | 1      | H+64     |
| 16  | \#solnSVs       | 在解中使用的卫星数                                                                                    | Uchar   | 1      | H+65     |
| 17  | Reserved        | 保留                                                                                                  | Uchar   | 1      | H+66     |
| 18  | Reserved        | 保留                                                                                                  | Uchar   | 1      | H+67     |
| 19  | Reserved        | 保留                                                                                                  | Uchar   | 1      | H+68     |

| ID    | 字段                           | 数据描述                                                                                                                              | 类型     | 字节数 | 字节偏移 |
|-------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|  20   |  ext sol stat                  | 扩展解的状态，参考[表7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                                |  Hex     |  1     |  H+69    |
|   21  | Galileo&B DS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                             |   Hex    |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码（参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273)[掩码](#_bookmark273)） |    Hex   |    1   |    H+71  |
|  23   | V-sol status                   |  解状态，参考[表0- 5 解的状态](#_bookmark435)                                                                                         |  Enum    |  4     |  H+72    |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                              | Enum     | 4      | H+76     |
|   25  |   latency                      | 根据速度时标计算的延迟值，以秒为单位。用历元时间减去延迟可得 到更准确的速度结果。                                                     |   Float  |   4    |   H+80   |
| 26    | age                            | 差分龄期，s                                                                                                                           | Float    | 4      | H+84     |
| 27    | hor spd                        | 对地水平速度，m/s                                                                                                                     | Double   | 8      | H+88     |
|  28   |  trk gnd                       | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                                                                                    |  Double  |  8     |  H+96    |
|   29  |   vert spd                     | 垂直速度，m/s，正值表示高度增加（向上），负值表示高度下降 （向下）                                                                    |   Double |   8    |   H+104  |
| 30    | Verspd std                     | 高程速度标准差，单位 m/s                                                                                                              | Float    | 4      | H+112    |
| 31    | Horspd std                     | 水平速度标准差，单位 m/s                                                                                                              | Float    | 4      | H+116    |
| 32    | xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                     | Hex      | 4      | H+120    |
| 33    | [CR][LF]                       | 语句结束符(仅 ASCII)                                                                                                                  | -        | -      | -        |

表 7-87 GPS/GLONASS/BDS2 使用的信号掩码

| Bit | 掩码 | 描述                 |
|-----|------|----------------------|
| 0   | 0x01 | 使用 GPS L1 计算     |
| 1   | 0x02 | 使用 GPS L2 计算     |
| 2   | 0x04 | 使用 GPS L5 计算     |
| 3   | 0x08 | 使用 BDS B3I 计算    |
| 4   | 0x10 | 使用 GLONASS L1 计算 |
| 5   | 0x20 | 使用 GLONASS L2 计算 |
| 6   | 0x40 | 使用 BDS B1I 计算    |
| 7   | 0x80 | 使用 BDS2 B2I 计算   |

表 7-88 Galileo&BDS3 使用的信号掩码

| Bit | 掩码 | 描述                  |
|-----|------|-----------------------|
| 0   | 0x01 | 使用 GALILEO E1 计算  |
| 1   | 0x02 | 使用 GALILEO E5B 计算 |
| 2   | 0x04 | 使用 GALILEO E5A 计算 |
| 3   | 0x08 | Reserved              |
| 4   | 0x10 | 使用 BDS3 B1I 计算    |
| 5   | 0x20 | 使用 BDS3 B3I 计算    |
| 6   | 0x40 | 使用 BDS3 B2a 计算    |
| 7   | 0x80 | 使用 BDS3 B1C 计算    |

表 7-89 扩展解状态

| Bit | 描述                               |
|-----|------------------------------------|
|   0 | RTK 解算校验 0 = 未校验 1 = 已校验 |

| Bit     | 描述                                                                                                     |
|---------|----------------------------------------------------------------------------------------------------------|
|     1-3 | 伪距电离层改正 0 = 未知 1 = Klobuchar 广播星历改正 2 = SBAS 电离层格网改正 3 = 多频改正 4 = 伪距差分改正 |

#### BESTNAVXYZ 最佳位置和速度（直角坐标系）

本指令包含接收机计算出的地心空间直角坐标系下最佳可用位置和速度信息。位置和速度的“status”字段表明了对应数据是否有效。

Message ID: 240

ASCII 输出语法:

BESTNAVXYZA 1

BINARY 输出语法:

BESTNAVXYZB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#BESTNAVXYZA,97,GPS,FINE,2190,364674000,0,0,18,9;SOL_COMPUTED,SINGLE,-2 160488.6043,4383615.8972,4084733.1053,0.0000,0.0000,0.0000,SOL_COMPUTED,DOP PLER_VELOCITY,-0.0023,0.0003,0.0020,0.0377,0.0503,0.0411,"",0.000,0.000,0.000,47,2 8,28,0,0,12,0,09\*299636fe

表 7-90 BESTNAVXYZ 数据结构

| ID   | 字段               | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|------|--------------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |  BESTNAVXYZ header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |         |   H    |   0      |
| 2    | P-sol status       | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H        |
| 3    | pos type           | 位置类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                              | Enum    | 4      | H+4      |
| 4    | P-X                | X 轴坐标，m                                                                                           | Double  | 8      | H+8      |
| 5    | P-Y                | Y 轴坐标，m                                                                                           | Double  | 8      | H+16     |
| 6    | P-Z                | Z 轴坐标，m                                                                                           | Double  | 8      | H+24     |
| 7    | P-X σ              | X 轴坐标标准差，m                                                                                     | Float   | 4      | H+32     |
| 8    | P-Y σ              | Y 轴坐标标准差，m                                                                                     | Float   | 4      | H+36     |
| 9    | P-Z σ              | Z 轴坐标标准差，m                                                                                     | Float   | 4      | H+40     |
| 10   | V-sol status       | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H+44     |
| 11   | vel type           | 速度类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                              | Enum    | 4      | H+48     |
| 12   | V-X                | X 轴速度，m/s                                                                                         | Double  | 8      | H+52     |
| 13   | V-Y                | Y 轴速度，m/s                                                                                         | Double  | 8      | H+60     |
| 14   | V-Z                | Z 轴速度，m/s                                                                                         | Double  | 8      | H+68     |
| 15   | V-X σ              | X 轴速度标准差，m/s                                                                                   | Float   | 4      | H+76     |
| 16   | V-Y σ              | Y 轴速度标准差，m/s                                                                                   | Float   | 4      | H+80     |
| 17   | V-Z σ              | Z 轴速度标准差，m/s                                                                                   | Float   | 4      | H+84     |
| 18   | stn ID             | 基站 ID，缺省值为 0                                                                                   | Char[4] | 4      | H+88     |
|   19 |   V-latency        | 根据速度时标计算的延迟值，以 秒为单位。用历元时间减去延迟可得到更准确的速度结果。                     |   Float |   4    |   H+92   |
| 20   | diff_age           | 差分龄期，s                                                                                           | Float   | 4      | H+96     |
| 21   | sol_age            | 解的龄期，s                                                                                           | Float   | 4      | H+100    |

| ID    | 字段                            | 数据描述                                                                                                                               | 类型   | 字节数 | 字节偏移 |
|-------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
| 22    | \#SVs                           | 跟踪的卫星数                                                                                                                           | Uchar  | 1      | H+104    |
| 23    | \#solnSVs                       | 在解中使用的卫星数                                                                                                                     | Uchar  | 1      | H+105    |
| 24    | \#ggL1                          | L1/G1/B1 信号参与解算的卫星数                                                                                                          | Uchar  | 1      | H+106    |
|  25   |  \#solnMultiSVs                 | L1/G1/B1/E1 信号参与解算的卫 星数                                                                                                      |  Uchar |  1     |  H+107   |
| 26    | Reserved                        | 保留                                                                                                                                   | Char   | 1      | H+108    |
|  27   |  ext sol stat                   | 扩展解的状态，参考[表7-89 扩展](#_bookmark275) [解状态](#_bookmark275)                                                                 |  Hex   |  1     |  H+109   |
|   28  |  Galileo&BDS3 sig mask          | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3](#_bookmark274) [使用的信号掩码](#_bookmark274)                               |   Hex  |   1    |   H+110  |
|    29 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的 信号掩码（参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信](#_bookmark273) [号掩码](#_bookmark273)） |    Hex |    1   |    H+111 |
|  30   |  xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进 制)                                                                                                     |  Hex   |  4     |  H+112   |
| 31    | [CR][LF]                        | 语句结束符(仅 ASCII)                                                                                                                   | -      | -      | -        |

#### BESTNAVH 从天线最佳的位置和速度

本指令包含接收机从天线计算出的最佳可用的 GPS 和惯性导航系统（INS，若可用）位置（米）、速度。此外，接收机还报告了几个状态指示符，其中包括差分龄期。差分龄期对预测由差分改正中断造成的异常非常有用。若龄期为 0，则表示未使用差分改正。

Message ID: 2119

ASCII 输出语法:

BESTNAVHA 1

BINARY 输出语法:

BESTNAVHB 1

适用产品：UM982、UMD982消息输出：

\#BESTNAVHA,97,GPS,FINE,2190,364700000,0,0,18,13;INSUFFICIENT_OBS,NONE,4 0.07898868399,116.23660520125,59.8754,-

8.4923,WGS84,2.9766,2.8787,10.0570,"0",0.000,11374.000,0,0,0,0,33,02,00,00,INSUFFI CIENT_OBS,NONE,0.000,0.000,0.0301,33.043127,-0.0892,0004000c\*7b4767e9

表 7-91 BESTNAVH 数据结构

| ID  | 字段             | 数据描述                                                                                                                | 类型   | 字节数 | 字节偏移 |
|-----|------------------|-------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  BESTNAVH header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |        |   H    |   0      |
| 2   | p-sol status     | 解状态，参考[表0- 5 解的状态](#_bookmark435)                                                                            | Enum   | 4      | H        |
|  3  |  pos type        | 位置类型（参考[表0- 4 位置或速度类](#_bookmark434) [型](#_bookmark434)）                                                |  Enum  |  4     |  H+4     |
| 4   | lat              | 纬度，deg                                                                                                               | Double | 8      | H+8      |
| 5   | lon              | 经度，deg                                                                                                               | Double | 8      | H+16     |
| 6   | hgt              | 海拔高，m                                                                                                               | Double | 8      | H+24     |
|  7  |  undulation      | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离（米）                                                               |  Float |  4     |  H+32    |
|  8  |  datum id\#      | 坐标系 ID 号，当前仅支持 WGS84 （二进制为 61）                                                                          |  Enum  |  4     |  H+36    |
| 9   | lat σ            | 纬度标准差，m                                                                                                           | Float  | 4      | H+40     |
| 10  | lon σ            | 经度标准差，m                                                                                                           | Float  | 4      | H+44     |

| ID    | 字段                            | 数据描述                                                                                                                               | 类型    | 字节数 | 字节偏移 |
|-------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
| 11    | hgt σ                           | 高度标准差，m                                                                                                                          | Float   | 4      | H+48     |
| 12    | stn id                          | 基站 ID，缺省值为 0                                                                                                                    | Char[4] | 4      | H+52     |
| 13    | diff_age                        | 差分龄期，s                                                                                                                            | Float   | 4      | H+56     |
| 14    | sol_age                         | 解的龄期，s                                                                                                                            | Float   | 4      | H+60     |
| 15    | \#SVs                           | 跟踪的卫星数                                                                                                                           | Uchar   | 1      | H+64     |
| 16    | \#solnSVs                       | 在解中使用的卫星数                                                                                                                     | Uchar   | 1      | H+65     |
| 17    | Reserved                        | 保留                                                                                                                                   | Uchar   | 1      | H+66     |
| 18    | Reserved                        | 保留                                                                                                                                   | Uchar   | 1      | H+67     |
| 19    | Reserved                        | 保留                                                                                                                                   | Uchar   | 1      | H+68     |
|  20   |  ext sol stat                   | 扩展解的状态，参考[表7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                                 |  Hex    |  1     |  H+69    |
|   21  |  Galileo&BDS3 sig mask          | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                              |   Hex   |   1    |   H+70   |
|    22 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS 2 使用的信 号掩码（参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号掩](#_bookmark273)[码](#_bookmark273)） |    Hex  |    1   |    H+71  |
| 23    | V-sol status                    | 解状态，参考[表0- 5 解的状态](#_bookmark435)                                                                                           | Enum    | 4      | H+72     |
| 24    | vel type                        | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                               | Enum    | 4      | H+76     |
|   25  |   latency                       | 根据速度时标计算的延迟值，以秒为单位。用历元时间减去延迟可得 到更准确的速度结果。                                                      |   Float |   4    |   H+80   |
| 26    | age                             | 差分龄期，s                                                                                                                            | Float   | 4      | H+84     |
| 27    | hor spd                         | 对地水平速度，m/s                                                                                                                      | Double  | 8      | H+88     |

| ID   | 字段       | 数据描述                                                           | 类型     | 字节数 | 字节偏移 |
|------|------------|--------------------------------------------------------------------|----------|--------|----------|
|  28  |  trk gnd   | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                 |  Double  |  8     |  H+96    |
|   29 |   vert spd | 垂直速度，m/s，正值表示高度增加 （向上），负值表示高度下降（向下） |   Double |   8    |   H+104  |
| 30   | Verspd std | 高程速度标准差，单位 m/s                                           | Float    | 4      | H+112    |
| 31   | Horspd std | 水平速度标准差，单位 m/s                                           | Float    | 4      | H+116    |
| 32   | xxxx       | 32 位 CRC 校验(仅 ASCII 和二进制)                                  | Hex      | 4      | H+120    |
| 33   | [CR][LF]   | 语句结束符(仅 ASCII)                                               | -        | -      | -        |

#### BESTNAVXYZH 从天线最佳位置和速度（直角坐标系）

本指令包含接收机从天线计算出的地心空间直角坐标系下最佳可用位置和速度信息。位置和速度的“status”字段表明了对应数据是否有效。

Message ID: 242

ASCII 输出语法:

BESTNAVXYZHA 1

BINARY 输出语法:

BESTNAVXYZHB 1

适用产品：UM982、UMD982消息输出：

\#BESTNAVXYZHA,97,GPS,FINE,2190,364732000,0,0,18,13;INSUFFICIENT_OBS,NO NE,-2160485.5484,4383615.5669,4084733.8716,0.0000,0.0000,0.0000,INSUFFICIENT_O BS,NONE,0.0227,-0.0831,-0.0382,0.5312,0.8483,0.5947,"",0.000,0.000,11406.000,0,0,0, 0,0,02,0,00\*58985f99

表 7-92 BESTNAVXYZH 数据结构

| ID   | 字段                | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|------|---------------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |  BESTNAVXYZH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |         |   H    |   0      |
| 2    | P-sol status        | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H        |
| 3    | pos type            | 位置类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                              | Enum    | 4      | H+4      |
| 4    | P-X                 | X 轴坐标，m                                                                                           | Double  | 8      | H+8      |
| 5    | P-Y                 | Y 轴坐标，m                                                                                           | Double  | 8      | H+16     |
| 6    | P-Z                 | Z 轴坐标，m                                                                                           | Double  | 8      | H+24     |
| 7    | P-X σ               | X 轴坐标标准差，m                                                                                     | Float   | 4      | H+32     |
| 8    | P-Y σ               | Y 轴坐标标准差，m                                                                                     | Float   | 4      | H+36     |
| 9    | P-Z σ               | Z 轴坐标标准差，m                                                                                     | Float   | 4      | H+40     |
| 10   | V-sol status        | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H+44     |
| 11   | vel type            | 速度类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                              | Enum    | 4      | H+48     |
| 12   | V-X                 | X 轴速度，m/s                                                                                         | Double  | 8      | H+52     |
| 13   | V-Y                 | Y 轴速度，m/s                                                                                         | Double  | 8      | H+60     |
| 14   | V-Z                 | Z 轴速度，m/s                                                                                         | Double  | 8      | H+68     |
| 15   | V-X σ               | X 轴速度标准差，m/s                                                                                   | Float   | 4      | H+76     |
| 16   | V-Y σ               | Y 轴速度标准差，m/s                                                                                   | Float   | 4      | H+80     |
| 17   | V-Z σ               | Z 轴速度标准差，m/s                                                                                   | Float   | 4      | H+84     |
| 18   | stn ID              | 基站 ID，缺省值为 0                                                                                   | Char[4] | 4      | H+88     |
|   19 |   V-latency         | 根据速度时标计算的延迟值，以秒为单位。用历元时间减去延迟可得 到更准确的速度结果。                     |   Float |   4    |   H+92   |
| 20   | diff_age            | 差分龄期，s                                                                                           | Float   | 4      | H+96     |
| 21   | sol_age             | 解的龄期，s                                                                                           | Float   | 4      | H+100    |

| ID    | 字段                            | 数据描述                                                                                                                              | 类型   | 字节数 | 字节偏移 |
|-------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
| 22    | \#SVs                           | 跟踪的卫星数                                                                                                                          | Uchar  | 1      | H+104    |
| 23    | \#solnSVs                       | 在解中使用的卫星数                                                                                                                    | Uchar  | 1      | H+105    |
| 24    | \#ggL1                          | L1/G1/B1 信号参与解算的卫星数                                                                                                         | Uchar  | 1      | H+106    |
|  25   |  \#solnMultiSVs                 | L1/G1/B1/E1 信号参与解算的卫 星数                                                                                                     |  Uchar |  1     |  H+107   |
| 26    | Reserved                        | 保留                                                                                                                                  | Char   | 1      | H+108    |
|  27   |  ext sol stat                   | 扩展解的状态，参考[表7-89 扩展](#_bookmark275) [解状态](#_bookmark275)                                                                |  Hex   |  1     |  H+109   |
|   28  |  Galileo&BDS3 sig mask          | Galileo 和 BDS3 使用的信号掩 码。参考[表7-88 Galileo&BDS3 使](#_bookmark274)[用的信号掩码](#_bookmark274)                             |   Hex  |   1    |   H+110  |
|    29 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码（参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信](#_bookmark273)[号掩码](#_bookmark273)） |    Hex |    1   |    H+111 |
|  30   |  xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进 制)                                                                                                    |  Hex   |  4     |  H+112   |
| 31    | [CR][LF]                        | 语句结束符(仅 ASCII)                                                                                                                  | -      | -      | -        |

#### BESTSAT 参与定位的卫星信息

本指令包含参与定位的卫星信息。

Message ID: 1041 ASCII 输出语法:

BESTSATA 1

BINARY 输出语法:

BESTSATB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出:

\#BESTSATA,79,GPS,FINE,2203,226245800,0,0,18,22;43,GPS,2,GOOD,00000013,GP S,5,GOOD,00000013,GPS,7,GOOD,00000003,GPS,13,GOOD,00000013,GPS,15,GOOD,00 000013,GPS,18,GOOD,00000007,GPS,20,GOOD,00000013,GPS,29,GOOD,00000013,GPS,

30,GOOD,00000007,QZSS,195,GOOD,00000017,QZSS,196,GOOD,00000017,QZSS,199,G OOD,00000017,GLONASS,42+8,GOOD,00000003,GLONASS,43+3,GOOD,00000001,GLO NASS,44+12,GOOD,00000003,GLONASS,57+9,GOOD,00000003,GLONASS,58+11,GOOD, 00000003,GALILEO,4,GOOD,00000017,GALILEO,11,GOOD,00000017,GALILEO,12,GOOD,

00000017,GALILEO,19,GOOD,00000017,GALILEO,33,GOOD,00000017,BEIDOU,1,GOOD,

00000017,BEIDOU,2,GOOD,00000017,BEIDOU,3,GOOD,00000017,BEIDOU,4,GOOD,000

00017,BEIDOU,6,GOOD,00000017,BEIDOU,7,GOOD,00000007,BEIDOU,8,GOOD,000000

17,BEIDOU,10,GOOD,00000007,BEIDOU,13,GOOD,00000017,BEIDOU,16,GOOD,000000

17,BEIDOU,19,GOOD,00000005,BEIDOU,20,GOOD,00000015,BEIDOU,27,GOOD,000000

05,BEIDOU,29,GOOD,00000015,BEIDOU,30,GOOD,00000015,BEIDOU,32,GOOD,000000

15,BEIDOU,35,GOOD,00000005,BEIDOU,38,GOOD,00000015,BEIDOU,39,GOOD,000000

15,BEIDOU,59,GOOD,00000015,BEIDOU,60,GOOD,00000015\*34479d6a

表 7-93 BESTSAT 数据结构

| ID  | 字段             | 数据描述                                                                                                               | 类型  | 字节数 | 字节偏移 |
|-----|------------------|------------------------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  BESTSAT Header  | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |       |   H    |   0      |
| 2   | \#entries        | 跟踪的记录数量                                                                                                         | Ulong | 4      | H+0      |
|  3  | Satellite system | GNSS 卫星系统列表，参考[表7-116](#_bookmark322) [卫星系统](#_bookmark322)                                              |  Enum |  4     |  H+4     |

| ID            | 字段                                             | 数据描述                                                                                                                                                                                                                                                                                                                                                                                                                                               | 类型              | 字节数        | 字节偏移              |
|---------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|---------------|-----------------------|
|             4 |             Satellite ID                         | 卫星 PRN 号（详见[表7-54 Unicore](#_bookmark216)[消息中的卫星 PRN](#_bookmark216)） 在二进制消息中，卫星 ID 字段由两个 Ushort 组成。最低的两个字节是系统标识符（如 GPS 的 PRN， GLONASS 的通道号），为 USHORT 类型；最高的两个字节是 GLONASS 的频率通道，其它系统这两个字节值为零。在 ASCII 消息中，卫星 ID 字段是系统标识符。如果系统是 GLONASS，而频率通道不是 零，则在系统标识符后加上频率通道数。例如，系统标识符是 13，频 率通道-2，输出为 13-2。 |             Ulong |             4 |             H+8       |
|  5            |  Status                                          | 在二进制消息中，数值是“0”；在 ASCII 消息中为：“GOOD”                                                                                                                                                                                                                                                                                                                                                                                                   |  Enum             |  4            |  H+12                 |
|     6         |     Signal mask                                  | [表7-94 BESTSAT GPS Signal Mask](#_bookmark284)[表7-95 BESTSAT GLONASS Signal](#_bookmark285) [Mask](#_bookmark285) [表7-96 BESTSAT BDS Signal Mask](#_bookmark286) [表7-97 BESTSAT Galileo Signal](#_bookmark287) [Mask](#_bookmark287)                                                                                                                                                                                                               |     Hex           |     4         |     H+16              |
| 7             | Next satellite offset = H + 4 + (\#entries x 16) |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                   |               |                       |
|   8           |   xxxx                                           |   32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                                                                                                                                                                                                                                                                                                                                    |   Hex             |   4           | H+4+ (\#entries x 16) |
| 9             | [CR][LF]                                         | 语句结束符(仅 ASCII)                                                                                                                                                                                                                                                                                                                                                                                                                                   | -                 | -             | -                     |

表 7-94 BESTSAT GPS Signal Mask

| Bit | MASK          | 描述                                                          |
|-----|---------------|---------------------------------------------------------------|
| 0   | 0x01          | GPS L1 used in Solution                                       |
| 1   | 0x02          | GPS L2 used in Solution                                       |
| 2   | 0x00 or 0x01  | GPS L5 used in Solution                                       |
| 3   | Reserved      | Reserved                                                      |
|  4  |  0x00 or 0x01 | 如果此卫星是和基站的共视卫星，此 bit 置为 0x01,否 则置为 0x00 |

表 7-95 BESTSAT GLONASS Signal Mask

| Bit | MASK          | 描述                                                                                 |
|-----|---------------|--------------------------------------------------------------------------------------|
| 0   | 0x01          | GLONASS L1 used in Solution                                                          |
| 1   | 0x02          | GLONASS L2 used in Solution                                                          |
| 2   | 0x04          | GLONASS L3 used in Solution                                                          |
| 3   | Reserved      | Reserved                                                                             |
|  4  |  0x00 or 0x01 | 如果此卫星是和基站的共视卫星，并且参与模糊度解算， 则此 bit 置为 0x01，否则置为 0x00 |

表 7-96 BESTSAT BDS Signal Mask

| Bit | MASK          | 描述                                                           |
|-----|---------------|----------------------------------------------------------------|
| 0   | 0x01          | BeiDou B1 used in Solution                                     |
| 1   | 0x02          | BeiDou B2 used in Solution                                     |
| 2   | 0x04          | BeiDou B3 used in Solution                                     |
| 3   | Reserved      | Reserved                                                       |
|  4  |  0x00 or 0x01 | 如果此卫星是和基站的共视卫星，此 bit 置为 0x01，否则 置为 0x00 |

表 7-97 BESTSAT Galileo Signal Mask

| Bit | MASK          | 描述                                                           |
|-----|---------------|----------------------------------------------------------------|
| 0   | 0x01          | Galileo E1 used in Solution                                    |
| 1   | 0x02          | Galileo E5A used in Solution                                   |
| 2   | 0x04          | Galileo E5B used in Solution                                   |
| 3   | 0x08          | Galileo ALTBOC used in Solution                                |
|  4  |  0x00 or 0x01 | 如果此卫星是和基站的共视卫星，此 bit 置为 0x01，否则 置为 0x00 |

#### ADRNAV RTK 位置和速度信息

本指令包含接收机载波相位 RTK 定位的位置及定位精度、状态、速度等信息。

Message ID: 142 ASCII 输出语法:

ADRNAVA 1

BINARY 输出语法:

ADRNAVB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#ADRNAVA,97,GPS,FINE,2190,364787000,0,0,18,1;INSUFFICIENT_OBS,NONE,0.000 00000000,0.00000000000,-17.0000,17.0000,WGS84,0.0000,0.0000,0.0000,"0",0.000,0.0

00,46,0,0,0,0,00,00,00,INSUFFICIENT_OBS,NONE,0.000,0.000,0.0000,0.000000,0.0000,0

0000000\*f4ac8d54

表 7-98 ADRNAV 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  ADRNAV header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |         |   H    |   0      |
| 2   | sol status     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H        |
| 3   | pos type       | 位置类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                              | Enum    | 4      | H+4      |
| 4   | lat            | 纬度，deg                                                                                             | Double  | 8      | H+8      |
| 5   | lon            | 经度，deg                                                                                             | Double  | 8      | H+16     |
| 6   | hgt            | 海拔高，m                                                                                             | Double  | 8      | H+24     |
|  7  |  undulation    | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离，m                                                |  Float  |  4     |  H+32    |
|   8 |   datum id\#   | 坐标系 ID，当前仅支持 WGS84， ASCII 输出为 WGS84，二进制枚举 值为 61                                  |   Enum  |   4    |   H+36   |
| 9   | lat σ          | 纬度标准差，m                                                                                         | Float   | 4      | H+40     |
| 10  | lon σ          | 经度标准差，m                                                                                         | Float   | 4      | H+44     |
| 11  | hgt σ          | 高度标准差，m                                                                                         | Float   | 4      | H+48     |
| 12  | stn id         | 基站 ID                                                                                               | Char[4] | 4      | H+52     |
| 13  | diff_age       | 差分龄期，s                                                                                           | Float   | 4      | H+56     |
| 14  | sol_age        | 解龄期，s                                                                                             | Float   | 4      | H+60     |
| 15  | \#SVs          | 跟踪的卫星数                                                                                          | Uchar   | 1      | H+64     |
| 16  | \#solnSVs      | 使用的卫星数                                                                                          | Uchar   | 1      | H+65     |
| 17  | Reserved       | 保留                                                                                                  | Uchar   | 1      | H+66     |
| 18  | Reserved       | 保留                                                                                                  | Uchar   | 1      | H+67     |
| 19  | Reserved       | 保留                                                                                                  | Uchar   | 1      | H+68     |

| ID    | 字段                           | 数据描述                                                                                                                            | 类型     | 字节数 | 字节偏移 |
|-------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|  20   |  ext sol stat                  | 扩展解的状态，[表7-89 扩展解状](#_bookmark275) [态](#_bookmark275)                                                                  |  Hex     |  1     |  H+69    |
|   21  |  Galileo&BDS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                           |   Hex    |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码。参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273)[掩码](#_bookmark273) |    Hex   |    1   |    H+71  |
| 23    | sol status                     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                                                      | Enum     | 4      | H+72     |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                            | Enum     | 4      | H+76     |
|   25  |   latency                      | 根据速度时标计算的延迟值，s。用 历元时间减去延迟可得到更准确的速度结果。                                                            |   Float  |   4    |   H+80   |
| 26    | age                            | 差分龄期，s                                                                                                                         | Float    | 4      | H+84     |
| 27    | hor spd                        | 对地水平速度，m/s                                                                                                                   | Double   | 8      | H+88     |
|  28   |  trk gnd                       | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                                                                                  |  Double  |  8     |  H+96    |
|   29  |   vert spd                     | 垂直速度，m/s。正值表示高度增加（向上），负值表示高度下降 （向下）                                                                  |   Double |   8    |   H+104  |
| 30    | Verspd std                     | 高程速度标准差，单位 m/s                                                                                                            | Float    | 4      | H+112    |
| 31    | Horspd std                     | 水平速度标准差，单位 m/s                                                                                                            | Float    | 4      | H+116    |
| 32    | xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                   | Hex      | 4      | H+120    |
| 33    | [CR][LF]                       | 语句结束符(仅 ASCII)                                                                                                                | -        | -      | -        |

#### ADRNAVH 从天线的 RTK 位置和速度信息

本指令包含接收机从天线的载波相位 RTK 定位的位置及定位精度、状态、速度等信息。

Message ID: 2117 ASCII 输出语法:

ADRNAVHA 1

BINARY 输出语法:

ADRNAVHB 1

适用产品：UM982、UMD982消息输出：

\#ADRNAVHA,97,GPS,FINE,2190,364822000,0,0,18,9;INSUFFICIENT_OBS,NONE,0.0 0000000000,0.00000000000,-17.0000,17.0000,WGS84,0.0000,0.0000,0.0000,"0",0.000,

0.000,0,0,0,0,0,00,00,00,INSUFFICIENT_OBS,NONE,0.000,0.000,0.0000,0.000000,0.000

0,00000000\*da9317a3

表 7-99 ADRNAVH 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  ADRNAVH header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | sol status      | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum   | 4      | H        |
| 3   | pos type        | 位置类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                              | Enum   | 4      | H+4      |
| 4   | lat             | 纬度，deg                                                                                             | Double | 8      | H+8      |
| 5   | lon             | 经度，deg                                                                                             | Double | 8      | H+16     |
| 6   | hgt             | 海拔高，m                                                                                             | Double | 8      | H+24     |

| ID    | 字段                           | 数据描述                                                                                                                             | 类型    | 字节数 | 字节偏移 |
|-------|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|  7    |  undulation                    | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离，m                                                                               |  Float  |  4     |  H+32    |
|   8   |   datum id\#                   | 坐标系 ID，当前仅支持 WGS84， ASCII 输出为 WGS84，二进制枚举 值为 61                                                                 |   Enum  |   4    |   H+36   |
| 9     | lat σ                          | 纬度标准差，m                                                                                                                        | Float   | 4      | H+40     |
| 10    | lon σ                          | 经度标准差，m                                                                                                                        | Float   | 4      | H+44     |
| 11    | hgt σ                          | 高度标准差，m                                                                                                                        | Float   | 4      | H+48     |
| 12    | stn id                         | 基站 ID                                                                                                                              | Char[4] | 4      | H+52     |
| 13    | diff_age                       | 差分龄期，s                                                                                                                          | Float   | 4      | H+56     |
| 14    | sol_age                        | 解龄期，s                                                                                                                            | Float   | 4      | H+60     |
| 15    | \#SVs                          | 跟踪的卫星数                                                                                                                         | Uchar   | 1      | H+64     |
| 16    | \#solnSVs                      | 使用的卫星数                                                                                                                         | Uchar   | 1      | H+65     |
| 17    | Reserved                       | 保留                                                                                                                                 | Uchar   | 1      | H+66     |
| 18    | Reserved                       | 保留                                                                                                                                 | Uchar   | 1      | H+67     |
| 19    | Reserved                       | 保留                                                                                                                                 | Uchar   | 1      | H+68     |
| 20    | ext sol stat                   | 扩展解的状态，[表7-89 扩展解状态](#_bookmark275)                                                                                     | Hex     | 1      | H+69     |
|   21  |  Galileo&BDS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                            |   Hex   |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码。参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273) [掩码](#_bookmark273) |    Hex  |    1   |    H+71  |
| 23    | sol status                     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                                                       | Enum    | 4      | H+72     |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                             | Enum    | 4      | H+76     |

| ID   | 字段       | 数据描述                                                                 | 类型     | 字节数 | 字节偏移 |
|------|------------|--------------------------------------------------------------------------|----------|--------|----------|
|   25 |   latency  | 根据速度时标计算的延迟值，s。用 历元时间减去延迟可得到更准确的速度结果。 |   Float  |   4    |   H+80   |
| 26   | age        | 差分龄期，s                                                              | Float    | 4      | H+84     |
| 27   | hor spd    | 对地水平速度，m/s                                                        | Double   | 8      | H+88     |
|  28  |  trk gnd   | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                       |  Double  |  8     |  H+96    |
|   29 |   vert spd | 垂直速度，m/s。正值表示高度增加（向上），负值表示高度下降 （向下）       |   Double |   8    |   H+104  |
| 30   | Verspd std | 高程速度标准差，单位 m/s                                                 | Float    | 4      | H+112    |
| 31   | Horspd std | 水平速度标准差，单位 m/s                                                 | Float    | 4      | H+116    |
| 32   | xxxx       | 32 位 CRC 校验(仅 ASCII 和二进制)                                        | Hex      | 4      | H+120    |
| 33   | [CR][LF]   | 语句结束符(仅 ASCII)                                                     | -        | -      | -        |

#### PPPNAV PPP 定位的位置与速度信息

本指令包含接收机 PPP 定位的位置及定位精度、状态等信息。PPP 特定版本支持。

Message ID: 1026 ASCII 输出语法:

PPPNAVA 1

BINARY 输出语法:

PPPNAVB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPNAVA,64,GPS,FINE,2207,464961000,0,0,18,13;SOL_COMPUTED,PPP_CONVER

GING,40.07899442145,116.23661087189,65.8944,-8.4923,WGS84,1.8755,1.4254,2.4821, "0",1.000,0.000,53,48,48,46,0,00,03,ff\*2d9412be

表 7-100 PPPNAV 数据结构

| ID    | 字段           | 数据描述                                                                                                                                                                     | 类型     | 字节数 | 字节偏移 |
|-------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1   |  PPPNAV header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211)                                                                        |          |   H    |   0      |
| 2     | sol status     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                                                                                               | Enum     | 4      | H        |
| 3     | pos type       | 位置类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                                                                     | Enum     | 4      | H+4      |
| 4     | lat            | 纬度，deg                                                                                                                                                                    | Double   | 8      | H+8      |
| 5     | lon            | 经度，deg                                                                                                                                                                    | Double   | 8      | H+16     |
| 6     | hgt            | 海拔高，m                                                                                                                                                                    | Double   | 8      | H+24     |
|  7    |  undulation    | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离，m                                                                                                                       |  Float   |  4     |  H+32    |
|     8 |     datum id\# | 坐标系 ID，当前固定填写 WGS84，ASCII 输出为 WGS84，二 进制枚举值为 61，实际输出坐标系基准可使用 CONFIG PPP DATUM 进行配置，目前 PPP 支持 WGS84 与 B2b-PPP 系统的原始坐标输出 |     Enum |     4  |     H+36 |
| 9     | lat σ          | 纬度标准差，m                                                                                                                                                                | Float    | 4      | H+40     |
| 10    | lon σ          | 经度标准差，m                                                                                                                                                                | Float    | 4      | H+44     |
| 11    | hgt σ          | 高度标准差，m                                                                                                                                                                | Float    | 4      | H+48     |

| ID      | 字段                           | 数据描述                                                                                                                                                                  | 类型         | 字节数 | 字节偏移  |
|---------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------|-----------|
|      12 |      stn id                    | 基站 ID： 如果定位类型为 B2b，station ID为 9959、9960、9961； 如果定位类型为 E6 HAS，station ID 固定为 9901； 如果定位类型为 QZSS L6 MDC， station ID 为 9934、9936、9939 |      Char[4] |      4 |      H+52 |
| 13      | diff_age                       | 差分龄期，s                                                                                                                                                               | Float        | 4      | H+56      |
| 14      | sol_age                        | 解龄期，s                                                                                                                                                                 | Float        | 4      | H+60      |
| 15      | \#SVs                          | 跟踪的卫星数                                                                                                                                                              | Uchar        | 1      | H+64      |
| 16      | \#solnSVs                      | 使用的卫星数                                                                                                                                                              | Uchar        | 1      | H+65      |
| 17      | Reserved                       | 保留                                                                                                                                                                      | Uchar        | 1      | H+66      |
| 18      | Reserved                       | 保留                                                                                                                                                                      | Uchar        | 1      | H+67      |
| 19      | Reserved                       | 保留                                                                                                                                                                      | Uchar        | 1      | H+68      |
| 20      | ext sol stat                   | 扩展解的状态，[表7-89 扩展解状态](#_bookmark275)                                                                                                                          | Hex          | 1      | H+69      |
|   21    |  Galileo&BDS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                                                                 |   Hex        |   1    |   H+70    |
|    22   | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码。参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273)[掩码](#_bookmark273)                                       |    Hex       |    1   |    H+71   |
| 23      | xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                                                         | Hex          | 4      | H+72      |
| 24      | [CR][LF]                       | 语句结束符(仅 ASCII)                                                                                                                                                      | -            | -      | -         |

#### SPPNAV 伪距位置和速度信息

本指令包含接收机伪距定位的位置及定位精度、状态、速度等信息。

Message ID: 46 ASCII 输出语法:

SPPNAVA 1

BINARY 输出语法:

SPPNAVB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#SPPNAVA,97,GPS,FINE,2294,472312000,0,0,18,14;SOL_COMPUTED,SINGLE,40.07 895888272,116.23651029820,65.8312,-8.4925,WGS84,1.2221,1.1053,2.1970,"0",0.000,

0.000,50,28,28,0,1,12,12,41,SOL_COMPUTED,DOPPLER_VELOCITY,0.000,0.000,0.0046,

335.592288,0.0045,0.0194,0.0123\*fab56d4e

表 7-101 SPPNAV 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  SPPNAV header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | sol status     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum   | 4      | H        |
| 3   | pos type       | 位置类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                              | Enum   | 4      | H+4      |
| 4   | lat            | 纬度，deg                                                                                             | Double | 8      | H+8      |
| 5   | lon            | 经度，deg                                                                                             | Double | 8      | H+16     |
| 6   | hgt            | 海拔高，m                                                                                             | Double | 8      | H+24     |
|  7  |  undulation    | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离，m                                                |  Float |  4     |  H+32    |

| ID    | 字段                           | 数据描述                                                                                                                            | 类型    | 字节数 | 字节偏移 |
|-------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   8   |   datum id\#                   | 坐标系 ID，当前仅支持 WGS84， ASCII 输出为 WGS84，二进制枚举值为 61                                                                 |   Enum  |   4    |   H+36   |
| 9     | lat σ                          | 纬度标准差，m                                                                                                                       | Float   | 4      | H+40     |
| 10    | lon σ                          | 经度标准差，m                                                                                                                       | Float   | 4      | H+44     |
| 11    | hgt σ                          | 高度标准差，m                                                                                                                       | Float   | 4      | H+48     |
| 12    | stn id                         | 基站 ID                                                                                                                             | Char[4] | 4      | H+52     |
| 13    | diff_age                       | 差分龄期，s                                                                                                                         | Float   | 4      | H+56     |
| 14    | sol_age                        | 解龄期，s                                                                                                                           | Float   | 4      | H+60     |
| 15    | \#SVs                          | 跟踪的卫星数                                                                                                                        | Uchar   | 1      | H+64     |
| 16    | \#solnSVs                      | 使用的卫星数                                                                                                                        | Uchar   | 1      | H+65     |
| 17    | Reserved                       | 保留                                                                                                                                | Uchar   | 1      | H+66     |
| 18    | Reserved                       | 保留                                                                                                                                | Uchar   | 1      | H+67     |
| 19    | Reserved                       | 保留                                                                                                                                | Uchar   | 1      | H+68     |
| 20    | ext sol stat                   | 扩展解的状态，[表7-89 扩展解状态](#_bookmark275)                                                                                    | Hex     | 1      | H+69     |
|   21  |  Galileo&BDS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                           |   Hex   |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码。参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273)[掩码](#_bookmark273) |    Hex  |    1   |    H+71  |
| 23    | sol status                     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                                                      | Enum    | 4      | H+72     |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                            | Enum    | 4      | H+76     |

| ID   | 字段       | 数据描述                                                                 | 类型     | 字节数 | 字节偏移 |
|------|------------|--------------------------------------------------------------------------|----------|--------|----------|
|   25 |   latency  | 根据速度时标计算的延迟值，s。用 历元时间减去延迟可得到更准确的速度结果。 |   Float  |   4    |   H+80   |
| 26   | age        | 差分龄期，s                                                              | Float    | 4      | H+84     |
| 27   | hor spd    | 对地水平速度，m/s                                                        | Double   | 8      | H+88     |
|  28  |  trk gnd   | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                       |  Double  |  8     |  H+96    |
|   29 |   vert spd | 垂直速度，m/s。正值表示高度增加（向上），负值表示高度下降 （向下）       |   Double |   8    |   H+104  |
| 30   | Verspd std | 高程速度标准差，单位 m/s                                                 | Float    | 4      | H+112    |
| 31   | Horspd std | 水平速度标准差，单位 m/s                                                 | Float    | 4      | H+116    |
| 32   | xxxx       | 32 位 CRC 校验(仅 ASCII 和二进制)                                        | Hex      | 4      | H+120    |
| 33   | [CR][LF]   | 语句结束符(仅 ASCII)                                                     | -        | -      | -        |

#### SPPNAVH 从天线的伪距位置和速度信息

本指令包含接收机从天线伪距定位的位置及定位精度、状态、速度等信息。

Message ID: 2116 ASCII 输出语法:

SPPNAVHA 1

BINARY 输出语法:

SPPNAVHB 1

适用产品：UM982、UMD982消息输出：

\#SPPNAVHA,97,GPS,FINE,2190,364950000,0,0,18,13;INSUFFICIENT_OBS,NONE,4 0.07898868399,116.23660520125,59.8754,-8.4923,WGS84,2.9766,2.8787,10.0570,"0",0.

000,11624.000,0,0,0,0,33,02,00,00,INSUFFICIENT_OBS,NONE,0.000,0.000,0.0301,33.04

3127,-0.0892,0004000C\*808205f0

表 7-102 SPPNAVH 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  SPPNAVH header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |         |   H    |   0      |
| 2   | sol status      | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                        | Enum    | 4      | H        |
| 3   | pos type        | 位置类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                              | Enum    | 4      | H+4      |
| 4   | lat             | 纬度，deg                                                                                             | Double  | 8      | H+8      |
| 5   | lon             | 经度，deg                                                                                             | Double  | 8      | H+16     |
| 6   | hgt             | 海拔高，m                                                                                             | Double  | 8      | H+24     |
|  7  |  undulation     | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离，m                                                |  Float  |  4     |  H+32    |
|   8 |   datum id\#    | 坐标系 ID，当前仅支持 WGS84， ASCII 输出为 WGS84，二进制枚举值为 61                                   |   Enum  |   4    |   H+36   |
| 9   | lat σ           | 纬度标准差，m                                                                                         | Float   | 4      | H+40     |
| 10  | lon σ           | 经度标准差，m                                                                                         | Float   | 4      | H+44     |
| 11  | hgt σ           | 高度标准差，m                                                                                         | Float   | 4      | H+48     |
| 12  | stn id          | 基站 ID                                                                                               | Char[4] | 4      | H+52     |
| 13  | diff_age        | 差分龄期，s                                                                                           | Float   | 4      | H+56     |
| 14  | sol_age         | 解龄期，s                                                                                             | Float   | 4      | H+60     |
| 15  | \#SVs           | 跟踪的卫星数                                                                                          | Uchar   | 1      | H+64     |
| 16  | \#solnSVs       | 使用的卫星数                                                                                          | Uchar   | 1      | H+65     |
| 17  | Reserved        | 保留                                                                                                  | Uchar   | 1      | H+66     |
| 18  | Reserved        | 保留                                                                                                  | Uchar   | 1      | H+67     |

| ID    | 字段                           | 数据描述                                                                                                                            | 类型     | 字节数 | 字节偏移 |
|-------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
| 19    | Reserved                       | 保留                                                                                                                                | Uchar    | 1      | H+68     |
|  20   |  ext sol stat                  | 扩展解的状态，[表7-89 扩展解状](#_bookmark275) [态](#_bookmark275)                                                                  |  Hex     |  1     |  H+69    |
|   21  |  Galileo&BDS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                           |   Hex    |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码。参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信](#_bookmark273)[号掩码](#_bookmark273) |    Hex   |    1   |    H+71  |
| 23    | sol status                     | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                                                      | Enum     | 4      | H+72     |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速](#_bookmark434) [度类型](#_bookmark434)）                                                            | Enum     | 4      | H+76     |
|   25  |   latency                      | 根据速度时标计算的延迟值，s。用 历元时间减去延迟可得到更准确的速度结果。                                                            |   Float  |   4    |   H+80   |
| 26    | age                            | 差分龄期，s                                                                                                                         | Float    | 4      | H+84     |
| 27    | hor spd                        | 对地水平速度，m/s                                                                                                                   | Double   | 8      | H+88     |
|  28   |  trk gnd                       | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                                                                                  |  Double  |  8     |  H+96    |
|   29  |   vert spd                     | 垂直速度，m/s。正值表示高度增加（向上），负值表示高度下降 （向下）                                                                  |   Double |   8    |   H+104  |
| 30    | Verspd std                     | 高程速度标准差，单位 m/s                                                                                                            | Float    | 4      | H+112    |
| 31    | Horspd std                     | 水平速度标准差，单位 m/s                                                                                                            | Float    | 4      | H+116    |
| 32    | xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                   | Hex      | 4      | H+120    |
| 33    | [CR][LF]                       | 语句结束符(仅 ASCII)                                                                                                                | -        | -      | -        |

#### STADOP DOP 信息

精度因子信息。该消息为用于 Bestnav 解算的所有卫星的 DOP 值。

Message ID: 954 ASCII 输出语法:

STADOPA 1

Binary 输出语法：

STADOPB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#STADOPA,46,GPS,FINE,2298,280151000,0,0,18,12;280151000,0.8094,0.7129,0.383 1,0.6046,0.3779,0.2902,0.2421,5.0,0.0,50,4,7,8,9,16,18,26,31,34,35,36,39,51,60,61,58,59

,49,50,161,163,219,220,162,164,165,166,167,169,170,176,182,189,190,196,199,200,205, 206,187,181,76,77,79,84,82,98,99,86,85\*3e6acf8a

表 7-103 STADOP 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型  | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  STADOP Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | Reserved       | 保留位                                                                                                | Ulong | 4      | H        |
| 3   | gdop           | 几何精度因子                                                                                          | Float | 4      | H+4      |
| 4   | Pdop           | 位置精度因子                                                                                          | Float | 4      | H+8      |
| 5   | Tdop           | 时间精度因子                                                                                          | Float | 4      | H+12     |
| 6   | Vdop           | 垂直精度因子                                                                                          | Float | 4      | H+16     |
| 7   | Hdop           | 水平精度因子                                                                                          | Float | 4      | H+20     |

| ID    | 字段     | 数据描述                                                                                                                                | 类型      | 字节数 | 字节偏移       |
|-------|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
| 8     | Ndop     | 北向精度因子                                                                                                                            | Float     | 4      | H+24           |
| 9     | Edop     | 东向精度因子                                                                                                                            | Float     | 4      | H+28           |
| 10    | Cutoff   | 截止高度角                                                                                                                              | Float     | 4      | H+32           |
| 11    | Reserved | 保留位                                                                                                                                  | Float     | 4      | H+36           |
| 12    | \#PRN    | 跟踪卫星总数                                                                                                                            | UShort    | 2      | H+40           |
|    13 |    PRN   | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx    | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                      |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                                    | -         | -      | -              |

#### STADOPH 从天线 DOP 信息

从天线的精度因子信息。该消息为用于 BESTNAVH 解算的所有卫星的DOP 值。

Message ID: 2122 ASCII 输出语法:

STADOPHA 1

Binary 输出语法：

STADOPHB 1

适用产品：UM982、UMD982消息输出：

\#STADOPHA,46,GPS,FINE,2298,280151000,0,0,18,28;280151000,0.8182,0.7199,0.3 888,0.6079,0.3856,0.2972,0.2456,5.0,0.0,49,16,9,8,4,26,18,7,31,34,36,35,39,58,60,59,50,

49,51,61,161,163,220,219,162,164,165,169,167,166,176,170,182,190,189,196,181,206,2

05,200,199,79,77,76,99,98,84,82,86,85\*fd39dcfc

表 7-104 STADOPH 数据结构

| ID    | 字段            | 数据描述                                                                                                                                  | 类型      | 字节数 | 字节偏移       |
|-------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
|   1   |  STADOPH Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结 构请参考[表7-51](#_bookmark211)                                     |           |   H    |   0            |
| 2     | Reserved        | 保留位                                                                                                                                    | Ulong     | 4      | H              |
| 3     | gdop            | 几何精度因子                                                                                                                              | Float     | 4      | H+4            |
| 4     | Pdop            | 位置精度因子                                                                                                                              | Float     | 4      | H+8            |
| 5     | Tdop            | 时间精度因子                                                                                                                              | Float     | 4      | H+12           |
| 6     | Vdop            | 垂直精度因子                                                                                                                              | Float     | 4      | H+16           |
| 7     | Hdop            | 水平精度因子                                                                                                                              | Float     | 4      | H+20           |
| 8     | Ndop            | 北向精度因子                                                                                                                              | Float     | 4      | H+24           |
| 9     | Edop            | 东向精度因子                                                                                                                              | Float     | 4      | H+28           |
| 10    | Cutoff          | 截止高度角                                                                                                                                | Float     | 4      | H+32           |
| 11    | Reserved        | 保留位                                                                                                                                    | Float     | 4      | H+36           |
| 12    | \#PRN           | 跟踪卫星总数                                                                                                                              | UShort    | 2      | H+40           |
|    13 |    PRN          | 跟踪卫星的PRN（详见[表](#_bookmark217) [7-55 Unicore 消息中的卫星](#_bookmark217) [PRN 偏移](#_bookmark217)），在位置解可用前为 null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx           | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                        |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF]        | 语句结束符(仅 ASCII)                                                                                                                      | -         | -      | -              |

#### ADRDOP DOP 信息

精度因子信息。该消息为用于 ADRNAV 解算的所有卫星的 DOP 值。

Message ID: 953 ASCII 输出语法:

ADRDOPA 1

Binary 输出语法：

ADRDOPB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#ADRDOPA,59,GPS,FINE,2298,280152000,0,0,18,7;280152000,0.8093,0.7129,0.383 1,0.6045,0.3779,0.2902,0.2421,5.0,0.0,50,4,7,8,9,16,18,26,31,34,35,36,39,51,60,61,58,59

,49,50,161,163,219,220,162,164,165,166,167,169,170,176,182,189,190,196,199,200,205, 206,187,181,76,77,79,84,82,98,99,86,85\*0eea644e

表 7-105 ADRDOP 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型  | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  ADRDOP Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | Reserved       | 保留位                                                                                                | Ulong | 4      | H        |
| 3   | gdop           | 几何精度因子                                                                                          | Float | 4      | H+4      |
| 4   | Pdop           | 位置精度因子                                                                                          | Float | 4      | H+8      |
| 5   | Tdop           | 时间精度因子                                                                                          | Float | 4      | H+12     |
| 6   | Vdop           | 垂直精度因子                                                                                          | Float | 4      | H+16     |
| 7   | Hdop           | 水平精度因子                                                                                          | Float | 4      | H+20     |
| 8   | Ndop           | 北向精度因子                                                                                          | Float | 4      | H+24     |
| 9   | Edop           | 东向精度因子                                                                                          | Float | 4      | H+28     |
| 10  | Cutoff         | 截止高度角                                                                                            | Float | 4      | H+32     |

| ID    | 字段     | 数据描述                                                                                                                                | 类型      | 字节数 | 字节偏移       |
|-------|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
| 11    | Reserved | 保留位                                                                                                                                  | Float     | 4      | H+36           |
| 12    | \#PRN    | 跟踪卫星总数                                                                                                                            | UShort    | 2      | H+40           |
|    13 |    PRN   | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx    | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                      |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                                    | -         | -      | -              |

#### ADRDOPH 从天线 DOP 信息

精度因子信息。该消息为用于 ADRNAVH 解算的所有卫星的 DOP 值。

Message ID: 2121 ASCII 输出语法:

ADRDOPHA 1

Binary 输出语法：

ADRDOPHB 1

适用产品：UM982、UMD982消息输出：

\#ADRDOPHA,46,GPS,FINE,2298,280151000,0,0,18,19;280151000,0.8182,0.7199,0.3 888,0.6079,0.3856,0.2972,0.2456,5.0,0.0,49,16,9,8,4,26,18,7,31,34,36,35,39,58,60,59,50,

49,51,61,161,163,220,219,162,164,165,169,167,166,176,170,182,190,189,196,181,206,2

05,200,199,79,77,76,99,98,84,82,86,85\*1e0ad999

表 7-106 ADRDOPH 数据结构

| ID    | 字段            | 数据描述                                                                                                                                | 类型      | 字节数 | 字节偏移       |
|-------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
|   1   |  ADRDOPH Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结 构请参考[表7-51](#_bookmark211)                                   |           |   H    |   0            |
| 2     | Reserved        | 保留位                                                                                                                                  | Ulong     | 4      | H              |
| 3     | gdop            | 几何精度因子                                                                                                                            | Float     | 4      | H+4            |
| 4     | Pdop            | 位置精度因子                                                                                                                            | Float     | 4      | H+8            |
| 5     | Tdop            | 时间精度因子                                                                                                                            | Float     | 4      | H+12           |
| 6     | Vdop            | 垂直精度因子                                                                                                                            | Float     | 4      | H+16           |
| 7     | Hdop            | 水平精度因子                                                                                                                            | Float     | 4      | H+20           |
| 8     | Ndop            | 北向精度因子                                                                                                                            | Float     | 4      | H+24           |
| 9     | Edop            | 东向精度因子                                                                                                                            | Float     | 4      | H+28           |
| 10    | Cutoff          | 截止高度角                                                                                                                              | Float     | 4      | H+32           |
| 11    | Reserved        | 保留位                                                                                                                                  | Float     | 4      | H+36           |
| 12    | \#PRN           | 跟踪卫星总数                                                                                                                            | UShort    | 2      | H+40           |
|    13 |    PRN          | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx           | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                      |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF]        | 语句结束符(仅 ASCII)                                                                                                                    | -         | -      | -              |

#### PPPDOP DOP 信息

精度因子信息。该消息为用于 PPPNAV 解算的所有卫星的 DOP 值。PPP 特定版本支持。

Message ID: 1025

ASCII 输出语法:

PPPDOPA 1

Binary 输出语法：

PPPDOPB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPDOPA,60,GPS,FINE,2298,280475000,0,0,18,18;280475000,0.7632,0.6743,0.3574,0. 5637,0.3700,0.0000,0.0000,5.0,0.0,51,4,7,8,9,16,18,26,21,34,35,36,39,51,60,61,58,59,49,50,6

2,161,163,219,220,162,164,165,166,167,169,170,176,182,189,190,196,199,200,205,206,187,

181,76,77,79,84,82,98,99,86,85\*bb86e61e

表 7-107 PPPDOP 数据结构

| ID  | 字段           | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|----------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  PPPDOP Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | Reserved       | 保留位                                                                                                | Ulong  | 4      | H        |
| 3   | gdop           | 几何精度因子                                                                                          | Float  | 4      | H+4      |
| 4   | Pdop           | 位置精度因子                                                                                          | Float  | 4      | H+8      |
| 5   | Tdop           | 时间精度因子                                                                                          | Float  | 4      | H+12     |
| 6   | Vdop           | 垂直精度因子                                                                                          | Float  | 4      | H+16     |
| 7   | Hdop           | 水平精度因子                                                                                          | Float  | 4      | H+20     |
| 8   | Ndop           | 北向精度因子                                                                                          | Float  | 4      | H+24     |
| 9   | Edop           | 东向精度因子                                                                                          | Float  | 4      | H+28     |
| 10  | Cutoff         | 截止高度角                                                                                            | Float  | 4      | H+32     |
| 11  | Reserved       | 保留位                                                                                                | Float  | 4      | H+36     |
| 12  | \#PRN          | 跟踪卫星总数                                                                                          | UShort | 2      | H+40     |

| ID    | 字段     | 数据描述                                                                                                                                | 类型      | 字节数 | 字节偏移       |
|-------|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
|    13 |    PRN   | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx    | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                      |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                                    | -         | -      | -              |

#### SPPDOP DOP 信息

精度因子信息。该消息为用于SPPNAV 解算的所有卫星的DOP 值，支持ONCHANGED请求方式。SPPDOP 需要 SPPNAV 驱动。

Message ID: 173

ASCII 输出语法:

SPPDOPA 1

SPPDOPA ONCHANGED

Binary 输出语法：

SPPDOPB 1

SPPDOPB ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#SPPDOPA,46,GPS,FINE,2298,280151000,0,0,18,41;280151000,1.8370,1.5714,0.951 5,1.3668,0.7752,0.6649,0.3985,5.0,0.0,28,4,8,9,16,26,34,35,39,76,77,79,84,98,99,161,16

3,166,167,169,170,176,189,190,196,199,200,219,220\*6f7a59fd

表 7-108 SPPDOP 数据结构

| ID    | 字段           | 数据描述                                                                                                                                 | 类型      | 字节数 | 字节偏移       |
|-------|----------------|------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
|   1   |  SPPDOP Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)                                    |           |   H    |   0            |
| 2     | Reserved       | 保留位                                                                                                                                   | Ulong     | 4      | H              |
| 3     | gdop           | 几何精度因子                                                                                                                             | Float     | 4      | H+4            |
| 4     | Pdop           | 位置精度因子                                                                                                                             | Float     | 4      | H+8            |
| 5     | Tdop           | 时间精度因子                                                                                                                             | Float     | 4      | H+12           |
| 6     | Vdop           | 垂直精度因子                                                                                                                             | Float     | 4      | H+16           |
| 7     | Hdop           | 水平精度因子                                                                                                                             | Float     | 4      | H+20           |
| 8     | Ndop           | 北向精度因子                                                                                                                             | Float     | 4      | H+24           |
| 9     | Edop           | 东向精度因子                                                                                                                             | Float     | 4      | H+28           |
| 10    | Cutoff         | 截止高度角                                                                                                                               | Float     | 4      | H+32           |
| 11    | Reserved       | 保留位                                                                                                                                   | Float     | 4      | H+36           |
| 12    | \#PRN          | 跟踪卫星总数                                                                                                                             | UShort    | 2      | H+40           |
|    13 |    PRN         | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字 段 |    UShort |    2   |    H+42        |
|  14   |  xxxx          | 32 位 CRC 校验(仅 ASCII 和二进 制)                                                                                                       |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF]       | 语句结束符(仅 ASCII)                                                                                                                     | -         | -      | -              |

#### SPPDOPH 从天线 DOP 信息

从天线的精度因子信息。该消息为用于 SPPNAVH 解算的所有卫星的 DOP 值，支持 ONCHANGED 请求方式。

Message ID: 2120

ASCII 输出语法:

SPPDOPHA 1

SPPDOPHA ONCHANGED

Binary 输出语法：

SPPDOPHB 1

SPPDOPHB ONCHANGED

适用产品：UM982、UMD982消息输出：

\#SPPDOPHA,46,GPS,FINE,2298,280151000,0,0,18,52;280151000,1.8370,1.5714,0.9 515,1.3668,0.7752,0.6649,0.3985,5.0,0.0,28,4,8,9,16,26,34,35,39,76,77,79,84,98,99,161,

163,166,167,169,170,176,189,190,196,199,200,219,220\*3a8ad917

表 7-109 SPPDOPH 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型  | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  SPPDOPH Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | Reserved        | 保留位                                                                                                | Ulong | 4      | H        |
| 3   | gdop            | 几何精度因子                                                                                          | Float | 4      | H+4      |
| 4   | Pdop            | 位置精度因子                                                                                          | Float | 4      | H+8      |
| 5   | Tdop            | 时间精度因子                                                                                          | Float | 4      | H+12     |
| 6   | Vdop            | 垂直精度因子                                                                                          | Float | 4      | H+16     |
| 7   | Hdop            | 水平精度因子                                                                                          | Float | 4      | H+20     |
| 8   | Ndop            | 北向精度因子                                                                                          | Float | 4      | H+24     |
| 9   | Edop            | 东向精度因子                                                                                          | Float | 4      | H+28     |
| 10  | Cutoff          | 截止高度角                                                                                            | Float | 4      | H+32     |
| 11  | Reserved        | 保留位                                                                                                | Float | 4      | H+36     |

| ID    | 字段     | 数据描述                                                                                                                                | 类型      | 字节数 | 字节偏移       |
|-------|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------------|
| 12    | \#PRN    | 跟踪卫星总数                                                                                                                            | UShort    | 2      | H+40           |
|    13 |    PRN   | 跟踪卫星的PRN（详见[表7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217)[移](#_bookmark217)），在位置解可用前为null 字段 |    UShort |    2   |    H+42        |
|  14   |  xxxx    | 32 位 CRC 校验(仅 ASCII 和二 进制)                                                                                                      |  Hex      |  4     |  H+42+2\*\#PRN |
| 15    | [CR][LF] | 语句结束符(仅 ASCII)                                                                                                                    | -         | -      | -              |

#### SATSINFO 卫星信息

本消息包含 GNSS 板卡跟踪到的所有卫星信息，包括卫星总数、卫星 PRN、高度角、方位角、不同频点的信噪比。

Message ID：2124

ASCII 输出语法：

SATSINFOA 1

Binary 输出语法：

SATSINFOB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#SATSINFOA,96,GPS,FINE,2215,367199000,0,0,18,16;50,2,0,0,0,63,2,302,51,0,45,0, 2,0,42,9,2,4,48,17,0,37,0,3,0,43,14,3,0,39,9,3,5,225,14,0,42,0,2,0,37,9,2,6,35,64,0,47,0,3,

0,52,14,3,0,48,9,3,9,80,33,0,42,0,3,0,44,14,3,0,40,9,3,11,300,56,0,46,0,3,0,50,14,3,0,46,9

,3,12,277,37,0,42,0,2,0,41,9,2,17,134,31,0,44,0,2,0,41,9,2,19,130,53,0,46,0,2,0,43,9,2,20,

232,47,0,46,0,2,0,42,9,2,25,316,15,0,38,0,3,0,45,14,3,0,40,9,3,28,0,0,0,37,0,2,0,31,9,2,19

4,170,8,5,38,0,3,5,41,14,3,5,37,9,3,195,112,67,5,45,0,3,5,49,14,3,5,47,9,3,196,132,61,5,4

2,0,3,5,48,14,3,5,46,9,3,199,163,43,5,36,0,3,5,46,14,3,5,44,9,3,39,116,64,1,43,0,2,1,49,5,

2,55,316,30,1,43,0,2,1,46,5,2,52,242,10,1,39,0,2,1,39,5,2,38,35,28,1,40,0,2,1,41,5,2,61,9

3,29,1,42,0,2,1,45,5,2,54,22,62,1,47,0,2,1,50,5,2,40,180,27,1,42,0,2,1,45,5,2,46,342,4,1,3

4,0,2,1,39,5,2,11,93,61,4,33,0,3,4,52,17,3,4,50,21,3,42,114,67,4,34,0,4,4,51,21,4,4,48,8,4

,4,49,12,4,2,224,33,4,45,17,2,4,41,21,2,10,214,52,4,29,0,3,4,46,17,3,4,45,21,3,28,306,28,

4,29,0,4,4,44,21,4,4,41,8,4,4,42,12,4,40,180,42,4,31,0,4,4,44,21,4,4,43,8,4,4,43,12,4,8,28

9,63,4,31,0,3,4,48,17,3,4,46,21,3,43,8,79,4,36,0,4,4,51,21,4,4,47,8,4,4,50,12,4,7,197,46,4

,28,0,3,4,47,17,3,4,45,21,3,21,47,30,4,31,0,4,4,43,21,4,4,43,8,4,4,43,12,4,23,243,4,4,24,8

,2,4,30,12,2,4,123,26,4,43,17,2,4,41,21,2,5,248,16,4,38,17,2,4,35,21,2,1,139,36,4,28,0,3,

4,46,17,3,4,43,21,3,34,111,40,4,32,0,4,4,48,21,4,4,44,8,4,4,41,12,4,38,317,74,4,35,0,4,4,

49,21,4,4,47,8,4,4,49,12,4,2,311,18,3,39,2,3,3,45,17,3,3,43,12,3,4,136,38,3,43,2,3,3,48,1

7,3,3,46,12,3,10,0,0,3,47,2,3,3,53,17,3,3,50,12,3,11,325,63,3,43,2,3,3,47,17,3,3,45,12,3,1

2,71,45,3,42,2,3,3,45,17,3,3,42,12,3,19,63,32,3,40,2,3,3,40,17,3,3,38,12,3,24,203,15,3,37

,2,3,3,43,17,3,3,40,12,3,25,260,32,3,42,2,3,3,46,17,3,3,44,12,3,9,181,7,3,37,2,3,3,41,17,3

,3,39,12,3,36,286,19,3,34,2,3,3,42,17,3,3,38,12,3\*a79d3813

表 7-110 SATSINFO 数据结构

| ID | 字段            | 数据描述                                                                                                               | 类型  | 字节数 | 字节偏移 |
|----|-----------------|------------------------------------------------------------------------------------------------------------------------|-------|--------|----------|
|  1 | SATSINFO header | 消息头，二进制消息头结构请参考[表](#_bookmark210) [7-50](#_bookmark210)，ASCII消息头结构请参考[表 7-51](#_bookmark211) |       |  H     |  0       |
| 2  | Sat number      | 当前跟踪到的总卫星数                                                                                                   | Byte  | 1      | H        |
|  3 | Version number  |  版本号，默认填 2                                                                                                      |  Byte |  1     |  H+1     |
| 4  | reserve         | 保留字段                                                                                                               | Byte  | 1      | H+2      |
| 5  | reserve         | 保留字段                                                                                                               | Byte  | 1      | H+3      |
| 6  | reserve         | 保留字段                                                                                                               | Byte  | 1      | H+4      |
| 7  | Frq flag        | 频率标识，详见[表7-111 频率标识](#_bookmark315)                                                                        | Byte  | 1      | H+5      |
| 8  | PRN             | 卫星PRN号，详见[表7-54 Unicore消息中](#_bookmark216)                                                                   | Byte  | 1      | H+6      |

| ID    | 字段                                                                                                                                     | 数据描述                                        | 类型   | 字节数 | 字节偏移                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|--------|--------|---------------------------|
|       |                                                                                                                                          | [的卫星PRN](#_bookmark216)                      |        |        |                           |
| 9     | Azimuth                                                                                                                                  | 方位角，度                                      | Short  | 2      | H+7                       |
| 10    | Elevation                                                                                                                                | 高度角，度                                      | Byte   | 1      | H+9                       |
| 11    | Sys status                                                                                                                               | 系统标识，参见[表7-112 系统标识](#_bookmark316) | Byte   | 1      | H+10                      |
| 12    | SNR                                                                                                                                      | 信噪比                                          | Byte   | 1      | H+11                      |
| 13    | Freq status                                                                                                                              | 频点标识，参见[表7-113 频点标识](#_bookmark317) | Byte   | 1      | H+12                      |
| 14    | Freq No                                                                                                                                  | 当前PRN包含频点的数量                           | Byte   | 1      | H+13                      |
| 15    | Next Frq info                                                                                                                            | 卫星下一个频点信息（如有）                      |        |        |                           |
|  16   | 下一卫星偏移= H+6+sat\*(4+freq No\*4)，freq No根据实时解算频点信息更新；详见[图7-1](#_bookmark314) [SATSINFO字节偏移说明](#_bookmark314) |                                                 |        |        |                           |
|    17 |    xxxx                                                                                                                                  |    32位 CRC校验（仅 ASCII和二进制）             |    Hex |    4   | H+6+ sat\*(4 +freq No\*4) |
| 18    | [CR][LF]                                                                                                                                 | 语句结束符（仅ASCII）                           | -      | -      | -                         |

Length (PRN + Azimuth + Elevation) Length (Sys status + SNR + Freq status + Freq No)

###### SatsInfo = H + 6 + Sat \* ( 4 + Freq No \* 4 )

Header

Sat number

Freq No

Length (Sat number + Version number + reserve + reserve + reserve + Frq flag)

图 7-1 SATSINFO 字节偏移说明

表 7-111 频率标识

| Bit  | 描述             | 值               |
|------|------------------|------------------|
| Bit7 | 保留             | 0                |
| Bit6 | 保留             | 0                |
| Bit5 | BDS B2b、GPS L2P | 0：不含；1：含有 |

| Bit  | 描述                               | 值               |
|------|------------------------------------|------------------|
| Bit4 | BDS B2a、GLO G3、GAL E6            | 0：不含；1：含有 |
| Bit3 | BDS B1C、GPS L1C                   | 0：不含；1：含有 |
| Bit2 | GPS L5、BDS B3I、GAL E5a、IRNSS L5 | 0：不含；1：含有 |
| Bit1 | GPS L2C、GLO L2、BDS B2I、GAL E5b  | 0：不含；1：含有 |
| Bit0 | GPS L1C/A、GLO L1、BDS B1I、GAL E1 | 0：不含；1：含有 |

表 7-112 系统标识

| Bit  | 描述                                                            | 备注 |
|------|-----------------------------------------------------------------|------|
| Bit7 | 0 = GPS 1 = GLONASS 2 = SBAS 3 = GAL 4 = BDS 5 = QZSS 6 = IRNSS |      |
| Bit6 |                                                                 |      |
| Bit5 |                                                                 |      |
| Bit4 |                                                                 |      |
| Bit3 |                                                                 |      |
| Bit2 |                                                                 |      |
| Bit1 |                                                                 |      |
| Bit0 |                                                                 |      |

表 7-113 频点标识

| Bit  | 描述                                                                                                                                                                                                                          | 备注 |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Bit7 | GPS: BDS: 0 = L1 C/A 0 = B1I 9 = L2P (Y) 4 = B1Q 3 = L1C pilot 8 = B1C(Pilot) 11 = L1C data 23 = B1C(Data) 6 = L5 data 5 = B2Q 14 = L5 pilot 17 = B2I 17 = L2C (L) 12 = B2a(Pilot) 28 = B2a(Data) GLONASS: 6 = B3Q 0 = L1 C/A |      |
| Bit6 |                                                                                                                                                                                                                               |      |
| Bit5 |                                                                                                                                                                                                                               |      |
| Bit4 |                                                                                                                                                                                                                               |      |
| Bit3 |                                                                                                                                                                                                                               |      |
| Bit2 |                                                                                                                                                                                                                               |      |
| Bit1 |                                                                                                                                                                                                                               |      |
| Bit0 |                                                                                                                                                                                                                               |      |

| Bit | 描述                                                                                                                                                                                                                                                                                                 | 备注 |
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
|     | 5 = L2 C/A 21 = B3I 6 = G3I 13= B2b(I) 7 = G3Q GAL: QZSS: 1 = E1B 0 = L1 C/A 2 = E1C 6 = L5 data 12 = E5A pilot 14 = L5 pilot 17 = E5B pilot 17 = L2C (L) 18 = E6B 18 = L61 Data 22 = E6C 22 = L61 Pilot SBAS: 24 = L62 Data1 0 = L1 C/A 25 = L62 Data2 6 = L5 (I) IRNSS： 6 = L5 data 14 = L5 pilot |      |

#### BASEPOS 基准站模式下基准站位置的输出信息

该消息用于模块在固定基准站模式下，输出固定基站的实时位置，起到对基站位置进行实时动态监测的作用，给上位机提供一个可以判断基准站是否被外在因素移动的信息来源。

注意移动站模式下，该指令不生效。

Message ID：49 ASCII 输出语法：

BASEPOSA 1

Binary 输出语法：

BASEPOSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#BASEPOSA,96,GPS,FINE,2207,289028000,0,0,18,20;SOL_COMPUTED,SINGLE,40.0789 9984715,116.23661761328,64.8315,8.4923,WGS84,2.8968,2.0472,6.2202,"0",0.000,0.000,55,

28,28,0,16,12,01,51,SOL_COMPUTED,DOPPLER_VELOCITY,0.000,0.000,0.0044,52.887930,0.

0082,0.0205,0.0116\*80a5f451

表 7-114 BASEPOS 数据结构

| ID  | 字段            | 数据描述                                                                                              | 类型    | 字节数 | 字节偏移 |
|-----|-----------------|-------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  BASEPOS header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |         |   H    |   0      |
|  2  | p-sol status    |  解状态，参考[表0- 5 解的状态](#_bookmark435)                                                         |  Enum   |  4     |  H       |
|  3  |  pos type       | 位置类型（参考[表 0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                             |  Enum   |  4     |  H+4     |
| 4   | lat             | 纬度，deg                                                                                             | Double  | 8      | H+8      |
| 5   | lon             | 经度，deg                                                                                             | Double  | 8      | H+16     |
| 6   | hgt             | 海拔高，m                                                                                             | Double  | 8      | H+24     |
|  7  |  undulation     | 大地水准面差距- 大地水准面和 WGS84 椭球面之间的距离（米）                                             |  Float  |  4     |  H+32    |
|  8  |  datum id\#     | 坐标系 ID 号，当前仅支持 WGS84 （二进制为 61）                                                        |  Enum   |  4     |  H+36    |
| 9   | lat σ           | 纬度标准差，m                                                                                         | Float   | 4      | H+40     |
| 10  | lon σ           | 经度标准差，m                                                                                         | Float   | 4      | H+44     |
| 11  | hgt σ           | 高度标准差，m                                                                                         | Float   | 4      | H+48     |
| 12  | stn id          | 基站 ID，缺省值为 0                                                                                   | Char[4] | 4      | H+52     |

| ID    | 字段                           | 数据描述                                                                                                                               | 类型    | 字节数 | 字节偏移 |
|-------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
| 13    | diff_age                       | 差分龄期，s                                                                                                                            | Float   | 4      | H+56     |
| 14    | sol_age                        | 解的龄期，s                                                                                                                            | Float   | 4      | H+60     |
| 15    | \#SVs                          | 跟踪的卫星数                                                                                                                           | Uchar   | 1      | H+64     |
| 16    | \#solnSVs                      | 在解中使用的卫星数                                                                                                                     | Uchar   | 1      | H+65     |
| 17    | Reserved                       | 保留                                                                                                                                   | Uchar   | 1      | H+66     |
| 18    | Reserved                       | 保留                                                                                                                                   | Uchar   | 1      | H+67     |
| 19    | Reserved                       | 保留                                                                                                                                   | Uchar   | 1      | H+68     |
|  20   |  ext sol stat                  | 扩展解的状态，参考[表7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                                 |  Hex    |  1     |  H+69    |
|   21  | Galileo&B DS3 sig mask         | Galileo 和 BDS3 使用的信号掩码。 参考[表7-88 Galileo&BDS3 使用的](#_bookmark274)[信号掩码](#_bookmark274)                              |   Hex   |   1    |   H+70   |
|    22 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS 2 使用的信 号掩码（参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信](#_bookmark273)[号掩码](#_bookmark273)） |    Hex  |    1   |    H+71  |
|  23   | V-sol status                   |  解状态，参考[表0- 5 解的状态](#_bookmark435)                                                                                          |  Enum   |  4     |  H+72    |
| 24    | vel type                       | 速度类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                                                               | Enum    | 4      | H+76     |
|   25  |   latency                      | 根据速度时标计算的延迟值，以秒为单位。用历元时间减去延迟可得 到更准确的速度结果。                                                      |   Float |   4    |   H+80   |
| 26    | age                            | 差分龄期，s                                                                                                                            | Float   | 4      | H+84     |
| 27    | hor spd                        | 对地水平速度，m/s                                                                                                                      | Double  | 8      | H+88     |
|  28   |  trk gnd                       | 相对于真北的实际对地运动方向 （相对地面轨迹），deg                                                                                     |  Double |  8     |  H+96    |

| ID   | 字段       | 数据描述                                                           | 类型     | 字节数 | 字节偏移 |
|------|------------|--------------------------------------------------------------------|----------|--------|----------|
|   29 |   vert spd | 垂直速度，m/s，正值表示高度增加（向上），负值表示高度下降 （向下） |   Double |   8    |   H+104  |
| 30   | Verspd std | 高程速度标准差，单位 m/s                                           | Float    | 4      | H+112    |
| 31   | Horspd std | 水平速度标准差，单位 m/s                                           | Float    | 4      | H+116    |
| 32   | xxxx       | 32 位 CRC 校验(仅 ASCII 和二进制)                                  | Hex      | 4      | H+120    |
| 33   | [CR][LF]   | 语句结束符(仅 ASCII)                                               | -        | -      | -        |

#### SATELLITE 可见卫星

该消息包含可见卫星列表及卫星信息。

Message ID: 1042 ASCII 输出语法:

SATELLITEA 1

Binary 输出语法:

SATELLITEB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出:

\#SATELLITEA,97,GPS,FINE,2190,364984000,0,0,18,13;GPS,TRUE,TRUE,9,3,0,25.2,3 08.1,0.000,0.000,10,0,2.4,175.2,0.000,0.000,12,0,0.2,39.3,0.000,0.000,16,0,12.5,210.8,0.

000,0.000,25,0,31.8,47.4,0.000,0.000,26,0,51.2,209.4,0.000,0.000,29,0,25.0,90.5,0.000,0.

000,31,0,71.2,345.0,0.000,0.000,32,0,56.6,127.5,0.000,0.000\*a60a9635

表 7-115 SATELLITE 数据结构

| ID           | 字段                | 数据描述                                                                                                                                                                                                                                                                                                                                                                                                                                               | 类型             | 字节数       | 字节偏移        |
|--------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|--------------|-----------------|
|   1          |  SATELLITE header   | 消息头，二进制消息头结构请参考[表](#_bookmark210) [7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211)                                                                                                                                                                                                                                                                                                               |                  |   H          |   0             |
|  2           | Satellite system    | GNSS 卫星系统列表，参考[表7-116](#_bookmark322) [卫星系统](#_bookmark322)                                                                                                                                                                                                                                                                                                                                                                              |  Enum            |  4           |  H              |
| 3            | sat vis             | 卫星是否可视，0 = FALSE 1 = TRUE                                                                                                                                                                                                                                                                                                                                                                                                                       | Enum             | 4            | H+4             |
|  4           |  comp alm           | 是否使用了北斗/GPS/GLONASS 完整 历书，0 = FALSE 1 = TRUE                                                                                                                                                                                                                                                                                                                                                                                               |  Enum            |  4           |  H+8            |
| 5            | \#sat               | 所有数据的卫星数                                                                                                                                                                                                                                                                                                                                                                                                                                       | Ulong            | 4            | H+12            |
|            6 |            PRN/slot | 卫星 PRN 号（详见[表7-54 Unicore](#_bookmark216)[消息中的卫星 PRN](#_bookmark216)）。 在二进制消息中，卫星 ID 字段由两个 Ushort 组成。最低的两个字节是系统标识符:（如 GPS 的 PRN，GLONASS的通道号），为 USHORT 类型；最高的两个字节是 GLONASS 的频率通 道，其它系统这两个字节值为零。在 ASCII 消息中，卫星 ID 字段是系统标识符。如果系统是 GLONASS，而频率通道不是零，则在系统标识符后加上频率通道数。例如，系统标识符是 13，频率通道-2，输出为 13-2。 |            Ulong |            4 |            H+16 |
| 7            | health              | 卫星健康状态，0=健康，1=不健康                                                                                                                                                                                                                                                                                                                                                                                                                         | Ulong            | 4            | H+20            |
| 8            | elev                | 仰角，deg                                                                                                                                                                                                                                                                                                                                                                                                                                              | Double           | 8            | H+24            |
| 9            | az                  | 方位角，deg                                                                                                                                                                                                                                                                                                                                                                                                                                            | Double           | 8            | H+32            |
| 10           | reserved            | 保留                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Double           | 8            | H+40            |

| ID   | 字段                                  | 数据描述                            | 类型   | 字节数 | 字节偏移           |
|------|---------------------------------------|-------------------------------------|--------|--------|--------------------|
| 11   | reserved                              | 保留                                | Double | 8      | H+48               |
| 12   | 下一卫星偏移为字段 6\~11 循环\#sat 次 |                                     |        |        |                    |
|   13 |   xxxx                                |   32 位 CRC 校验(仅 ASCII 和二进制) |   Hex  |   4    | H+12+ (\#sat x 40) |
| 14   | [CR][LF]                              | 语句结束符(仅 ASCII)                | -      | -      | -                  |

表 7-116 卫星系统

| 二进制值 | ASCII 格式的卫星系统名称 |
|----------|--------------------------|
| 0        | GPS                      |
| 1        | GLONASS                  |
| 2        | SBAS                     |
| 5        | GALILEO                  |
| 6        | BEIDOU                   |
| 7        | QZSS                     |
| 9        | NAVIC                    |

#### SATECEF 直角坐标中的卫星位置

该消息包含位置解算所需的解码卫星信息：卫星坐标（ECEF WGS84），卫星时钟校正，电离层校正和对流层校正信息。

Message ID: 2115

ASCII 输出语法:

SATECEFA 1

Binary 输出语法:

SATECEFB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出:

\#SATECEFA,97,GPS,FINE,2190,365060000,0,0,18,12;28,GPS,25,-15074001.0000,-13 21521.1250,21554962.0000,78939.508,8.906,4.603,0.0,GPS,26,-5199400.0000,2515496

8.0000,6019832.0000,50877.914,6.491,3.066,0.0,GPS,29,-24350838.0000,1869061.6250,

10471350.0000,-138099.781,10.301,5.618,0.0,GPS,31,-5542408.0000,14613293.0000,21

302554.0000,-47215.703,5.403,2.538,0.0,GPS,32,-18396664.0000,16438964.0000,97068

92.0000,-12763.542,6.180,2.902,0.0,QZSS,194,-26913374.0000,25085678.0000,2557819

8.0000,-202.491,5.491,2.560,0.0,QZSS,199,-25393438.0000,33651112.0000,4994.1079,

3.026,7.522,3.566,0.0,GALILEO,3,7417062.5000,15510334.0000,24086542.0000,-15340

0.016,7.043,3.451,1.0,GALILEO,5,-12822431.0000,21697142.0000,15516904.0000,-6674

5.031,5.324,2.456,1.0,GALILEO,24,-14646293.0000,12395834.0000,22518314.0000,-391

926.406,5.595,2.636,1.0,GALILEO,25,-3816618.5000,28188316.0000,8166408.5000,-167

453.578,6.307,2.980,1.0,BEIDOU,1,-34395868.0000,24403858.0000,-356958.1562,-8741

3.930,8.793,4.208,2.0,BEIDOU,2,4489574.5000,41931996.0000,342.9382,227784.938,8.9

65,4.403,2.0,BEIDOU,3,-14650923.0000,39556356.0000,-831224.1250,141089.422,7.68

2,3.588,2.0,BEIDOU,6,-11866700.0000,23972774.0000,32526292.0000,215105.672,5.39

6,2.463,2.0,BEIDOU,7,-12324336.0000,40175348.0000,-4187626.7500,18499.482,8.480,

4.034,2.0,BEIDOU,9,-3438167.7500,24575944.0000,34374596.0000,-117248.531,5.592,

2.592,2.0,BEIDOU,16,-16779596.0000,22749714.0000,31341410.0000,12072.259,5.408,

2.465,2.0,BEIDOU,19,-14636672.0000,23563198.0000,-3078972.7500,274718.438,9.268,

4.502,2.0,BEIDOU,21,12200400.0000,10552887.0000,22784140.0000,-286255.938,9.48

8,5.114,2.0,BEIDOU,22,-1677701.1250,24076402.0000,14022415.0000,-288599.844,5.80

2,2.686,2.0,BEIDOU,36,-7533112.0000,16531093.0000,21199316.0000,-254393.703,5.39

3,2.461,2.0,BEIDOU,39,-20703172.0000,22689450.0000,28809826.0000,10351.210,5.45

1,2.486,2.0,BEIDOU,40,-20012358.0000,37200804.0000,70317.0625,69271.031,7.476,3.

475,2.0,BEIDOU,45,8088047.5000,25093244.0000,9098498.0000,191929.906,8.316,4.06

1,2.0,BEIDOU,46,-18328430.0000,-1177068.3750,21021694.0000,-26218.129,9.093,4.59

6,2.0,BEIDOU,59,-32338378.0000,27044200.0000,513189.9062,6.267,8.236,3.879,2.0,BE IDOU,60,7289870.5000,41498212.0000,-1629297.3750,-43.630,9.758,4.989,2.0\*017f82f3

表 7-117 SATECEF 数据结构

| ID            | 字段             | 数据描述                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 类型             | 字节数        | 字节偏移        |
|---------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|---------------|-----------------|
|   1           |   SATECEF header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211)                                                                                                                                                                                                                                                                                                                                                    |                  |   H           |   0             |
| 2             | SatNum           | 卫星数                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Ulong            | 4             | H               |
|  3            |  GNSS_SYSTEM     | GNSS 卫星系统列表，参考[表](#_bookmark322) [7-116 卫星系统](#_bookmark322)                                                                                                                                                                                                                                                                                                                                                                               |  Enum            |  4            |  H+4            |
|             4 |             Prn  | 卫星 PRN 号（详见[表7-54 Unicore](#_bookmark216)[消息中的卫星 PRN](#_bookmark216)）。 在二进制消息中，卫星 ID 字段由两个 Ushort 组成。最低的两个字节是系统标识符:（如 GPS 的 PRN， GLONASS 的通道号），为 USHORT 类型；最高的两个字节是 GLONASS 的频率通道，其它系统这两个字节值为零。在 ASCII 消息中，卫星 ID 字段是系统标识符。如果系统是 GLONASS，而频率通道 不是零，则在系统标识符后加上频率通道数。例如，系统标识符是 13，频率通道-2，输出为 13-2。 |             UINT |             4 |             H+8 |
| 5             | SatCoord_X       | 卫星 X 轴（ECEF，m）                                                                                                                                                                                                                                                                                                                                                                                                                                     | Float            | 4             | H+12            |
| 6             | SatCoord_Y       | 卫星 Y 轴（ECEF，m）                                                                                                                                                                                                                                                                                                                                                                                                                                     | Float            | 4             | H+16            |
| 7             | SatCoord_Z       | 卫星 Z 轴（ECEF，m）                                                                                                                                                                                                                                                                                                                                                                                                                                     | Float            | 4             | H+20            |
| 8             | Satclk           | 卫星时钟校正（m）                                                                                                                                                                                                                                                                                                                                                                                                                                        | Float            | 4             | H+24            |

| ID | 字段                                  | 数据描述                          | 类型   | 字节数 | 字节偏移 |
|----|---------------------------------------|-----------------------------------|--------|--------|----------|
| 9  | IonoDelay                             | 电离层延迟，m                     | Float  | 4      | H+28     |
| 10 | TropDelay                             | 对流层延迟，m                     | Float  | 4      | H+32     |
| 11 | dReserved1                            | 保留                              | Double | 8      | H+36     |
| 12 | 下一卫星偏移= H + 4 + (\#SatNum x 40) |                                   |        |        |          |
| 13 | xxxx                                  | 32 位 CRC 校验(仅 ASCII 和二进制) | Hex    | 4      |          |
| 14 | [CR][LF]                              | 语句结束符(仅 ASCII)              | -      | -      | -        |

#### RECTIME 时间信息

该 Log 提供了几个时间相关的信息，包括接收机钟差和 UTC 时间偏差等。

Message ID: 102 ASCII 输出语法:

RECTIMEA 1

Binary 输出语法:

RECTIMEB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#RECTIMEA,97,GPS,FINE,2190,365121000,0,0,18,12;VALID,3.580410506e- 04,0.000000000e+00,-18.00000000000,2021,12,30,5,25,3000,VALID\*7e364e74

表 7-118 RECTIME 数据结构

| ID | 字段           | 数据描述                                                                                                               | 类型 | 字节数 | 字节偏移 |
|----|----------------|------------------------------------------------------------------------------------------------------------------------|------|--------|----------|
|  1 | RECTIME header | 消息头，二进制消息头结构请参考[表](#_bookmark210) [7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |      |  H     |  0       |

| ID    | 字段           | 数据描述                                                                                                                                  | 类型      | 字节数 | 字节偏移 |
|-------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|   2   |   clock status | 时钟模型状态。0 = VALID，有效；3 = INVALID，无效。二进制信息输出时显示 0 或 3 枚举值                                                      |   Enum    |   4    |   H      |
|    3  |    offset      | 相对于 GPS 时的接收机钟差，s。正值意味着接收机时钟早于 GPS 时间。要得出 GPS 的时间，请使用下面的公式： GPS 时间= 接收机时间-钟差          |    Double |    8   |    H+4   |
| 4     | Offset std     | 接收机钟差的标准差，s                                                                                                                     | Double    | 8      | H+12     |
|    5  |    utc offset  | GPS 时间到UTC 时间的偏差，通过历书参数计算，s。UTC 时间为 GPS 的时间加上当前的UTC 偏差加上接收机钟差： UTC 时间= GPS 时间+ 钟差+ UTC 偏差 |    Double |    8   |    H+20  |
| 6     | utc year       | UTC 年                                                                                                                                    | Ulong     | 4      | H+28     |
| 7     | utc month      | UTC 月 (0-12)10                                                                                                                           | Uchar     | 1      | H+32     |
| 8     | utc day        | UTC 天 (0-31)11                                                                                                                           | Uchar     | 1      | H+33     |
| 9     | utc hour       | UTC 小时 (0-23)                                                                                                                           | Uchar     | 1      | H+34     |
| 10    | utc min        | UTC 分钟 (0-59)                                                                                                                           | Uchar     | 1      | H+35     |
| 11    | utc ms         | UTC 毫秒 (0-60999)12                                                                                                                      | Ulong     | 4      | H+36     |
|    12 |    utc status  | UTC 状态：0 = INVALID，无效； 1 = VALID，有效； 2 = WARNING13，警告。二进制信息输出时显示 0、1 或 2 枚举 值。                             |    Enum   |    4   |    H+40  |
| 13    | xxxx           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                         | Hex       | 4      | H+44     |
| 14    | [CR][LF]       | 语句结束符(仅 ASCII)                                                                                                                      | -         | -      | -        |

10, [11](#_bookmark327) 如果UTC 时间未知，月和日的值均为 0

12 使用闰秒时最大值为 60999

13 指示由于缺少历书采用默认闰秒值

#### UNIHEADING 航向信息

本指令输出包含接收机运动的航向。航向是指接收机的主天线（ANT1）与从天线

（ANT2）之间构成一个基线向量，从真北顺时针方向到此基线向量的夹角。该条信息当前可从定向接收机（HEADING）输出。

Message ID: 972

ASCII 输出语法:

UNIHEADINGA 1

Binary 输出语法:

UNIHEADINGB 1

适用产品：UM982、UMD982消息输出：

\#UNIHEADINGA,97,GPS,FINE,2190,365174000,0,0,18,12;INSUFFICIENT_OBS,NONE

,0.0000,0.0000,0.0000,0.0000,0.0000,0.0000,"",0,0,0,0,0,00,0,0\*ee072604

表 7-119 UNIHEADING 数据结构

| ID  | 字段               | 数据描述                                                                                               | 类型  | 字节数 | 字节偏移 |
|-----|--------------------|--------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  UNIHEADING header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | sol stat           | 解状态（参考[表0- 5 解的状态](#_bookmark435)）                                                         | Enum  | 4      | H        |
| 3   | pos type           | 位置类型（参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                               | Enum  | 4      | H+4      |
| 4   | length             | 基线长                                                                                                 | Float | 4      | H+8      |
| 5   | heading            | 航向(0 到 360.0 deg)                                                                                   | Float | 4      | H+12     |
| 6   | pitch              | 俯仰(±90 deg)                                                                                          | Float | 4      | H+16     |
| 7   | Reserved           | 保留                                                                                                   | Float | 4      | H+20     |

| ID    | 字段                            | 数据描述                                                                                                                            | 类型     | 字节数 | 字节偏移 |
|-------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
| 8     | hdgstddev                       | 航向标准偏差                                                                                                                        | Float    | 4      | H+24     |
| 9     | ptchstddev                      | 俯仰标准偏差                                                                                                                        | Float    | 4      | H+28     |
| 10    | stn id                          | 基站 ID                                                                                                                             | Char[4]  | 4      | H+32     |
| 11    | \#SVs                           | 跟踪的卫星数                                                                                                                        | Uchar    | 1      | H+36     |
| 12    | \#solnSVs                       | 使用的卫星数                                                                                                                        | Uchar    | 1      | H+37     |
| 13    | \#obs                           | 截止高度角以上的卫星数                                                                                                              | Uchar    | 1      | H+38     |
| 14    | \#multi                         | 截止高度角以上有L2 观测的卫星数                                                                                                     | Uchar    | 1      | H+39     |
| 15    | Reserved                        | 保留                                                                                                                                | Uchar    | 1      | H+40     |
|  16   |  ext sol stat                   | 扩展解的状态，参考[表 7-89 扩展](#_bookmark275) [解状态](#_bookmark275)                                                             |  Uchar   |  1     |  H+41    |
|   17  |  Galileo&BDS3 sig mask          | Galileo 和BDS3 使用的信号掩码。参考[表 7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                           |   Uchar  |   1    |   H+42   |
|    18 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码，参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信](#_bookmark273)[号掩码](#_bookmark273) |    Uchar |    1   |    H+43  |
| 19    | xxxx                            | 32 位CRC 校验(仅 ASCII 和二进制)                                                                                                    | Hex      | 4      | H+44     |
| 20    | [CR][LF]                        | 语句结束符(仅 ASCII)                                                                                                                | \_       | \_     | \_       |

-   若 INS 为使能状态，当解状态sol stat 为 0 时，增加了位置类型 pos type 为 INS 的情况，此时输出由 INS 计算并折算至 GNSS 双天线定向模式下航向、俯仰角的结果，用户需要结合解状态与位置类

    型共同判断航向信息的有效性及计算来源。

#### UNIHEADING2 多流动站定向信息

该 Log 包含接收机运动的航向。航向是指移动基站（MOVINGBASE）至定向接收机

（HEADING）之间构成一个基线向量，从真北顺时针方向到此基线向量的夹角。该 Log 当前可从定向接收机（HEADING）输出。本指令与 UNIHEADING 信息类似，但额外有一个流动站 ID 字段。

Message ID: 1331

ASCII 输出语法:

UNIHEADING2A ONCHANGED

Binary 输出语法:

UNIHEADING2B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#UNIHEADING2A,50,GPS,FINE,2207,282484000,0,0,18,675;SOL_COMPUTED,NARR OW_INT,10736.3838,88.3470,0.0876,0.0000,0.0001,0.0001,"201",52,29,29,29,3,01,3,c3\* 898773d6

表 7-120 UNIHEADING2 数据结构

| ID  | 字段                 | 数据描述                                                                                               | 类型  | 字节数 | 字节偏移 |
|-----|----------------------|--------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  UNIHEADIN G2 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |       |   H    |   0      |
| 2   | sol stat             | 解状态，参考[表0- 5 解的状态](#_bookmark435)                                                           | Enum  | 4      | H        |
| 3   | pos type             | 位置类型（参考[表 0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)）                              | Enum  | 4      | H+4      |
| 4   | length               | 基线长                                                                                                 | Float | 4      | H+8      |

| ID    | 字段                           | 数据描述                                                                                                                            | 类型     | 字节数 | 字节偏移 |
|-------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
| 5     | heading                        | 航向(0 到 360.0 deg)                                                                                                                | Float    | 4      | H+12     |
| 6     | pitch                          | 俯仰(±90 deg)                                                                                                                       | Float    | 4      | H+16     |
| 7     | Reserved                       | 保留                                                                                                                                | Float    | 4      | H+20     |
| 8     | hdgstddev                      | 航向标准偏差                                                                                                                        | Float    | 4      | H+24     |
| 9     | ptchstddev                     | 俯仰标准偏差                                                                                                                        | Float    | 4      | H+28     |
| 10    | Master stn ID                  | 主站 ID                                                                                                                             | Char[4]  | 4      | H+32     |
| 11    | \#SVs                          | 跟踪的卫星数                                                                                                                        | Uchar    | 1      | H+36     |
| 12    | \#solnSVs                      | 使用的卫星数                                                                                                                        | Uchar    | 1      | H+37     |
| 13    | \#obs                          | 截止高度角以上的卫星数                                                                                                              | Uchar    | 1      | H+38     |
| 14    | \#multi                        | 截止高度角以上有 L2 观测的卫星数                                                                                                    | Uchar    | 1      | H+39     |
| 15    | Reserved                       | 保留                                                                                                                                | Uchar    | 1      | H+40     |
|  16   |  ext sol stat                  | 扩展解的状态，参考[表 7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                             |  Uchar   |  1     |  H+41    |
|   17  |  Galileo&BDS 3 sig mask        | Galileo 和 BDS3 使用的信号掩码。参考[表 7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                          |   Uchar  |   1    |   H+42   |
|    18 | GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码，参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号](#_bookmark273)[掩码](#_bookmark273) |    Uchar |    1   |    H+43  |
| 19    | xxxx                           | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                                   | Hex      | 4      | H+44     |
| 20    | [CR][LF]                       | 语句结束符(仅 ASCII)                                                                                                                | -        | -      |          |

#### HEADINGSTATUS Heading 解算状态

用于查询当前接收机 Heading 的解算状态。

Message ID：521

ASCII 输出语法：

HEADINGSTATUSA 1

Binary 输出语法：

HEADINGSTATUSB 1

适用产品：UM982、UMD982消息输出：

\#HEADINGSTATUSA,40,GPS,FINE,2255,117816000,0,0,18,15;233.0000,123.0000,0.0

,0.0,0.0,0.0,0,0\*5d660f9c

表 7-121 HEADINGSTATUS 数据结构

| 序号 | 字段                   | 内容                                                                                                   | 类型   | 字节数 | 字节偏移 |
|------|------------------------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1  |  HEADINGSTAT US Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |        |   H    |   0      |
|  2   |  CfgLength             | CONFIG HEADING LENGTH 中被 配置的基线长度                                                              |  Float |  4     |  H       |
|  3   |  Cfgtol                | CONFIG HEADING LENGTH 中被 配置的容忍误差                                                              |  Float |  4     |  H+4     |
| 4    | Reserved               | 保留位                                                                                                 | Float  | 4      | H+8      |
| 5    | Reserved               | 保留位                                                                                                 | Float  | 4      | H+12     |
| 6    | Reserved               | 保留位                                                                                                 | Float  | 4      | H+16     |
| 7    | Reserved               | 保留位                                                                                                 | Float  | 4      | H+20     |
| 8    | Reserved               | 保留位                                                                                                 | UINT   | 4      | H+24     |
| 9    | Reserved               | 保留位                                                                                                 | UINT   | 4      | H+28     |
|  10  |  Xxxx                  | 32 位 CRC 校验 (仅 ASCII 和二进 制)                                                                    |  Hex   |  4     |  H+32    |
| 11   | [CR][LF]               | 语句结束符(仅 ASCII)                                                                                   |        |        |          |

#### RTKSTATUS RTK 解算状态信息

用于查询接收机 RTK 解算的相关信息，如当前的定位状态，差分源的数据信息等。

Message ID: 509 ASCII 输出语法:

RTKSTATUSA 1

Binary 输出语法:

RTKSTATUSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#RTKSTATUSA,97,GPS,FINE,2190,365354000,0,0,18,1;0,0,0,0,0,0,0,0,0,0,0,NONE,0, 0,0,0,0\*f06a8a06

表 7-122 RTKSTATUS 数据结构

| 序号 | 字段              | 内容                                                                                                            | 类型    | 字节数 | 字节偏移 |
|------|-------------------|-----------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |  RTKSTATUS Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)          |         |   H    |   0      |
|    2 |    gpsSource      | GPS 系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的 可用改正值时则对应 bit 位置为 1，按 16 进制显示； |    UINT |    4   |    H     |
| 3    | Reserved          | 保留位                                                                                                          | UINT    | 4      | H+4      |
|    4 |    bdsSource1     | 北斗系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的可用改正值时则对应 bit 位置为 1，按 16 进制显示；  |    UINT |    4   |    H+8   |

| 序号  | 字段          | 内容                                                                                                              | 类型    | 字节数 | 字节偏移 |
|-------|---------------|-------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|    5  |    bdsSource2 | 北斗系统 33 到 63 号卫星显示， 源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+12  |
| 6     | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+16     |
|    7  |    gloSource  | GLO 系统 1 到 23 号卫星显示， 源数据解析状态，收到 1 颗卫星 的可用改正值时则对应bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+20  |
| 8     | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+24     |
|    9  |    galSource1 | Gal 系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的可用改正值时则对应 bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+28  |
|    10 |    galSource2 | Gal 系统 33 到 36 号卫星显示， 源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+32  |
|    11 |    QzssSource | QZSS 系统 193 到 202 号卫星显 示，源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示； |    UINT |    4   |    H+36  |
| 12    | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+40     |
| 13    | Pos type      | 位置类型，（参考[表 0- 4 位置或](#_bookmark434) [速度类型](#_bookmark434)）                                       | Enum    | 4      | H+44     |

| 序号     | 字段                  | 内容                                                                                                                                                             | 类型       | 字节数  | 字节偏移   |
|----------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|---------|------------|
|       14 |      Calculate status | 0：无差分源数据输入 1：差分源可用观测值不足 2：差分源延迟较大 3：电离层活跃（基准站模式有效） 4：ROVER 端观测值不足 5：满足 RTK 解算 说明 RTK/RTD 模块解算的状态 |       Enum |       4 |       H+48 |
|    15    |    Ion detected       | 电离层闪烁对 RTK 定位结果的影响 0：对 RTK 解没有影响 1\~255：对 RTK 解存在负面影响                                                                               |    uchar   |    1    |    H+52    |
|     16   |     Dual rtk flag\*   | 0xFF：未配置双天线基线长度 0：未解算出基线长（双天线未全部进入固定解） 1：未超标 2：超标 仅适用于双天线产品                                                      |     Uchar  |     1   |     H+53   |
| 17       | ADR Number            | 载波有效观测值总个数                                                                                                                                             | Uchar      | 1       | H+54       |
| 18       | Reserved              | 保留位                                                                                                                                                           | Uchar      | 1       | H+55       |
| 19       | Xxxx                  | 32 位 CRC 校验                                                                                                                                                   | Hex        | 4       | H+56       |
| 20       | [CR][LF]              | 结束符                                                                                                                                                           |            |         |            |

\* 字段 16（Dual rtk flag）：UM982 Build9669 及之后的版本支持

#### RTKSTATUS2 从天线的 RTK 解算状态信息

用于查询接收机从天线 RTK 解算的相关信息，如当前的定位状态，差分源的数据信息等。

Message ID: 691 ASCII 输出语法:

RTKSTATUS2A 1

Binary 输出语法:

RTKSTATUS2B 1

适用产品：UM982消息输出：

\#RTKSTATUS2A,39,GPS,FINE,2331,283227000,16117,0,18,54;89D24A00,0,81C0B1B F,3C000161,0,6380E,0,1805096,2,4E,0,NARROW_INT,5,0,FF,110,0\*8b15c636

表 7-123 RTKSTATUS2 数据结构

| 序号 | 字段                | 内容                                                                                                           | 类型    | 字节数 | 字节偏移 |
|------|---------------------|----------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |  RTKSTATUS 2 Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)         |         |   H    |   0      |
|    2 |    gpsSource        | GPS 系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的可用改正值时则对应 bit 位置为 1，按 16 进制显示； |    UINT |    4   |    H     |
| 3    | Reserved            | 保留位                                                                                                         | UINT    | 4      | H+4      |
|    4 |    bdsSource1       | 北斗系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的可用改正值时则对应 bit 位置为 1，按 16 进制显示； |    UINT |    4   |    H+8   |

| 序号  | 字段          | 内容                                                                                                              | 类型    | 字节数 | 字节偏移 |
|-------|---------------|-------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|    5  |    bdsSource2 | 北斗系统 33 到 63 号卫星显示， 源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+12  |
| 6     | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+16     |
|    7  |    gloSource  | GLO 系统 1 到 23 号卫星显示， 源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示；     |    UINT |    4   |    H+20  |
| 8     | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+24     |
|    9  |    galSource1 | Gal 系统 1 到 32 号卫星显示，源 数据解析状态，收到 1 颗卫星的可用改正值时则对应 bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+28  |
|    10 |    galSource2 | Gal 系统 33 到 36 号卫星显示， 源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示；    |    UINT |    4   |    H+32  |
|    11 |    QzssSource | QZSS 系统 193 到 202 号卫星显 示，源数据解析状态，收到 1 颗卫星的可用改正值时则对应bit 位置为 1，按 16 进制显示； |    UINT |    4   |    H+36  |
| 12    | Reserved      | 保留位                                                                                                            | UINT    | 4      | H+40     |
| 13    | Pos type      | 位置类型，（参考[表 0- 4 位置或](#_bookmark434) [速度类型](#_bookmark434)）                                       | Enum    | 4      | H+44     |

| 序号     | 字段                  | 内容                                                                                                                                                             | 类型       | 字节数  | 字节偏移   |
|----------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|---------|------------|
|       14 |      Calculate status | 0：无差分源数据输入 1：差分源可用观测值不足 2：差分源延迟较大 3：电离层活跃（基准站模式有效） 4：ROVER 端观测值不足 5：满足 RTK 解算 说明 RTK/RTD 模块解算的状态 |       Enum |       4 |       H+48 |
|    15    |    Ion detected       | 电离层闪烁对 RTK 定位结果的影响 0：对 RTK 解没有影响 1\~255：对 RTK 解存在负面影响                                                                               |    uchar   |    1    |    H+52    |
|     16   |     Dual rtk flag\*   | 0xFF：未配置双天线基线长度 0：未解算出基线长（双天线未全部进入固定解） 1：未超标 2：超标 仅适用于双天线产品                                                      |     Uchar  |     1   |     H+53   |
| 17       | ADR Number            | 从天线载波有效观测值总个数                                                                                                                                       | Uchar      | 1       | H+54       |
| 18       | Reserved              | 保留位                                                                                                                                                           | Uchar      | 1       | H+55       |
| 19       | Xxxx                  | 32 位 CRC 校验                                                                                                                                                   | Hex        | 4       | H+56       |
| 20       | [CR][LF]              | 结束符                                                                                                                                                           |            |         |            |

#### AGNSSSTATUS 辅助定位状态信息

用于查询接收机辅助定位的相关状态信息。

Message ID: 512

ASCII 输出语法:

AGNSSSTATUSA 1

Binary 输出语法:

AGNSSSTATUSB 1

适用产品：UM982、UMD982、UM980、UMD980、UB9A0、UBD9A0

消息输出：

\#AGNSSSTATUSA,77,GPS,FINE,2216,457483000,0,0,18,9;0000004EF7FFFFFF,0C00 3FFFBFFCBFFF,0000000000DF7FFF,0000000B67945FDF,0,F,01,07,2022,0,070418.26,18,

0,0,4004.73963848,11614.19678280,57.9901\*67b51741

表 7-124 AGNSSSTATUS 数据结构

| 序号         | 字段                | 内容                                                                                                                                                                                  | 类型         | 字节数 | 字节偏移 |
|--------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------|----------|
|   1          |  AGNSSSTATUS Header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211)                                                                                 |              |   H    |   0      |
|     2,3,4 ,5 |      Source         | GPS：64 位，1 位代表 1 颗星； BDS：64 位，1 位代表1 颗星； GLO：64 位，1 位代表1 颗星； GAL：64 位，1 位代表 1 颗星；源数据解析状态，收到1 颗星可用的改正值则对应位置为1，16 进制显示 |      UINT[2] |      8 |      H   |
| 6            | Reserved            | 保留                                                                                                                                                                                  | UINT         | 4      | H+32     |
|    7         |    Calculate status | Bit0：辅助源数据输入，0 为无辅助源数据输入，1 为有辅助源数据输入 Bit1：可用卫星不足，0 为不 足，1 为足够，下发星历可能存                                                              |    UINT      |    4   |    H+36  |

| 序号 | 字段           | 内容                                                                                                                   | 类型    | 字节数 | 字节偏移 |
|------|----------------|------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|      |                | 在与观测值不匹配的情况； Bit2：辅助源时间无效，0 为无效，1 为有效； Bit3： 辅助源传输的位置无 效，0 为无效，1 为有效； |         |        |          |
|  8   |  Aid day       | 收到的 UTC 日，两位数，取值 范围 01\~31                                                                                |  UINT   |  4     |  H+40    |
|  9   |  Aid mon       | 收到的 UTC 月，两位数，取值 范围 01\~12                                                                                |  UINT   |  4     |  H+44    |
| 10   | Aid year       | 收到的 UTC 年，四位数                                                                                                  | UINT    | 4      | H+48     |
| 11   | Reserved       | 保留位                                                                                                                 | UINT    | 4      | H+52     |
|  12  |  Aid Time      | 收到的辅助时间，时分秒，  hhmmss.sss                                                                                   |  Double |  8     |  H+56    |
| 13   | Aid LeapSecond | 收到的闰秒参数                                                                                                         | UShort  | 2      | H+64     |
| 14   | Reserved       | 保留                                                                                                                   | UShort  | 2      | H+66     |
| 15   | Reserved       | 保留                                                                                                                   | UINT    | 4      | H+68     |
|  16  |  Aid Lat       | 收 到 的 辅 助 坐 标 ， 纬 度 ， ddmm.mmmmmmmm                                                                         |  Double |  8     |  H+72    |
|  17  |  Aid Lon       | 收 到 的 辅 助 坐 标 ， 经 度 ， dddmm.mmmmmmmm                                                                        |  Double |  8     |  H+80    |
|  18  |  Aid Height    | 收到的辅助坐标，小数点后 4 位，单位 m                                                                                  |  Double |  8     |  H+88    |
| 19   | xxxx           | 32 位 CRC 校验                                                                                                         | Hex     | 4      | H+96     |
| 20   | [CR][LF]       | 结束符                                                                                                                 |         |        |          |

#### RTCSTATUS RTC 初始化状态查询

用于查询接收机的 RTC 寄存器初始化状态的相关信息。该消息语句仅能按照 1Hz 输

出。

Message ID: 510 ASCII 输出语法:

RTCSTATUSA 1

Binary 输出语法:

RTCSTATUSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#RTCSTATUSA,97,GPS,FINE,2190,365386000,0,0,18,14;1,0,0,0,2190,365386,1495,0,

0\*ac0f615a

表 7-125 RTCSTATUS 数据结构

| 序号 | 字段              | 内容                                                                                                   | 类型     | 字节数 | 字节偏移 |
|------|-------------------|--------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1  |  RTCSTATUS Header | 消息头，二进制消息头结构请 参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |          |   H    |   0      |
|   2  |   Type            | 0：无效 1：有效 显示 RTC 计数器状态                                                                    |   Uchar  |   1    |   H      |
| 3\~5 | Reserved\*3       | 保留                                                                                                   | Uchar\*3 | 3      | H+1      |
|  6   |  Week             | 周计数，当数据无效时，该值 为-1；                                                                      |  INT     |  4     |  H+4     |
| 7    | Second            | 周内秒                                                                                                 | UINT     | 4      | H+8      |
| 8    | Subsecond         | 秒以内计数（us）                                                                                       | UINT     | 4      | H+12     |
| 9    | Reserved          | 保留位                                                                                                 | UINT     | 4      | H+16     |
| 10   | Reserved          | 保留位                                                                                                 | UINT     | 4      | H+20     |

| 序号 | 字段     | 内容   | 类型 | 字节数 | 字节偏移 |
|------|----------|--------|------|--------|----------|
| 11   | Xxxx     | 校验位 | Hex  | 4      | H+24     |
| 12   | [CR][LF] | 结束符 |      |        |          |

#### JAMSTATUS 干扰检测

用于查询接收机干扰检测信息，只支持 1Hz 消息输出。

Message ID: 511 ASCII 输出语法:

JAMSTATUSA 1

Binary 输出语法:

JAMSTATUSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960、UM960L

消息输出：

\#JAMSTATUSA,97,GPS,FINE,2190,365412000,0,0,18,14;SINGLE,0,0,0,0\*e31418ea

表 7-126 JAMSTATUS 数据结构

| 序号 | 字段              | 内容                                                                                                    | 类型    | 字节数 | 字节偏移 |
|------|-------------------|---------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1  |  JAMSTATUS Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210) ， ASCII 消息头结构请参考[表7-51](#_bookmark211) |         |   H    |   0      |
| 2    | Pos type          | 位置类型（参考[表 0- 4 位](#_bookmark434) [置或速度类型](#_bookmark434)）                               | Enum    | 4      | H        |
|   3  |   CWRatio         | 取值范围：0\~255 标识干扰信号的强度，越高对定位影响越大；                                               |   Uchar |   1    |   H+4    |
| 4    | CWFlag            | 0：NO CW JAM                                                                                            | Uchar   | 1      | H+5      |

| 序号 | 字段     | 内容                       | 类型     | 字节数 | 字节偏移 |
|------|----------|----------------------------|----------|--------|----------|
|      |          | 1：CW JAM 2：Strong CW JAM |          |        |          |
| 5，6 | Reserved | 保留位                     | Uchar\*2 | 2      | H+6      |
| 7    | Xxxx     | 校验位                     | Hex      | 4      | H+8      |
| 8    | [CR][LF] | 结束符                     |          |        |          |

#### FREQJAMSTATUS 各频段干扰检测信息

用于查询接收机 L1/L2/L5 各频段的干扰检测结果信息，只支持 1Hz 消息输出。

Message ID: 519 ASCII 输出语法:

FREQJAMSTATUSA 1

Binary 输出语法:

FREQJAMSTATUSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM960、UMD960、UM982、 UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\#FREQJAMSTATUSA,97,GPS,FINE,2164,559464000,0,0,18,8;SINGLE,255,2,0,0,0,0,0,

0\*b0cdc7de

表 7-127 FREQJAMSTATUS 数据结构

| 序号 | 字段                  | 内容                                                                                                  | 类型 | 字节数 | 字节偏移 |
|------|-----------------------|-------------------------------------------------------------------------------------------------------|------|--------|----------|
|   1  |  FREQJAMSTATUS Header | 消息头，二进制消息头结 构请参考[表 7-50](#_bookmark210)，ASCII消息头结构请参考[表7-51](#_bookmark211) |      |   H    |   0      |

| 序号  | 字段        | 内容                                                                      | 类型     | 字节数 | 字节偏移 |
|-------|-------------|---------------------------------------------------------------------------|----------|--------|----------|
| 2     | Pos type    | 位置类型（参考[表 0- 4 位](#_bookmark434) [置或速度类型](#_bookmark434)） | Enum     | 4      | H        |
|   3   |   L1CWRatio | 取值范围：0\~255 标识干扰信号的强度，越高对定位影响越大                   |   UCHAR  |   1    |   H+4    |
|   4   |   L1CWFlag  | 0：NO CW JAM 1：CW JAM 2：Strong CW JAM                                   |   UCHAR  |   1    |   H+5    |
|   5   |   L2CWRatio | 取值范围：0\~255 标识干扰信号的强度，越高对定位影响越大                   |   UCHAR  |   1    |   H+6    |
|   6   |   L2CWFlag  | 0：NO CW JAM 1：CW JAM 2：Strong CW JAM                                   |   UCHAR  |   1    |   H+7    |
|   7   |   L5CWRatio | 取值范围：0\~255 标识干扰信号的强度，越高对定位影响越大                   |   UCHAR  |   1    |   H+8    |
|   8   |   L5CWFlag  | 0：NO CW JAM 1：CW JAM 2：Strong CW JAM                                   |   UCHAR  |   1    |   H+9    |
| 9，10 | Reserved    | 保留位                                                                    | Uchar\*2 | 2      | H+10     |
| 11    | Xxxx        | 校验位                                                                    | Hex      | 4      | H+12     |
| 12    | [CR][LF]    | 结束符                                                                    |          |        |          |

#### RTCMSTATUS 接收机接收到的 RTCM 数据包监测信息

用于查询接收机接收到的 RTCM 数据包，只支持 ONCHANGED 消息输出。

Message ID：2125

ASCII 输出语法：

RTCMSTATUSA ONCHANGED

Binary 输出语法：

RTCMSTATUSB ONCHANGED

适用产品：UM960L、UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、 UM960、UMD960

消息输出：

\#RTCMSTATUSA,76,GPS,FINE,2219,392572000,0,0,18,187;1124,21186,0,21,0,6,11,0

,0,21\*601a7581

表 7-128 RTCMSTATUS 数据结构

| 序号 | 字段               | 内容                                                                                                   | 类型   | 字节数 | 字节偏移 |
|------|--------------------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1  |  RTCMSTATUS Header | 消息头，二进制消息头结构请参 考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |        |   H    |   0      |
|  2   |  Msg ID            | MSM1\~MSM7 ID 信息 （含 RTCM1006/RTCM1033）                                                            |  UINT  |  4     |  H       |
| 3    | Msg Num            | 接收到数据的条数统计                                                                                   | UINT   | 4      | H+4      |
| 4    | Base ID            | 基站 ID                                                                                                | UINT   | 4      | H+8      |
| 5    | Sats Num           | 当前 Msg 中的卫星数量                                                                                  | UINT   | 4      | H+12     |
|  6   |  L1 num            | L1 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348)                                 |  UCHAR |  1     |  H+16    |
|  7   |  L2 num            | L2 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348)                                 |  UCHAR |  1     |  H+17    |
|  8   |  L3 num            | L3 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348)                                 |  UCHAR |  1     |  H+18    |
|  9   |  L4 num            | L4 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348)                                 |  UCHAR |  1     |  H+19    |

| 序号 | 字段     | 内容                                                                   | 类型   | 字节数 | 字节偏移 |
|------|----------|------------------------------------------------------------------------|--------|--------|----------|
|  10  |  L5 num  | L5 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348) |  UCHAR |  1     |  H+20    |
|  11  |  L6 num  | L6 观测量数量，对应的信号见 [表7-129 L1\~L6 对应关系表](#_bookmark348) |  UCHAR |  1     |  H+21    |
| 12   | Xxxx     | 校验位                                                                 | Hex    | 4      | H+22     |
| 13   | [CR][LF] | 结束符                                                                 |        |        |          |

表 7-129 L1\~L6 对应关系表

| 卫星系统    | 信号 ID | 信号通道 |
|-------------|---------|----------|
|     GPS     | 1       | L1C/A    |
|             | 2       | L2P      |
|             | 3       | L2C      |
|             | 4       | L5       |
|             | 5       | L1C      |
|             | 6       | Reserved |
|     GLONASS | 1       | G1C/A    |
|             | 2       | G1P      |
|             | 3       | G2C/A    |
|             | 4       | G2P      |
|             | 5 \~ 6  | Reserved |
|     Galileo | 1       | E1       |
|             | 2       | E6       |
|             | 3       | E5B      |
|             | 4       | E5A+B    |
|             | 5       | E5A      |
|             | 6       | Reserved |
|  QZSS       | 1       | L1C/A    |
|             | 2       | LEX      |

| 卫星系统 | 信号 ID | 信号通道 |
|----------|---------|----------|
|          | 3       | L2C      |
|          | 4       | L5       |
|          | 5       | L1C      |
|          | 6       | Reserved |
|     BDS  | 1       | B1       |
|          | 2       | B3       |
|          | 3       | B2       |
|          | 4       | B2A      |
|          | 5       | B2B      |
|          | 6       | B1C      |

#### HWSTATUS 硬件状态信息

硬件状态信息，仅支持 1Hz 输出。

Message ID: 218 ASCII 输出语法:

HWSTATUSA 1

Binary 输出语法:

HWSTATUSB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#HWSTATUSA,97,GPS,FINE,2221,111183000,0,0,18,15;66807,0.920,1.020,0.908,1,- 0.693,0.0,0x00,0,0x0377,0,0\*9d7ce51d

表 7-130 HWSTATUS 数据结构

| 序号 | 字段             | 内容                                                                                                   | 类型   | 字节数 | 偏移   |
|------|------------------|--------------------------------------------------------------------------------------------------------|--------|--------|--------|
|   1  |  HWSTATUS Header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |        |  H     |  0     |
| 2    | Reserved         | 保留位                                                                                                 | Int    | 4      | H      |
|  3   |  DC09            | DC09 量 测 电 压 正 常 范 围 值 0.85\~1.0V；小数点后三位有效。                                         |  Float |  4     |  H+4   |
|  4   |  DC10            | DC10 量 测 电 压 正 常 范 围 值 0.95\~1.1V；小数点后三位有效。                                         |  Float |  4     |  H+8   |
|  5   |  DC18            | DC18 量 测 电 压 正 常 范 围 值 1.7\~1.9V；小数点后三位有效。                                          |  Float |  4     |  H+12  |
|   6  |   Clockflag      | ClockDrift 有效标志位 0 = Invalid 1 = valid                                                            |   UINT |   4    |   H+16 |
| 7    | ClockDrift       | 晶振漂移的等效速度，单位 m/s                                                                           | Float  | 4      | H+20   |
| 8    | Reserved         | 保留位                                                                                                 | Float  | 4      | H+24   |
|  9   |  hwFlag          | 用于标识硬件相关信息，bit 说明 参见下表                                                                |  UCHAR |  1     |  H+28  |
| 10   | Reserved         | 保留                                                                                                   | UCHAR  | 1      | H+29   |
| 11   | PLL_LOCK         | PLL 状态                                                                                               | USHORT | 2      | H+30   |
| 12   | Reserved         | 保留                                                                                                   | UINT   | 4      | H+32   |
| 13   | Reserved         | 保留                                                                                                   | UINT   | 4      | H+36   |
| 14   | Xxxx             | 校验位                                                                                                 | Hex    | 4      | H+40   |
| 15   | [CR][LF]         | 结束符                                                                                                 |        |        |        |

表 7-131 HWFLAG 字段比特位说明表

| 比特位 | 定义                                  |
|--------|---------------------------------------|
| Bit0   | 0=有源晶振 1=无源晶振                 |
| Bit1   | 0=VCXO 压控 1=TCXO 非压控             |
| Bit2   | 0=26MHz 晶振 1=20MHz 晶振             |
| Bit3   | 0=仅支持有源晶振 1=支持有源和无源晶振 |
| Bit4   | 0=内钟；1=外钟                        |
| Bit5   |                                       |
| Bit6   |                                       |
| Bit7   | Check status 0=未知 1=有效            |

#### AGC AGC 状态

AGC 自动增益状态信息，当天线链路异常出现开路的情况时，AGC 自动增益调节将会变大，当出现信号干扰导致噪底被抬高时，AGC 自动增益调节将会变低。AGC 自动增益的结果一般遵循此规律，但是由于模组的硬件间的差异性，AGC 自动增益的数值模组间显示会存在一定的差异性。

Message ID: 220

ASCII 输出语法:

AGCA 1

Binary 输出语法:

AGCB 1

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982、UM960、 UMD960

消息输出：

\#AGCA,65,GPS,FINE,2190,375570000,0,0,18,37;44,46,63,-1,-1,41,1,0,-1,-1\*634f1e4b

表 7-132 AGC 数据结构

| ID  | 字段        | 数据描述                                                                                                               | 类型    | 字节数 | 字节偏移 |
|-----|-------------|------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  AGC header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |         |   H    |   0      |
|   2 |   ANT1L1    | 主天线 L1 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H      |
|   3 |   ANT1L2    | 主天线 L2 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H+2    |
|   4 |   ANT1L5    | 主天线 L5 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H+4    |
| 5   | Reserved    | 保留位                                                                                                                 | Short   | 2      | H+6      |
| 6   | Reserved    | 保留位                                                                                                                 | Short   | 2      | H+8      |
|   7 |   ANT2L1    | 从天线 L1 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H+10   |
|   8 |   ANT2L2    | 从天线 L2 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H+12   |
|   9 |   ANT2L5    | 从天线 L5 数值 AGC 寄存器的范围为 0\~255；若为- 1，则表示此通道无效。                                                  |   Short |   2    |   H+14   |
| 10  | Reserved    | 保留位                                                                                                                 | Short   | 2      | H+16     |
| 11  | Reserved    | 保留位                                                                                                                 | Short   | 2      | H+18     |
| 12  | xxxx        | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                                      | Hex     | 4      | H+20     |

| ID | 字段     | 数据描述             | 类型 | 字节数 | 字节偏移 |
|----|----------|----------------------|------|--------|----------|
| 13 | [CR][LF] | 语句结束符(仅 ASCII) | -    | -      | -        |

#### KSXT 定位定向数据输出语句

本消息包含 GNSS 接收机的时间、位置、定位和定向相关数据，只支持 ASCII 输出。

ASCII 输出语法：

KSXT 1 当前串口输出 1Hz 的 KSXT 信息 KSXT COM2 1 在 COM2 口输出 1Hz 的 KSXT 信息

适用产品：UM960、UMD960、UM980、UMD980、UB9A0、UBD9A0、UM982、 UMD982

消息输出：

\$KSXT,20190909084745.00,116.23662400,40.07897925,68.3830,299.22,- 67.03,190.28,0.022,,1,3,46,28,,,,-0.004,-0.021,-0.020,,\*27

表 7-133 KSXT 数据结构

| ID | 字段       | 数据描述                                                                | 符号              |
|----|------------|-------------------------------------------------------------------------|-------------------|
|  1 |  \$KSXT    | 消息头，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |                   |
| 2  | Utc        | UTC 时间                                                                | yyyymmddhhmmss.ss |
|  3 |  Lon       | 经度（单位，度），保留小数点后 8 位 有效数字                            |  DDD.DDDDDDDD     |
|  4 |  Lat       | 纬度（单位，度），保留小数点后 8 位 有效数字                            |  DD.DDDDDDDD      |
|  5 |  Height    | 海拔高（单位，米），保留小数点后 4 位有效数字                           |  xxxxx.xxxx       |
| 6  | Heading    | 方位角，保留小数点后 2 位有效数字                                       | xxx.xx            |
| 7  | Pitch      | 俯仰角，保留小数点后 2 位有效数字                                       | xxx.xx            |
| 8  | Track true | 速度角，保留小数点后 2 位有效数字                                       | xxx.xx            |

| ID    | 字段            | 数据描述                                                                         | 符号      |
|-------|-----------------|----------------------------------------------------------------------------------|-----------|
|  9    |  Vel            | 水平速度，单位 km/h，保留小数点后 3 位有效数字                                   |  xxx.xxx  |
| 10    | Roll            | 横滚角，保留小数点后 2 位有效数字                                                | xxx.xx    |
|    11 |    Pos qual     | 定位质量标识符： 0 = 定位不可用或无效 1 = 单点定位 2 = RTK 浮点解 3 = RTK 固定解 |    X      |
|    12 |    Heading qual | 定向质量标识符： 0 = 定位不可用或无效 1 = 单点定位 2 = RTK 浮点解 3 = RTK 固定解 |    X      |
| 13    | \#hsolnSVs      | 从天线当前参与解算的卫星数量                                                     | xx        |
| 14    | \#msolnSVs      | 主天线当前参与解算的卫星数量                                                     | xx        |
|   15  |   East          | 东向位置坐标：以基准站为原点的地理坐标系下的东向位置，单位：米，小数 点后 3 位   |   xxx.xxx |
|   16  |   North         | 北向位置坐标：以基准站为原点的地理坐标系下的北向位置，单位：米，小数 点后 3 位   |   xxx.xxx |
|   17  |   Up            | 天向位置坐标：以基准站为原点的地理坐标系下的天向位置，单位：米，小数 点后 3 位   |   xxx.xxx |
|  18   |  EastVel        | 东向速度：地理坐标系下的东向速度， 小数点后 3 位，单位：Km/h(如无为空)           |  xxx.xxx  |

| ID   | 字段      | 数据描述                                                                 | 符号      |
|------|-----------|--------------------------------------------------------------------------|-----------|
|  19  |  northVel | 北向速度：地理坐标系下的北向速度， 小数点后 3 位，单位：Km/h(如无为空)   |  xxx.xxx  |
|   20 |   upVel   | 天向速度：地理坐标系下的天顶向速度，小数点后 3 位，单位：Km/h(如无 为空) |   xxx.xxx |
| 21   | Reserved  | 保留                                                                     |           |
| 22   | Reserved  | 保留                                                                     |           |
|  23  |  \*xx     | 异或校验，\$ 到\* 之间（不包括\$ 和\*） 的数异或后的值，十六进制         |  \*FF     |
| 24   | [CR][LF]  | 语句结束符                                                               | [CR][LF]  |

#### INFOPART1

针对产品固定存储区域 PART1 部分的信息读取。

Message ID：1019 ASCII 输出语法：

INFOPART1A

Binary 输出语法：

INFOPART1B

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#INFOPART1A,69,GPS,FINE,2190,376054000,0,0,18,953;0\*723399e1

表 7-134 INFOPART1 数据结构

| ID  | 字段              | 数据描述                                                                                              | 类型 | 字节数 | 字节偏移 |
|-----|-------------------|-------------------------------------------------------------------------------------------------------|------|--------|----------|
|   1 |  INFOPART1 header | 消息头，二进制消息头结构请参 考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |      |   H    |   0      |

| ID  | 字段              | 数据描述                                                      | 类型         | 字节数 | 字节偏移 |
|-----|-------------------|---------------------------------------------------------------|--------------|--------|----------|
| 2   | Count             | 消息条数                                                      | Uchar        | 1      | H        |
| 3   | Info id           | 0\~7                                                          | Uchar        | 1      | H+1      |
| 4   | Length            | 数据段长度                                                    | Ushort       | 2      | H+2      |
|   5 |   Data            | 信息段内容，最大 128 字节，小 于 128 字节时按实际数据长度输出 |   Uchar[128] |   128  |   H+4    |
| 6   | 循环 Count 次输出 |                                                               |              |        |          |
|  7  |  xxxx             | 32 位 CRC 校验(仅 ASCII 和二进 制)                            |  Hex         |  4     |  H+X     |
| 8   | [CR][LF]          | 语句结束符(仅 ASCII)                                          | -            | -      | -        |

#### INFOPART2

针对产品固定存储区域 PART2 部分的信息读取。

Message ID：1020 ASCII 输出语法：

INFOPART2A

Binary 输出语法：

INFOPART2B

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#INFOPART2A,67,GPS,FINE,2190,376094000,0,0,18,753;0\*c5702fa1

表 7-135 INFOPART2 数据结构

| ID  | 字段              | 数据描述                                                                                              | 类型        | 字节数 | 字节偏移 |
|-----|-------------------|-------------------------------------------------------------------------------------------------------|-------------|--------|----------|
|   1 |  INFOPART2 header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211) |             |   H    |   0      |
| 2   | Count             | 消息条数                                                                                              | Uchar       | 1      | H        |
| 3   | Info id           | 0\~23                                                                                                 | Uchar       | 1      | H+1      |
| 4   | Length            | 数据段长度                                                                                            | Ushort      | 2      | H+2      |
|  5  |  Data             | 信息段内容，最大 128 字节，小于 128 字节时按实际数据长度输出                                          |  Uchar[128] |  128   |  H+4     |
| 6   | 循环 Count 次输出 |                                                                                                       |             |        |          |
| 7   | xxxx              | 32 位 CRC 校验(仅 ASCII 和二进制)                                                                     | Hex         | 4      | H+X      |
| 8   | [CR][LF]          | 语句结束符(仅 ASCII)                                                                                  | -           | -      | -        |

#### MSPOS 双天线的最佳位置

本指令包含接收机主从天线计算的位置信息。

Message ID: 520 ASCII 输出语法:

MSPOSA 1

BINARY 输出语法:

MSPOSB 1

适用产品：UM982、UMD982

-   UM982 Build9669 及之后的版本支持

消息输出：

\#MSPOSA,86,GPS,FINE,2247,471141000,0,0,18,25;SOL_COMPUTED,SINGLE,40.078 96381103,116.23651058490,64.4448,1.3441,1.2328,2.9707,46,28,,SOL_COMPUTED,SIN

GLE,40.07896511614,116.23651086865,64.5809,1.3723,1.1967,2.9210,45,28,,"0",0.000\*

a71a580e

表 7-136 MSPOS 数据结构

| ID  | 字段                | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|---------------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |   MSPOS header      | 消息头，二进制消息头结构请 参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |        |   H    |   0      |
|  2  | Master_p-sol status | 主天线位置的解状态，参考[表](#_bookmark435) [0- 5 解的状态](#_bookmark435)                            |  Enum  |  4     |  H       |
|  3  |  Master_pos type    | 主天线的位置类型（参考[表0- 4](#_bookmark434) [位置或速度类型](#_bookmark434)）                       |  Enum  |  4     |  H+4     |
| 4   | Master_lat          | 主天线的纬度，deg                                                                                     | Double | 8      | H+8      |
| 5   | Master_lon          | 主天线的经度，deg                                                                                     | Double | 8      | H+16     |
| 6   | Master_Hgt          | 主天线的海拔高，m                                                                                     | Double | 8      | H+24     |
| 7   | Master_lat σ        | 主天线的纬度标准差，m                                                                                 | Float  | 4      | H+32     |
| 8   | Master_lon σ        | 主天线的经度标准差，m                                                                                 | Float  | 4      | H+36     |
| 9   | Master_hgt σ        | 主天线的高度标准差，m                                                                                 | Float  | 4      | H+40     |
| 10  | MasterObs           | 主天线跟踪观测到的卫星总数                                                                            | UCHAR  | 1      | H+44     |
| 11  | MasterSatUse        | 主天线参与解算的卫星总数                                                                              | UCHAR  | 1      | H+45     |
| 12  | Reserved            | 保留位                                                                                                | Short  | 2      | H+46     |
|  13 | Slave_p-sol status  | 从天线的解状态，参考[表 0- 5](#_bookmark435) [解的状态](#_bookmark435)                                |  Enum  |  4     |  H+48    |
|  14 |  Slave_pos type     | 从天线的位置类型（参考[表0- 4](#_bookmark434) [位置或速度类型](#_bookmark434)）                       |  Enum  |  4     |  H+52    |
| 15  | Slave_lat           | 从天线的纬度，deg                                                                                     | Double | 8      | H+56     |

| ID  | 字段        | 数据描述                           | 类型    | 字节数 | 字节偏移 |
|-----|-------------|------------------------------------|---------|--------|----------|
| 16  | Slave_lon   | 从天线的经度，deg                  | Double  | 8      | H+64     |
| 17  | Slave_Hgt   | 从天线的海拔高，m                  | Double  | 8      | H+72     |
| 18  | Slave_lat σ | 从天线的纬度标准差，m              | Float   | 4      | H+80     |
| 19  | Slave_lon σ | 从天线的经度标准差，m              | Float   | 4      | H+84     |
| 20  | Slave_hgt σ | 从天线的高度标准差，m              | Float   | 4      | H+88     |
| 21  | SlaveObs    | 从天线跟踪观测到的卫星总数         | UCHAR   | 1      | H+92     |
| 22  | SlaveSatUse | 从天线参与解算的卫星总数           | UCHAR   | 1      | H+93     |
| 23  | Reserved    | 保留位                             | Short   | 2      | H+94     |
| 24  | stn id      | 基站 ID，缺省值为 0                | Char[4] | 4      | H+96     |
| 25  | age         | 差分龄期，s                        | Float   | 4      | H+100    |
|  26 |  xxxx       | 32 位 CRC 校验(仅 ASCII 和二 进制) |  Hex    |  4     |  H+104   |
| 27  | [CR][LF]    | 语句结束符(仅 ASCII)               | -       | -      | -        |

#### TROPINFO 对流层天顶延迟信息输出

TROPINFO 用于输出对流层天顶延迟信息。该消息仅支持按 ONCE 或ONCHANGED 模式输出；另外，该消息仅在 PPP 使能时可输出。

Message ID：2318

ASCII 输出语法：

TROPINFOA ONCHANGED

Binary 输出语法：

TROPINFOB ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#TROPINFOA,85,GPS,FINE,2244,93693000,0,0,18,63;SAASTAMOINEN,2.354103,2.2 92246,0.061857,0.026856,0.000000\*89ed6541

表 7-137 TROPINFO 数据结构

| ID  | 字段             | 数据描述                                                                                               | 类型  | 字节数 | 字节偏移 |
|-----|------------------|--------------------------------------------------------------------------------------------------------|-------|--------|----------|
|   1 |  TROPINFO header | 消息头，二进制消息头结构请参考 [表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |       |   H    |   0      |
|   2 |   Trop module    | 使用的参考对流层模型，ASCII 下默认输出“ SAASTAMOINEN ”， 二进制下输出为 1                              |   INT |   4    |   H      |
| 3   | TropZenith       | 天顶总延迟                                                                                             | Float | 4      | H+4      |
| 4   | Dry              | 天顶干延迟                                                                                             | Float | 4      | H+8      |
| 5   | Wet              | 天顶🗎延迟                                                                                              | Float | 4      | H+12     |
| 6   | Std              | 天顶总延迟标准差                                                                                       | Float | 4      | H+16     |
| 7   | Reserved         | 保留位                                                                                                 | Float | 4      | H+20     |
| 8   | Xxxx             | 32 位CRC 校验                                                                                          | HEX   | 4      | H+24     |
| 9   | [CR][LF]         | 语句结束符(仅 ASCII)                                                                                   |       |        |          |

#### PPPB2BINFO1 信息类型 1

本指令包含 PPP-B2b 信息类型 1，包含卫星掩码信息，详细可参考 PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2302

ASCII 输出语法：

PPPB2BINFO1A ONCHANGED

Binary 输出语法：

PPPB2BINFO1B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO1A,80,GPS,FINE,2203,366209000,0,0,18,1;219,1,2,20590,00003FFDF FFC0001FFFFFFFE0000000000000000000000000000000000000000\*f7e11cb5

表 7-138 PPPB2BINFO1 数据结构

| ID  | 字段                | 数据描述                                                                                               | 类型      | 字节数 | 字节偏移 |
|-----|---------------------|--------------------------------------------------------------------------------------------------------|-----------|--------|----------|
|   1 |  PPPB2BINFO1 header | 消息头，二进制消息头结构请 参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |           |   H    |   0      |
| 2   | Prn                 | PRN (161 based)                                                                                        | Short     | 2      | H        |
| 3   | Iodssr              | 状态空间描述数据的版本号                                                                               | Uchar     | 1      | H+2      |
| 4   | Iodp                | 卫星掩码的数据版本号                                                                                   | Uchar     | 1      | H+3      |
| 5   | Sow                 | 历元时刻，天内秒                                                                                       | UINT      | 4      | H+4      |
| 6   | Mask                | PRN bit mask                                                                                           | Uchar[32] | 32     | H+8      |
| 7   | Xxxx                | 32 位CRC 校验                                                                                          | HEX       | 4      | H+40     |
| 8   | [CR][LF]            | 语句结束符(仅 ASCII)                                                                                   |           |        |          |

#### PPPB2BINFO2 信息类型 2

本指令包含 PPP-B2b 信息类型 2，包含卫星轨道改正数及用户测距精度指数，详细可参考 PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2304

ASCII 输出语法：

PPPB2BINFO2A ONCHANGED

Binary 输出语法：

PPPB2BINFO2B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO2A,86,GPS,FINE,2203,366269000,0,0,18,1;219,1,0,20631,72,86,- 84,25,-24,0,27,84,50,39,71,18,4,27,90,57,-3,129,-1,0,27,93,86,-

182,90,163,4,27,0,0,0,0,0,0,00,0,0,0,0,0,0,00\*16d92a8c

表 7-139 PPPB2BINFO2 数据结构

| ID  | 字段                | 数据描述                                                                                               | 类型           | 字节数 | 字节偏移 |
|-----|---------------------|--------------------------------------------------------------------------------------------------------|----------------|--------|----------|
|   1 |  PPPB2BINFO2 header | 消息头，二进制消息头结构 请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |                |   H    |   0      |
| 2   | Prn                 | PRN (161 based)                                                                                        | Ushort         | 2      | H        |
| 3   | Iodssr              | 状态空间描述数据的版本号                                                                               | Uchar          | 1      | H+2      |
| 4   | Reserved            | 预留                                                                                                   | Uchar          | 1      | H+3      |
| 5   | SOW                 | 历元时刻，天内秒                                                                                       | UINT           | 4      | H+4      |
| 6   | OrbitCorr           | 轨道修正数                                                                                             | StOrbitCorr[6] | 72     | H+8      |
| 7   | XXXX                | 32 位CRC 校验                                                                                          | HEX            | 4      | H+80     |
| 8   | [CR][LF]            | 语句结束符(仅 ASCII)                                                                                   |                |        |          |

typedef struct

{

USHORT usPrn; //ICD中SatSlot，掩码位置号 USHORT usIodn; //基本导航电文版本号 SHORT sRadial; //径向改正数

SHORT sInTrack; //切向改正数 SHORT sCross; //法向改正数 UCHAR ucIODCorr;//改正数版本号

UCHAR ucURAI; //URAI本颗卫星的用户距离精度指数

}_PACKED\_ StOrbitCorr;

#### PPPB2BINFO3 信息类型 3

本指令包含PPP-B2b 信息类型 3，包含码间偏差改正数等信息，详细可参考 PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持ONCHANGED 请求方式。

Message ID：2306

ASCII 输出语法：

PPPB2BINFO3A ONCHANGED

Binary 输出语法：

PPPB2BINFO3B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO3A,78,GPS,FINE,2203,366263000,0,0,18,1;219,1,3,20631,40,8,0,15,1, 43,2,50,4,-305,5,-259,7,-227,8,-199,12,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,44,8,0,-35,1,-43,2,-37,

4,-255,5,-210,7,-212,8,-182,12,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,45,8,0,-490,1,-355,2,-350,4,-3

27,5,-284,7,-270,8,-243,12,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0\*943febbe

表 7-140 PPPB2BINFO3 数据结构

| ID  | 字段                 | 数据描述                                                                                               | 类型   | 字节数 | 字节偏移 |
|-----|----------------------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  PPPB2BINF O3 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | Prn                  | PRN (161 based)                                                                                        | Ushort | 2      | H        |
| 3   | Iodssr               | 状态空间描述数据的版本号                                                                               | Uchar  | 1      | H+2      |
| 4   | SatNum               | 卫星数量                                                                                               | Uchar  | 1      | H+3      |
| 5   | Sow                  | 历元时刻，天内秒                                                                                       | UINT   | 4      | H+4      |

| ID | 字段      | 数据描述             | 类型                   | 字节数      | 字节偏移        |
|----|-----------|----------------------|------------------------|-------------|-----------------|
|  6 |  CodeBias |  码间偏差            | StCodeBias \_t[SatNum] | 64\*SatN um |  H+8            |
|  7 |  xxxx     |  32 位CRC 校验       |  HEX                   |  4          | H+8+64\*S atNum |
| 8  | [CR][LF]  | 语句结束符(仅 ASCII) | -                      | -           | -               |

typedef struct

{

USHORT usMode; //码偏差对应的信号支路及处理模式 SHORT sCodeCorr; //码偏差值

}_PACKED\_ StCodeCorr_t;

typedef struct

{

USHORT usSatSlot; //卫星掩码位置

USHORT usBiasNum; //码间偏差数量 StCodeCorr_t stCodeCorr[15]; //码间偏差修正数

}_PACKED\_ StCodeBias_t;

#### PPPB2BINFO4 信息类型 4

本指令包含PPP-B2b 信息类型 4，包含卫星钟差改正数等信息，详细可参考 PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持ONCHANGED 请求方式。

Message ID：2308

ASCII 输出语法：

PPPB2BINFO4A ONCHANGED

Binary 输出语法：

PPPB2BINFO4B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO4A,85,GPS,FINE,2203,366294000,0,0,18,1;219,1,2,20674,0,0,0,0,0,-16 383,0,-16383,0,-16383,0,-16383,0,-16383,7,71,0,-16383,5,119,0,-16383,0,-16383,3,79,0,-

16383,0,-16383,0,-16383,0,-16383,1,-52,0,-16383,0,-16383,3,773,4,1225,3,775,0,-16383,

0,-16383\*3a7fd61c

表 7-141 PPPB2BINFO4 数据结构

| ID   | 字段                 | 数据描述                                                                                                 | 类型            | 字节数 | 字节偏移 |
|------|----------------------|----------------------------------------------------------------------------------------------------------|-----------------|--------|----------|
|    1 |   PPPB2BINFO4 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210) ， ASCII 消息头结构请参 考[表7-51](#_bookmark211) |                 |    H   |    0     |
| 2    | Prn                  | PRN (161 based)                                                                                          | Ushort          | 2      | H        |
|  3   |  Iodssr              | 状态空间描述数据的版 本号                                                                                |  Uchar          |  1     |  H+2     |
| 4    | Iodp                 | 卫星掩码的数据版本号                                                                                     | Uchar           | 1      | H+3      |
| 5    | Sow                  | 历元时刻，天内秒                                                                                         | UINT            | 4      | H+4      |
| 6    | SubType              | 子类型标识                                                                                               | Uchar           | 1      | H+8      |
| 7    | Reserved             | 预留                                                                                                     | Uchar[3]        | 3      | H+9      |
| 8    | ClkCorr              | 钟差修正数                                                                                               | StClkCorr_t[23] | 92     | H+12     |
| 9    | xxxx                 | 32 位CRC 校验                                                                                            | HEX             | 4      | H+104    |
| 10   | [CR][LF]             | 语句结束符(仅 ASCII)                                                                                     | -               | -      | -        |

typedef struct

{

USHORT usIodCorr; //改正数版本号

SHORT sC0; //钟差改正数

}_PACKED\_ StClkCorr_t;

#### PPPB2BINFO5 信息类型 5

本指令包含 PPP-B2b 信息类型 5，包含用户测距精度指数，详细可参考 PPP-B2b ICD文件。PPP 特定版本支持。命令输入仅支持ONCHANGED 请求方式。

Message ID：2310

ASCII 输出语法：

PPPB2BINFO5A ONCHANGED

Binary 输出语法：

PPPB2BINFO5B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO5A,85,GPS,FINE,2203,366294000,0,0,18,1;219,1,2,20674,0,0,0,0,0,-16 383,0,-16383,0,-16383,0,-16383,0,-16383,7,71,0,-16383,5,119,0,-16383,0,-16383,3,79,0,-

16383,0,-16383,0,-16383,0,-16383,1,-52,0,-16383,0,-16383,3,773,4,1225,3,775,0,-16383,

0,-16383,0,-16383,0,-16383,0,-16383,0,-16383,0,-16383,7,71,0,-16383,5,119,0,-16383,0,-

16383,3,79,0,-16383,0,-16383,0,-16383,0,-16383,1,-52,0,-16383,0,-16383,3,773,4,1225,3,

775,0,-16383,0,-16383,0,-16383,0,-16383,0,-16383,0,-16383,0,-16383,7,71,0,-16383,5,11

9,0,-16383,0,-16383,3,79,0,-16383,0,-16383,0,-16383,0,-16383,1,-52,0,-16383,0,-16383,

3,773,4,1225,3,775,0,-16383,0,-16383,0,-16383\*3a7fd61c

表 7-142 PPPB2BINFO5 数据结构

| ID  | 字段                | 数据描述                                                                                               | 类型         | 字节数 | 字节偏移 |
|-----|---------------------|--------------------------------------------------------------------------------------------------------|--------------|--------|----------|
|   1 |  PPPB2BINFO5 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |              |   H    |   0      |
| 2   | Prn                 | PRN (161 based)                                                                                        | Ushort       | 2      | H        |
| 3   | Iodssr              | 状态空间描述数据的版本号                                                                               | Uchar        | 1      | H+2      |
| 4   | IODP                | 掩码版本号                                                                                             | Uchar        | 1      | H+3      |
| 5   | Subtype             | 标识号                                                                                                 | Uchar        | 1      | H+4      |
| 6   | Reserved            | 保留位                                                                                                 | Uchar        | 1      | H+5      |
| 7   | Reserved            | 保留位                                                                                                 | Uchar        | 1      | H+6      |
| 8   | Reserved            | 保留位                                                                                                 | Uchar        | 1      | H+7      |
| 9   | SOW                 | 历元时刻，天内秒                                                                                       | UINT         | 4      | H+8      |
| 10  | URAI                | 用户距离精度指数                                                                                       | StURAI-t[70] | 140    | H+12     |
| 11  | XXXX                | 32 位CRC 校验                                                                                          | HEX          | 4      | H+152    |
| 12  | [CR][LF]            | 语句结束符(仅 ASCII)                                                                                   |              |        |          |

typedef struct

{

UCHAR ucCLASS;

UCHAR ucValue;

}_PACKED\_ StURAI_t;

#### PPPB2BINFO6 信息类型 6

本指令包含 PPP-B2b 信息类型 6，钟差改正数与轨道改正数组合信息，详细可参考 PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2312

ASCII 输出语法：

PPPB2BINFO6A ONCHANGED

Binary 输出语法：

PPPB2BINFO6B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO6A,85,GPS,FINE,2203,366294000,0,0,18,1;219,1,2,20674,1,2,0,0,- 16383,20674,1,0,0,0,219,1,2,3,4,5,6,220,1,2,3,4,5,6\*3a7fd61c

表 7-143 PPPB2BINFO6 数据结构

| ID  | 字段                | 数据描述                                                                                               | 类型   | 字节数 | 字节偏移 |
|-----|---------------------|--------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  PPPB2BINFO6 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | PRN                 | PRN (161 based)                                                                                        | Ushort | 2      | H        |
| 3   | NumC                | 钟差改正数卫星数量                                                                                     | Uchar  | 1      | H+2      |
| 4   | NumO                | 轨道改正数卫星数量                                                                                     | Uchar  | 1      | H+3      |
| 5   | RawNumc             | 钟差改正数                                                                                             | StNumC | 96     | H+4      |
| 6   | RawNumo             | 轨道改正数                                                                                             | StNumO | 80     | H+100    |
| 7   | XXXX                | 32 位CRC 校验                                                                                          | HEX    | 4      | H+180    |
| 8   | [CR][LF]            | 语句结束符(仅 ASCII)                                                                                   |        |        |          |

typedef struct

{

USHORT usIODCorr; SHORT sC0;

}_PACKED\_ StClkCorr6_t;

typedef struct

{

UINT uiSow; UCHAR ucIodssr; UCHAR ucIodp;

USHORT usSatStartIndex; StClkCorr6_t astClkCorr[22];

}_PACKED\_ StNumC_t;

typedef struct

{

USHORT usPrn; USHORT usIodn; SHORT sRadial; SHORT sInTrack; SHORT sCross; UCHAR ucIodCorr; UCHAR ucURAI;

}_PACKED\_ StOrbitCorr_t;

typedef struct

{

UINT uiSow; UCHAR ucIodssr;

UCHAR aucReserved[3]; StOrbitCorr_t astOrbitCorr[6];

}_PACKED\_ StNumO_t;

#### PPPB2BINFO7 信息类型 7

此条信息用于组合播发钟差改正数与轨道改正数信息，其与 PPPB2BINFO6 信息类型 6 的差异在于：关于卫星钟差改正数与卫星的对应关系，不通过掩码对应，而通过 Satslot

对应，详细请参考PPP-B2b ICD 文件。PPP 特定版本支持。命令输入仅支持ONCHANGED请求方式。

Message ID：2314

ASCII 输出语法：

PPPB2BINFO7A ONCHANGED

Binary 输出语法：

PPPB2BINFO7B ONCHANGED

适用产品：UM980、UMD980、UB9A0、UBD9A0、UM982、UMD982

消息输出：

\#PPPB2BINFO7A,85,GPS,FINE,2203,366294000,0,0,18,1;219,1,2,20674,1,2,0,0,219, 1,2,20674,1,0,0,0,219,1,2,3,4,5,6,220,1,2,3,4,5,6\*3a7fd61d

表 7-144 PPPB2BINFO7 数据结构

| ID  | 字段                | 数据描述                                                                                              | 类型   | 字节数 | 字节偏移 |
|-----|---------------------|-------------------------------------------------------------------------------------------------------|--------|--------|----------|
|   1 |  PPPB2BINFO6 header | 消息头，二进制消息头结 构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |        |   H    |   0      |
| 2   | PRN                 | PRN (161 based)                                                                                       | Ushort | 2      | H        |
| 3   | NumC                | 钟差改正数卫星数量                                                                                    | Uchar  | 1      | H+2      |
| 4   | NumO                | 轨道改正数卫星数量                                                                                    | Uchar  | 1      | H+3      |
| 5   | RawNumc             | 钟差改正数                                                                                            | StNumC | 128    | H+4      |
| 6   | RawNumo             | 轨道改正数                                                                                            | StNumO | 80     | H+132    |
| 7   | XXXX                | 32 位CRC 校验                                                                                         | HEX    | 4      | H+212    |
| 8   | [CR][LF]            | 语句结束符(仅 ASCII)                                                                                  |        |        |          |

typedef struct

{

INT iPrn;

USHORT usIODCorr; SHORT sC0;

}_PACKED\_ StClkCorr7_t;

typedef struct

{

UINT uiSow; UCHAR ucIodssr; UCHAR ucIodp;

UCHAR aucReserved[2]; StClkCorr7_t astRawClkCorr[15];

}_PACKED\_ StNumC7_t;

typedef struct

{

USHORT usPrn; USHORT usIodn; SHORT sRadial; SHORT sInTrack; SHORT sCross; UCHAR ucIodCorr; UCHAR ucURAI;

}_PACKED\_ StOrbitCorr7_t;

typedef struct

{

UINT uiSow; UCHAR ucIodssr;

UCHAR aucReserved[3]; StOrbitCorr7_t astRawOrbitCorr[6];

}_PACKED\_ StNumO7_t;

#### E6MASKBLOCK 掩码信息

该消息提供了当前模组解算出的 E6 HAS 服务提供的掩码信息， 该消息仅支持 ONCHANGED 输出。

Message ID: 2319

ASCII 输出语法:

E6MASKBLOCKA ONCHANGED

Binary 输出语法:

E6MASKBLOCKB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

消息输出：

\#E6MASKBLOCKA,62,GPS,FINE,2287,384303800,0,0,18,26;2700,50,19,25,0,2,0,0,7F FFFBDF00,8140,1,BFFFFFFFDFEFF6DFFFFFFE0000000000000000000000000000000000 000000000000000000000000,0,0,0,0,2,73FA29E6D0,4904,0,00000000000000000000000

000000000000000000000000000000000000000000000000000000000,0,0,0,0\*d0234a2

b

表 7-145 E6MASKBLOCK 数据结构

| ID   | 字段                | 数据描述                                                                                                    | 类型     | 字节数 | 字节偏移 |
|------|---------------------|-------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1  |  E6MASKBLOCK header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结 构请参考[表7-51](#_bookmark211)       |          |   H    |   0      |
|    2 |    TOH              | 消息接收时间（时内秒），与 GST 时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。 |    ULONG |    4   |    H     |

| ID                                | 字段              | 数据描述                                                                                                                                                                                 | 类型         | 字节数   | 字节偏移   |
|-----------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------|------------|
|        3                          |        Block Flag | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表 有，“0”代表无 |        UCHAR |        1 |        H+4 |
| 4                                 | Reserved          | 保留位                                                                                                                                                                                   | UCHAR        | 1        | H+5        |
| 5                                 | MASK ID           | 掩码 ID                                                                                                                                                                                  | UCHAR        | 1        | H+6        |
| 6                                 | IOD Set ID        | 数据期号系列 ID                                                                                                                                                                          | UCHAR        | 1        | H+7        |
| 7                                 | Nsys              | 具有改正数的 GNSS 数量                                                                                                                                                                   | USHORT       | 2        | H+8        |
| 8                                 | Reserved          | 保留位                                                                                                                                                                                   | USHORT       | 2        | H+10       |
| 如下循环 Nsys，当前 Nsys 固定为 2 |                   |                                                                                                                                                                                          |              |          |            |
|    9                              |    GNSS ID        | GNSS ID 0：GPS 1：保留 2：Galileo 3-15：保留                                                                                                                                             |    USHORT    |    2     |    H+12    |
|     10                            |     Sat Mask      | 卫星掩码，字段长度为 40 bit，用于标识已改正的卫星 （“1”）和未改正的卫星 （“0”）。详见[表7-146 卫星](#_bookmark380)[掩码](#_bookmark380)。最高有效位对应 Satellite Index = 0。            |     Hex      |     5    |     H+14   |

| ID       | 字段             | 数据描述                                                                                                                                                                                                          | 类型      | 字节数   | 字节偏移    |
|----------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|----------|-------------|
|      11  |      Signal Mask | 信号掩码，字段长度为 16 bit，用于标识具有码偏差改正数和相位偏差改正数的信号 （“1”）以及不具备以上改正数的信号（“0”）。详见[表](#_bookmark381) [7-147 信号掩码](#_bookmark381)。最高有效位对 应 Signal Index = 0。 |      Hex  |      2   |      H+19   |
|   12     |   CMAF           | 单元掩码标识，用于标记消息中是否包含单元掩码：“1”为 是；“0”为否。                                                                                                                                                 |   UCHAR   |   1      |   H+21      |
|       13 |       CM         | 单元掩码，一个二维表，其中行表示可用信号（信号掩码中显示为 1 的信号），列表示可 用卫星（卫星掩码中显示为 1的卫星）。 该字段用于标识可用卫星及可 用信号的偏差改正数情况： “1”表示有；“0”表示无。                   |       Hex |       40 |       H+22  |
|  14      |  NM              | 导航电文索引，见[表7-148 导](#_bookmark382) [航电文索引](#_bookmark382)                                                                                                                                           |  UCHAR    |  1       |  H+62       |
| 15       | Reserved         | 保留位                                                                                                                                                                                                            | UCHAR[3]  | 3        | H+63        |
|  16      |  xxxx            | 32 位 CRC 校验（仅 ASCII 和二 进制）                                                                                                                                                                              |  Hex      |  4       |  H+12+2\*54 |
| 17       | [CR][LF]         | 语句结束符（仅 ASCII）                                                                                                                                                                                            | -         | -        | -           |

表 7-146 卫星掩码

| Satellite Index | Galileo SVID | GPS PRN |
|-----------------|--------------|---------|
| 0               | 1            | 1       |

| Satellite Index | Galileo SVID | GPS PRN |
|-----------------|--------------|---------|
| 1               | 2            | 2       |
| …               | …            | …       |
| 39              | 40           | 40      |

表 7-147 信号掩码

| Signal Index | Galileo        | GPS         |
|--------------|----------------|-------------|
| 0            | E1-B I/NAV OS  | L1 C/A      |
| 1            | E1-C           | Reserved    |
| 2            | E1-B + E1-C    | Reserved    |
| 3            | E5a-I F/NAV OS | L1C(D)      |
| 4            | E5a-Q          | L1C(P)      |
| 5            | E5a-I+E5a-Q    | L1C(D+P)    |
| 6            | E5b-I I/NAV OS | L2 CM       |
| 7            | E5b-Q          | L2 CL       |
| 8            | E5b-I+E5b-Q    | L2 CM+CL    |
| 9            | E5-I           | L2 P        |
| 10           | E5-Q           | Reserved    |
| 11           | E5-I + E5-Q    | L5 I        |
| 12           | E6-B C/NAV HAS | L5 Q        |
| 13           | E6-C           | L5 I + L5 Q |
| 14           | E6-B + E6-C    | Reserved    |
| 15           | Reserved       | Reserved    |

表 7-148 导航电文索引

| Navigation Message Index | Galileo  | GPS           |
|--------------------------|----------|---------------|
| 0                        | I/NAV    | LNAV (L1 C/A) |
| 1-7                      | Reserved | Reserved      |

#### E6ORBITBLOCK 轨道改正

该消息提供了当前模组解算出的 E6 HAS 服务提供的轨道改正信息，该消息仅支持 ONCHANGED 输出。

Message ID: 2320 ASCII 输出语法:

E6ORBITBLOCKA ONCHANGED

Binary 输出语法:

E6ORBITBLOCKB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

消息输出：

\#E6ORBITBLOCKA,62,GPS,FINE,2287,384303800,0,0,18,26;2700,50,19,25,0,10,0,13,

\-16,-150,-25,17,71,-34,-48,113,-352,-54,-84,48,-28,-33,23,30,42,167,119,60,-21,83,-19,1

3,91,18,10,32,84,-171,-113,145,-74,-82,110,20,-345,-4,46,102,-59,-178,-74,103,-8,-23,14,

169,-331,160,-66,1,-49,106,-22,54,37,-72,-15,65,-10,74,-163,233,-422,-54,-50,74,40,-296,

\-78,62,-66,224,-13,54,45,-259,19,32,-374,29,-20,51,69,-98,-32,51,-58,22,17,34,-125,-71,-

58,45,-406,-66,-63,44,-88,96,67,44,85,75,20,40,-58,79,-24,84,26,-118,128,127,131,-7,-5,1

27,20,12,23,127,31,-33,-21,127,-59,36,5,236,70,61,49,127,-7,9,-15,126,8,-12,19,127,-22,

12,-12,127,42,-6,14,127,-69,15,32,127,-38,0,44,127,51,-30,-33,127,-35,-4,17,126,35,12,3

2,127,36,13,12,127,-117,-7,31,127,-110,13,54,127,56,-4,18,127,21,-32,17,127,-107,34,21,

127,54,7,17,121,32,-15,-19,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0\*35090b59

表 7-149 E6ORBITBLOCK 数据结构

| ID  | 字段                 | 数据描述                                                                                              | 类型 | 字节数 | 字节偏移 |
|-----|----------------------|-------------------------------------------------------------------------------------------------------|------|--------|----------|
|   1 |  E6ORBITBLOCK header | 消息头，二进制消息头结构请参 考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |      |   H    |   0      |

| ID                                                          | 字段              | 数据描述                                                                                                                                                                                 | 类型         | 字节数   | 字节偏移   |
|-------------------------------------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------|------------|
|    2                                                        |    TOH            | 消息接收时间（时内秒），与 GST 时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。                                                                              |    ULONG     |    4     |    H       |
|        3                                                    |        Block Flag | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表 有，“0”代表无 |        UCHAR |        1 |        H+4 |
| 4                                                           | Reserved          | 保留位                                                                                                                                                                                   | UCHAR        | 1        | H+5        |
| 5                                                           | MASK ID           | 掩码 ID                                                                                                                                                                                  | UCHAR        | 1        | H+6        |
| 6                                                           | IOD Set ID        | 数据期号系列 ID                                                                                                                                                                          | UCHAR        | 1        | H+7        |
|  7                                                          |  VI               | 改正数有效期间隔，见[表7-150](#_bookmark385) [有效期间隔](#_bookmark385)                                                                                                                 |  SHORT       |  2       |  H+8       |
| 8                                                           | Reserved          | 保留位                                                                                                                                                                                   | SHORT        | 2        | H+10       |
| 以下内容根据当前 HAS 服务提供的卫星数据，固定循环 68 次输出 |                   |                                                                                                                                                                                          |              |          |            |
|  9                                                          |  IODref           | 数据期号，用于标识改正的轨道 和时钟信息                                                                                                                                                  |  USHORT      |  2       |  H+12      |
|    10                                                       |    DR             | 轨道径向改正， “1000000000000”表示数据 不可用，单位：米，比例： 0.0025，范围：±10.2375                                                                                                   |    SHORT     |    2     |    H+14    |

| ID    | 字段     | 数据描述                                                                             | 类型     | 字节数 | 字节偏移    |
|-------|----------|--------------------------------------------------------------------------------------|----------|--------|-------------|
|    11 |    DIT   | 轨道切向改正， “100000000000”表示数据不 可用，单位：米，比例： 0.008，范围：±16.376  |    SHORT |    2   |    H+16     |
|    12 |    DCT   | 轨道法向改正， “100000000000” 表示数据不 可用，单位：米，比例： 0.008，范围：±16.376 |    SHORT |    2   |    H+18     |
|  13   |  xxxx    | 32 位 CRC 校验（仅 ASCII 和二 进制）                                                 |  Hex     |  4     |  H+12+8\*68 |
| 14    | [CR][LF] | 语句结束符（仅 ASCII）                                                               | -        | -      | -           |

表 7-150 有效期间隔

| Validity Interval Index | Validity Interval |
|-------------------------|-------------------|
| 0                       | 5 s               |
| 1                       | 10 s              |
| 2                       | 15 s              |
| 3                       | 20 s              |
| 4                       | 30 s              |
| 5                       | 60 s              |
| 6                       | 90 s              |
| 7                       | 120 s             |
| 8                       | 180 s             |
| 9                       | 240 s             |
| 10                      | 300 s             |
| 11                      | 600 s             |
| 12                      | 900 s             |
| 13                      | 1800 s            |
| 14                      | 3600 s            |
| 15                      | Reserved          |

#### E6CLOCKFULLBLOCK 钟差全集改正

该消息提供了当前模组解算出的 E6 HAS 服务提供的钟差全集改正信息，该消息仅支持 ONCHANGED 输出。

Message ID: 2321

ASCII 输出语法:

E6CLOCKFULLBLOCKA ONCHANGED

Binary 输出语法:

E6CLOCKFULLBLOCKB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

消息输出：

\#E6CLOCKFULLBLOCKA,63,GPS,FINE,2287,384268800,0,0,18,27;2667,8,15,24,15,5, 0,0,0,0,0,-639,40,-311,118,365,-322,-166,60,-717,-159,-142,-4096,-190,333,-254,-619,-9

7,-783,-504,-705,-107,285,-279,-142,-4096,-21,-72,-424,189,241,260,12,61,-111,27,-25,-6

2,181,71,-104,-88,101,-36,154,11,-73,-76,74,-19,3,-64,-88,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0\*

3f50e3fc

表 7-151 E6CLOCKFULLBLOCK 数据结构

| ID   | 字段                      | 数据描述                                                                                                    | 类型     | 字节数 | 字节偏移 |
|------|---------------------------|-------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1  |  E6CLOCKFULLBL OCK header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)       |          |   H    |   0      |
|    2 |    TOH                    | 消息接收时间（时内秒），与 GST 时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。 |    ULONG |    4   |    H     |

| ID       | 字段              | 数据描述                                                                                                                                                                                 | 类型          | 字节数   | 字节偏移   |
|----------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|----------|------------|
|        3 |        Block Flag | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表 有，“0”代表无 |        UCHAR  |        1 |        H+4 |
| 4        | Reserved          | 保留位                                                                                                                                                                                   | UCHAR         | 1        | H+5        |
| 5        | MASK ID           | 掩码 ID                                                                                                                                                                                  | UCHAR         | 1        | H+6        |
| 6        | IOD Set ID        | 数据期号系列 ID                                                                                                                                                                          | UCHAR         | 1        | H+7        |
|  7       |  VI               | 改正数有效期间隔，见[表7-150](#_bookmark385) [有效期间隔](#_bookmark385)                                                                                                                 |  SHORT        |  2       |  H+8       |
| 8        | Reserved          | 保留位                                                                                                                                                                                   | SHORT         | 2        | H+10       |
|    9     |    DCM            | 时钟改正乘数，每个参数 2 bit，参数个数为被改正的 GNSS 数量 （Nsys），详见[表7-152 DCM 参](#_bookmark388) [数](#_bookmark388)                                                             |   UCHAR[ 4]   |    4     |    H+12    |
|    10    |    DCC            | 时钟改正数据， “1000000000000”表示数据不可用，“0111111111111”表示 卫星不可用，单位：米，比例： 0.0025，范围：±10.2375                                                                    |    SHORT[ 68] |    136   |    H+16    |
|  11      |  xxxx             | 32 位 CRC 校验（仅 ASCII 和二 进制）                                                                                                                                                     |  Hex          |  4       |  H+152     |
| 12       | [CR][LF]          | 语句结束符（仅 ASCII）                                                                                                                                                                   | -             | -        | -          |

表 7-152 DCM 参数

| DCM Value | Multiplier |
|-----------|------------|
| “00”      | 1          |
| “01”      | 2          |
| “10”      | 3          |
| “11”      | 4          |

#### E6CLOCKSUBBLOCK 钟差子集改正

该消息提供了当前模组解算出的 E6 HAS 服务提供的钟差子集改正信息，该消息仅支持 ONCHANGED 输出。

Message ID: 2322

ASCII 输出语法:

E6CLOCKSUBBLOCKA ONCHANGED

Binary 输出语法:

E6CLOCKSUBBLOCKB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

表 7-153 E6CLOCKSUBBLOCK 数据结构

| ID   | 字段                     | 数据描述                                                                                                    | 类型     | 字节数 | 字节偏移 |
|------|--------------------------|-------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1  |  E6CLOCKSUB BLOCK header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)       |          |   H    |   0      |
|    2 |    TOH                   | 消息接收时间（时内秒），与 GST 时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。 |    ULONG |    4   |    H     |

| ID                                                                    | 字段              | 数据描述                                                                                                                                                                                 | 类型         | 字节数   | 字节偏移   |
|-----------------------------------------------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------|------------|
|        3                                                              |        Block Flag | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表 有，“0”代表无 |        UCHAR |        1 |        H+4 |
| 4                                                                     | Reserved          | 保留位                                                                                                                                                                                   | UCHAR        | 1        | H+5        |
| 5                                                                     | MASK ID           | 掩码 ID                                                                                                                                                                                  | UCHAR        | 1        | H+6        |
| 6                                                                     | IOD Set ID        | 数据期号系列 ID                                                                                                                                                                          | UCHAR        | 1        | H+7        |
|  7                                                                    |  VI               | 改正数有效期间隔，见[表7-150](#_bookmark385) [有效期间隔](#_bookmark385)                                                                                                                 |  SHORT       |  2       |  H+8       |
| 8                                                                     | Nsys              | 具有改正数的 GNSS 数量                                                                                                                                                                   | SHORT        | 2        | H+10       |
| 以下内容按照 Nsys 提供的数量进行循环输出，当前 Nsys 固定循环 2 次输出 |                   |                                                                                                                                                                                          |              |          |            |
|    9                                                                  |    GNSS ID        | GNSS ID 0：GPS 1：保留 2：Galileo 3-15：保留                                                                                                                                             |    USHORT    |    2     |    H+12    |
|    10                                                                 |    DCM            | 时钟改正乘数，每个参数 2 bit，参数个数为被改正的 GNSS 数量 （Nsys），详见[表7-152 DCM](#_bookmark388) [参数](#_bookmark388)                                                              |    USHORT    |    2     |    H+14    |

| ID     | 字段         | 数据描述                                                                                                                                                                      | 类型          | 字节数 | 字节偏移 |
|--------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|--------|----------|
|     11 |     Sat Mask | 卫星掩码，字段长度为 40 bit，用于标识已改正的卫星 （“1”）和未改正的卫星 （“0”）。详见[表7-146 卫星](#_bookmark380)[掩码](#_bookmark380)。最高有效位对应 Satellite Index = 0。 |     Hex       |     5  |     H+16 |
| 12     | Reserved     | 保留位                                                                                                                                                                        | UCHAR[3]      | 3      | H+21     |
|    13  |    DCC       | 时钟改正数据， “1000000000000”表示数据不可用，“0111111111111”表示 卫星不可用，单位：米，比例： 0.0025，范围：±10.2375                                                         |    SHORT[3 6] |    72  |    H+24  |
|  14    |  xxxx        | 32 位 CRC 校验（仅 ASCII 和二 进制）                                                                                                                                          |  Hex          |  4     |  H+96    |
| 15     | [CR][LF]     | 语句结束符（仅 ASCII）                                                                                                                                                        | -             | -      | -        |

#### E6CBIASBLOCK 码偏差改正

该消息提供了当前模组解算出的 E6 HAS 服务提供的码偏差改正信息，该消息仅支持 ONCHANGED 输出。

Message ID: 2323

ASCII 输出语法:

E6CBIASBLOCKA ONCHANGED

Binary 输出语法:

E6CBIASBLOCKAB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

消息输出：

\#E6CBIASBLOCKA,62,GPS,FINE,2287,384303800,0,0,18,27;2700,50,19,25,0,14,0,-30 4,-327,791,799,222,-17,-289,-129,-488,488,976,815,590,-202,-368,584,-768,975,734,-2,-

121,-833,959,663,-841,959,640,248,680,400,720,-648,-856,680,-928,136,504,216,392,86

4,640,744,-832,544,-840,904,256,640,424,-359,728,744,-816,848,-648,304,728,511,999,5

43,319,959,335,255,558,-74,-408,432,936,712,560,-976,935,-1017,599,368,864,-456,-62

5,-929,671,504,80,144,207,-273,-361,-657,-649,-368,424,760,752,375,-609,951,967,-568,

424,768,784,615,-121,-217,-217,-256,8,15,-49,-528,-415,881,841,664,-775,225,113,247,-

617,943,983,-497,-729,735,767,-888,448,800,760,511,-273,-497,-473,-824,456,816,840,3

43,-449,-809,-801,-288,512,920,936,207,-249,-449,-441,-809,-241,-433,-401,-153,-537,-9

61,-953,-152,432,776,776,199,-457,-825,-873,-737,-641,895,887,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0\*3cebdc0a

表 7-154 E6CBIASBLOCK 数据结构

| ID   | 字段                  | 数据描述                                                                                                                | 类型     | 字节数 | 字节偏移 |
|------|-----------------------|-------------------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1  |  E6CBIASBLO CK header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |          |   H    |   0      |
|    2 |    TOH                | 消息接收时间（时内秒），与 GST时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。              |    ULONG |    4   |    H     |

| ID       | 字段              | 数据描述                                                                                                                                                                                 | 类型           | 字节数   | 字节偏移   |
|----------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|----------|------------|
|        3 |        Block Flag | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表有， “0”代表无 |        UCHAR   |        1 |        H+4 |
| 4        | Reserved          | 保留位                                                                                                                                                                                   | UCHAR          | 1        | H+5        |
| 5        | MASK ID           | 掩码 ID                                                                                                                                                                                  | UCHAR          | 1        | H+6        |
| 6        | IOD Set ID        | 数据期号系列 ID                                                                                                                                                                          | UCHAR          | 1        | H+7        |
|  7       |  VI               | 改正数有效期间隔，见[表7-150 有](#_bookmark385) [效期间隔](#_bookmark385)                                                                                                                |  SHORT         |  2       |  H+8       |
| 8        | Reserved          | 保留位                                                                                                                                                                                   | SHORT          | 2        | H+10       |
|    9     |    Code Biases    | 第 n 个 SV 第 m 个信号的码偏差，如[表7-147 信号掩码](#_bookmark381)所示（或单元掩码所定义）。“10000000000”表示数据不可用，单位：米，比 例：0.0025，范围：±10.2375                        |    SHORT[ 256] |    512   |    H+12    |
|  10      |  xxxx             | 32 位 CRC 校验（仅 ASCII 和二进 制）                                                                                                                                                     |  Hex           |  4       |  H+524     |
| 11       | [CR][LF]          | 语句结束符（仅 ASCII）                                                                                                                                                                   | -              | -        | -          |

#### E6PBIASBLOCK 相位偏差改正

该消息提供了当前模组解算出的 E6 HAS 服务提供的相位偏差改正信息，该消息仅支持 ONCHANGED 输出。

Message ID: 2324 ASCII 输出语法:

E6PBIASBLOCKA ONCHANGED

Binary 输出语法:

E6PBIASBLOCKB ONCHANGED

适用产品：UM980、UM982、UB9A0、UM981

表 7-155 E6PBIASBLOCK 数据结构

| ID       | 字段                  | 数据描述                                                                                                                                                                                 | 类型         | 字节数   | 字节偏移   |
|----------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------|------------|
|   1      |  E6PBIASBLO CK header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211)                                                                   |              |   H      |   0        |
|    2     |    TOH                | 消息接收时间（时内秒），与 GST时间有关。消息适用时间的计算方法见 Galileo HAS SIS ICD Issue 1.0 第 7.7 章。                                                                               |    ULONG     |    4     |    H       |
|        3 |        Block Flag     | 消息标识，6 比特 Bit5：掩码信息标识 Bit4：轨道改正标识 Bit3：钟差全集改正标识 Bit2：钟差子集改正标识 Bit1：码偏差改正标识 Bit0：相位偏差改正标识 以上每个比特位中，“1”代表有， “0”代表无 |        UCHAR |        1 |        H+4 |
| 4        | Reserved              | 保留位                                                                                                                                                                                   | UCHAR        | 1        | H+5        |
| 5        | MASK ID               | 掩码 ID                                                                                                                                                                                  | UCHAR        | 1        | H+6        |
| 6        | IOD Set ID            | 数据期号系列 ID                                                                                                                                                                          | UCHAR        | 1        | H+7        |

| ID                                             | 字段             | 数据描述                                                                                                                                                          | 类型      | 字节数 | 字节偏移     |
|------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|--------------|
|  7                                             |  VI              | 改正数有效期间隔，见[表7-150 有](#_bookmark385) [效期间隔](#_bookmark385)                                                                                         |  SHORT    |  2     |  H+8         |
| 8                                              | Reserved         | 保留位                                                                                                                                                            | SHORT     | 2      | H+10         |
| 以下内容按当前 HAS 服务播发情况循环输出 256 次 |                  |                                                                                                                                                                   |           |        |              |
|     9                                          |     Phase Biases | 第 n 个 SV 第 m 个信号的相位偏差，如[表7-147 信号掩码](#_bookmark381)所示（或单元掩码所定义）。 “10000000000”表示数据不可 用，单位：米，比例：0.01，范围： ±10.23 |     SHORT |     2  |     H+12     |
|   10                                           |   PDI            | 第 n 个 SV 第 m 个信号的相位不连续标识，如[表7-147 信号掩码](#_bookmark381)所示 （或单元掩码所定义）                                                              |  USHOR T  |   2    |   H+14       |
|  11                                            |  xxxx            | 32 位 CRC 校验（仅 ASCII 和二进 制）                                                                                                                              |  Hex      |  4     | H+12+4\* 256 |
| 12                                             | [CR][LF]         | 语句结束符（仅 ASCII）                                                                                                                                            | -         | -      | -            |

#### BSLNENUHD2 东北天坐标系下的基线长度

该消息包含东北天坐标系（ENU）下使用 Heading2 定向时的基线长度相关信息。

-   关于 Heading2 的详细释义，请参考第 [3.7](#_bookmark28) 章。
-   该消息需要开启 Heading2（输入指令 MODE HEADING2）后才能输出。

Message ID: 1316 ASCII 输出语法:

BSLNENUHD2A ONCHANGED

Binary 输出语法:

BSLNENUHD2B ONCHANGED

适用产品：UM980、UMD980、UM982、UMD982、UB9A0、UBD9A0

消息输出：

\#BSLNENUHD2A,78,GPS,FINE,2298,444774000,0,0,18,466;SOL_COMPUTED,NARROW\_ INT,10722.7418,306.2500,-16.3518,0.0134,0.0190,0.0354,"","201",51,29,29,29,3,01,03,cb\*c4 2490b3

表 7-156 BSLNENUHD2 数据结构

| ID  | 字段               | 数据描述                                                                                                               | 类型    | 字节数 | 字节偏移 |
|-----|--------------------|------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  BSLNENUHD2 header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |         |   H    |   0      |
| 2   | sol status         | 解算状态，参考[表0- 5 解的状态](#_bookmark435)                                                                         | Enum    | 4      | H        |
|  3  |  pos type          | 位置类型，参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)                                                 |  Enum   |  4     |  H+4     |
|  4  |  East              | （流动站相对于基准站）基线的东 向分量，单位：米                                                                        |  Double |  8     |  H+8     |
|  5  |  North             | （流动站相对于基准站）基线的北 向分量，单位：米                                                                        |  Double |  8     |  H+16    |
|  6  |  Up                | （流动站相对于基准站）基线的天 向分量，单位：米                                                                        |  Double |  8     |  H+24    |
| 7   | East STD           | 基线东向分量的标准差，单位：米                                                                                         | Float   | 4      | H+32     |
| 8   | North STD          | 基线北向分量的标准差，单位：米                                                                                         | Float   | 4      | H+36     |
| 9   | Up STD             | 基线天向分量的标准差，单位：米                                                                                         | Float   | 4      | H+40     |
| 10  | Rover ID           | 流动站 ID                                                                                                              | Char[4] | 4      | H+44     |
| 11  | Master ID          | 基准站 ID                                                                                                              | Char[4] | 4      | H+48     |
| 12  | \#SVs              | 跟踪的卫星数                                                                                                           | Uchar   | 1      | H+52     |
| 13  | \#solnSVs          | 解算使用的卫星数                                                                                                       | Uchar   | 1      | H+53     |
| 14  | Reserved           | 保留位                                                                                                                 | Uchar   | 1      | H+54     |

| ID    | 字段                            | 数据描述                                                                                                                            | 类型   | 字节数 | 字节偏移 |
|-------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
| 15    | Reserved                        | 保留位                                                                                                                              | Uchar  | 1      | H+55     |
| 16    | Reserved                        | 保留位                                                                                                                              | Hex    | 1      | H+56     |
|  17   |  ext sol stat                   | 扩展解的状态，参考[表7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                              |  Hex   |  1     |  H+57    |
|   18  |  Galileo&BDS3 sig mask          | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                           |   Hex  |   1    |   H+58   |
|    19 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码，参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号掩](#_bookmark273)[码](#_bookmark273) |    Hex |    1   |    H+59  |
|  20   |  xxxx                           | 32 位 CRC 校验（仅 ASCII 和二进 制）                                                                                                |  Hex   |  4     |  H+60    |
| 21    | [CR][LF]                        | 语句结束符（仅 ASCII）                                                                                                              | -      | -      | -        |

#### BSLNXYZHD2 直角坐标系下的基线长度

该消息包含直角坐标系（XYZ）下使用 Heading2 定向时的基线长度相关信息。

-   关于 Heading2 的详细释义，请参考第 [3.7](#_bookmark28) 章。
-   该消息需要开启 Heading2（输入指令 MODE HEADING2）后才能输出。

Message ID: 1317 ASCII 输出语法:

BSLNXYZHD2A ONCHANGED

Binary 输出语法:

BSLNXYZHD2B ONCHANGED

适用产品：UM980、UMD980、UM982、UMD982、UB9A0、UBD9A0

消息输出：

\#BSLNXYZHD2A,78,GPS,FINE,2298,444774000,0,0,18,465;SOL_COMPUTED,NARROW_I NT,-9536.1481,-4907.4470,223.8114,0.0212,0.0332,0.0154,"","201",51,29,29,29,3,01,03,cb\* 2427e31b

表 7-157 BSLNXYZHD2 数据结构

| ID  | 字段               | 数据描述                                                                                                                | 类型    | 字节数 | 字节偏移 |
|-----|--------------------|-------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  BSLNXYZHD2 header | 消息头，二进制消息头结构请参考 [表7-50](#_bookmark210)，ASCII 消息头结构请参考[表](#_bookmark211) [7-51](#_bookmark211) |         |   H    |   0      |
| 2   | sol status         | 解算状态，参考[表0- 5 解的状态](#_bookmark435)                                                                          | Enum    | 4      | H        |
|  3  |  pos type          | 位置类型，参考[表0- 4 位置或速度](#_bookmark434) [类型](#_bookmark434)                                                  |  Enum   |  4     |  H+4     |
|  4  |  dX                | （流动站相对于基准站）基线的 X 轴分量，单位：米                                                                         |  Double |  8     |  H+8     |
|  5  |  dY                | （流动站相对于基准站）基线的 Y 轴分量，单位：米                                                                         |  Double |  8     |  H+16    |
|  6  |  dZ                | （流动站相对于基准站）基线的 Z 轴分量，单位：米                                                                         |  Double |  8     |  H+24    |
| 7   | dX STD             | 基线 X 轴分量的标准差，单位：米                                                                                         | Float   | 4      | H+32     |
| 8   | dY STD             | 基线 Y 轴分量的标准差，单位：米                                                                                         | Float   | 4      | H+36     |
| 9   | dZ STD             | 基线 Z 轴分量的标准差，单位：米                                                                                         | Float   | 4      | H+40     |
| 10  | Rover ID           | 流动站 ID                                                                                                               | Char[4] | 4      | H+44     |
| 11  | Master ID          | 基准站 ID                                                                                                               | Char[4] | 4      | H+48     |
| 12  | \#SVs              | 跟踪的卫星数                                                                                                            | Uchar   | 1      | H+52     |
| 13  | \#solnSVs          | 解算使用的卫星数                                                                                                        | Uchar   | 1      | H+53     |
| 14  | Reserved           | 保留位                                                                                                                  | Uchar   | 1      | H+54     |
| 15  | Reserved           | 保留位                                                                                                                  | Uchar   | 1      | H+55     |
| 16  | Reserved           | 保留位                                                                                                                  | Hex     | 1      | H+56     |

| ID    | 字段                            | 数据描述                                                                                                                             | 类型   | 字节数 | 字节偏移 |
|-------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
|  17   |  ext sol stat                   | 扩展解的状态，参考[表7-89 扩展解](#_bookmark275) [状态](#_bookmark275)                                                               |  Hex   |  1     |  H+57    |
|   18  |  Galileo&BDS3 sig mask          | Galileo 和 BDS3 使用的信号掩码。参考[表7-88 Galileo&BDS3 使用的](#_bookmark274) [信号掩码](#_bookmark274)                            |   Hex  |   1    |   H+58   |
|    19 |  GPS, GLONASS and BDS2 sig mask | GPS, GLONASS 和 BDS2 使用的信 号掩码，参考[表7-87](#_bookmark273) [GPS/GLONASS/BDS2 使用的信号掩](#_bookmark273) [码](#_bookmark273) |    Hex |    1   |    H+59  |
|  20   |  xxxx                           | 32 位 CRC 校验（仅 ASCII 和二进 制）                                                                                                 |  Hex   |  4     |  H+60    |
| 21    | [CR][LF]                        | 语句结束符（仅 ASCII）                                                                                                               | -      | -      | -        |

#### DOPHD2 Heading2 精度因子

该消息包含 Heading2 解算所用卫星的精度因子（DOP）。

-   关于 Heading2 的详细释义，请参考第 [3.7](#_bookmark28) 章。
-   该消息需要开启 Heading2（输入指令 MODE HEADING2）后才能输出。

Message ID: 1333 ASCII 输出语法:

DOPHD2A ONCHANGED

Binary 输出语法:

DOPHD2B ONCHANGED

适用产品：UM980、UMD980、UM982、UMD982、UB9A0、UBD9A0

消息输出：

\#DOPHD2A,78,GPS,FINE,2298,444774000,0,0,18,466;1.7488,1.4302,0.7034,1.2278,1.00 63,2.0,29,4,16,28,31,34,39,81,82,101,161,162,163,167,169,170,171,176,183,185,192,197,199

,200,203,219,220,26,104,166\*50cc4364

表 7-158 DOPHD2 数据结构

| ID  | 字段           | 数据描述                                                                                                                                     | 类型    | 字节数 | 字节偏移 |
|-----|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|   1 |  DOPHD2 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考 [表7-51](#_bookmark211)                                       |         |   H    |   0      |
| 2   | GDOP           | 几何精度因子                                                                                                                                 | Float   | 4      | H        |
| 3   | PDOP           | 位置精度因子                                                                                                                                 | Float   | 4      | H+4      |
| 4   | HDOP           | 水平精度因子                                                                                                                                 | Float   | 4      | H+8      |
| 5   | HTDOP          | 水平和时间精度因子                                                                                                                           | Float   | 4      | H+12     |
| 6   | TDOP           | 时间精度因子                                                                                                                                 | Float   | 4      | H+16     |
| 7   | Elev mask      | 截止高度角                                                                                                                                   | Float   | 4      | H+20     |
| 8   | \#sats         | 跟踪卫星总数                                                                                                                                 | Ulong   | 4      | H+24     |
|   9 |   Sats list    | 跟踪卫星的 PRN （ 详见[表 7-55](#_bookmark217) [Unicore 消息中的卫星 PRN 偏](#_bookmark217) [移](#_bookmark217)），在位置解可用前为null 字段 |   Ulong |   4    |   H+28   |
|  10 |  xxxx          | 32 位 CRC 校验（仅 ASCII 和二进 制）                                                                                                         |  Hex    |  4     |  H+32    |
| 11  | [CR][LF]       | 语句结束符（仅 ASCII）                                                                                                                       | -       | -      | -        |

#### L6MDCTYPE1 卫星掩码信息

本指令包含 QZSS MADOCA-PPP 信息类型 1，包含卫星掩码信息，详细可参考 QZSS ICD 文件。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2325 ASCII 输出语法：

L6MDCTYPE1A ONCHANGED

Binary 输出语法：

L6MDCTYPE1B ONCHANGED

适用产品：UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE1A,89,GPS,FINE,2331,121686000,16071,0,18,28;36,4073,1,121685,5,0, 11,4,0,0,0,7,0,7F7B7BFF00,A4A4,1,0,0,0,CB7FF6DF6DF7FF6CB6CBFCB2CBFDF7DF7FF6 DF6DC000000000000000000000000000000000000000,1,F3B7FD0000,F000,0,0,0,0,0000 000000000000000000000000000000000000000000000000000000000000000000000000

0000,2,7AFA29C2D0,2400,0,0,0,0,00000000000000000000000000000000000000000000

000000000000000000000000000000000000,4,6000000000,9240,0,0,0,0,0000000000000

0000000000000000000000000000000000000000000000000000000000000000000\*79a6

8e3a

表 7-159 L6MDCTYPE1 数据结构

| ID  | 字段               | 数据描述                                                                                               | 类型                           | 字节数        | 字节偏移        |
|-----|--------------------|--------------------------------------------------------------------------------------------------------|--------------------------------|---------------|-----------------|
|   1 |  L6MDCTYPE1 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |                                |   H1          |   0             |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头结 构参考[表7-160](#_bookmark403)                                               |                                |  H2           |  H1             |
|   3 |   MASK             |   掩码数据                                                                                             | StL6PPPMsgS ysMask_t[Nu mGNSS] |  52\*Nu mGNSS |  H(H1+H 2)      |
|   4 |   Xxxx             |   32 位 CRC 校验                                                                                       |   HEX                          |   4           | H+52\*N umGNS S |
| 5   | [CR][LF]           | 语句结束符(仅 ASCII)                                                                                   |                                |               |                 |

typedef struct

{

UCHAR usGnssID;

UCHAR aucSatMask[5];

UCHAR aucSigMask[2];

UCHAR ucCellMaskVali; UCHAR aucReserved[3];

UCHAR aucCellMask[40]; //

}_PACKED\_ StL6PPPMsgSysMask_t;

表 7-160 L6 改正数消息头

| ID | 字段       | 类型   | 描述               | 字节数 | 字节偏移 |
|----|------------|--------|--------------------|--------|----------|
| 1  | PRN        | ULONG  | PRN 编号           | 4      | 0        |
| 2  | MsgNum     | USHORT | 消息编号           | 2      | 4        |
| 3  | SubID      | USHORT | 子类型 ID          | 2      | 6        |
| 4  | EpochTime  | ULONG  | 历元时间           | 4      | 8        |
| 5  | Interval   | USHORT | SSR 更新间隔       | 2      | 12       |
| 6  | Indicator  | UCHAR  | 多消息指示位       | 1      | 14       |
| 7  | SSRIOD     | UCHAR  | SSR 数据版本号     | 1      | 15       |
| 8  | NumGNSS    | UCHAR  | 增强的卫星系统数量 | 1      | 16       |
| 9  | Reserved   | UCHAR  | 预留               | 1      | 17       |
| 10 | HourlyTime | USHORT | 小时历元时间       | 2      | 18       |
| 11 | CorNum     | USHORT | 改正数数量         | 2      | 20       |
| 12 | MsgValid   | USHORT | 消息验证           | 2      | 22       |

![](media/d7a12b509f3def40a5bb667e5857b26e.png)

![](media/03d77b5ff5696422050c36b7b7f17316.png)

![](media/471a2d3333826962e11ad3c50441526a.png)

#### L6MDCTYPE2 轨道改正数

本指令包含 QZSS MADOCA-PPP 信息类型 2，包含卫星轨道改正数信息，详细可参考 QZSS L6 ICD 文件。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2326 ASCII 输出语法：

L6MDCTYPE2A ONCHANGED

Binary 输出语法：

L6MDCTYPE2B ONCHANGED

适用产品：UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE2A,89,GPS,FINE,2331,121686000,16071,0,18,29;36,4073,2,0,5,0,11,0,0

,2885,68,7,172,-432,610,316,53,-132,131,-130,215,-193,235,21,62,159,-119,-105,50,-

123,-266,150,46,-7,-142,13,41,-201,532,100,57,53,-67,-6,136,-4,-27,-58,26,118,-

156,82,71,38,-36,-5,25,58,14,-166,34,11,-27,-64,94,-31,200,-60,103,-39,-132,-

104,62,117,-452,151,18,-249,215,99,109,26,-321,-54,42,191,-110,-70,15,17,281,-

16,104,91,-153,153,17,-15,124,-12,147,-188,586,-4,22,124,-89,-94,54,-43,-60,-103,59,-

95,219,-37,32,-13,-147,77,51,117,52,103,51,217,199,98,51,292,2,158,51,156,-

124,59,51,556,-534,64,51,1,-14,-11,51,444,12,24,51,196,-115,66,51,231,-72,87,51,224,-

13,-45,51,293,255,-125,51,308,307,-96,51,118,-180,-213,51,157,-209,-131,51,322,-676,-

445,51,57,-255,-11,51,81,266,-23,51,568,695,-244,51,284,-569,-50,74,160,-86,-8,73,-

8,21,23,74,156,5,17,74,112,85,17,74,79,12,37,74,108,20,40,74,101,3,-14,74,55,44,-

2,71,65,27,-45,74,206,-76,48,72,225,-67,14,74,111,90,76,74,276,-17,-39,73,115,-19,-

10,72,154,-57,6,74,242,-11,15,74,92,-47,-63,74,196,-10,19,74,91,-77,-5,70,42,-57,-

8,133,403,59,22,133,220,17,36\*7d02c73e

表 7-161 L6MDCTYPE2 数据结构

| ID  | 字段               | 数据描述                                                                                               | 类型                          | 字节数     | 字节偏移  |
|-----|--------------------|--------------------------------------------------------------------------------------------------------|-------------------------------|------------|-----------|
|   1 |  L6MDCTYPE2 header | 消息头，二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消息 头结构请参考[表7-51](#_bookmark211) |                               |   H1       |   0       |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头 结构参考[表7-160](#_bookmark403)                                               |                               |  H2        |  H1       |
|  3  |  OrbitCorr         |  卫星轨道数据                                                                                          | StL6PPPMsgSat Orbit_t[CorNum] | 8\*CorN um | H(H1+H 2) |

| ID | 字段     | 数据描述             | 类型 | 字节数 | 字节偏移     |
|----|----------|----------------------|------|--------|--------------|
|  4 |  Xxxx    |  32 位 CRC 校验      |  HEX |  4     | H+8\*Cor Num |
| 5  | [CR][LF] | 语句结束符(仅 ASCII) |      |        |              |

typedef struct

{

USHORT usIODE;

SHORT sRadial;

SHORT sAlong;

SHORT sCross; //

}_PACKED\_ StL6PPPMsgSatOrbit_t;

#### L6MDCTYPE3 时钟改正数

本指令包含QZSS MADOCA-PPP 信息类型3，包含时钟改正数信息，详细可参考QZSS L6 ICD 文件。命令输入仅支持ONCHANGED 请求方式。

Message ID：2327 ASCII 输出语法：

L6MDCTYPE3A ONCHANGED

Binary 输出语法：

L6MDCTYPE3B ONCHANGED

适用产品： UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE3A,89,GPS,FINE,2331,121671000,16071,0,18,29;36,4073,3,0,2,0,11,0,0

,2870,68,4,-859,684,184,-18,206,86,-349,-175,568,146,-242,349,-457,476,-1106,-895,-

934,567,389,-190,-85,-66,387,-53,-143,219,228,2666,1212,-689,-1579,492,-1751,-

73,897,2194,2403,328,1680,-813,1665,874,-88,-1193,1680,738,146,-22,-51,-199,-164,-

77,-87,327,56,-176,-292,-97,-283,180,-60,-105,-25,26,-208,-68,128,248\*5413e1d3

表 7-162 L6MDCTYPE3 数据结构

| ID  | 字段               | 数据描述                                                                                                | 类型           | 字节数     | 字节偏移     |
|-----|--------------------|---------------------------------------------------------------------------------------------------------|----------------|------------|--------------|
|   1 |  L6MDCTYPE3 header | 消息头， 二进制消息头结构请参考[表 7-50](#_bookmark210)，ASCII 消 息头结构请参考[表7-51](#_bookmark211) |                |   H1       |   0          |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头 结构参考[表7-160](#_bookmark403)                                                |                |  H2        |  H1          |
|  3  |  Clk               |  时钟数据                                                                                               | asClk[CorN um] |  2\*CorNum |  H(H1+H2)    |
|  4  |  Xxxx              |  32 位 CRC 校验                                                                                         |  HEX           |  4         | H+2\*Cor Num |
| 5   | [CR][LF]           | 语句结束符(仅 ASCII)                                                                                    |                |            |              |

#### L6MDCTYPE4 码间偏差改正数

本指令包含 QZSS MADOCA-PPP 信息类型 4，包含码间偏差改正数信息，详细可参考 QZSS L6 ICD 文件。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2328 ASCII 输出语法：

L6MDCTYPE4A ONCHANGED

Binary 输出语法：

L6MDCTYPE4B ONCHANGED

适用产品： UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE4A,89,GPS,FINE,2331,121696000,16071,0,18,30;36,4073,4,0,5,0,11,0, 0,2895,68,12,204,232,336,0,0,0,0,-143,-163,-246,-235,-157,0,0,0,-13,3,10,-1,-63,0,49,38,

77,80,0,0,0,-168,-183,-293,-278,-188,0,0,63,62,111,103,0,0,0,-161,-157,-286,-265,-112,0,

0,-138,-140,-204,-227,-25,0,0,62,47,60,109,101,19,0,76,74,120,125,0,0,0,72,69,118,0,0,0,

0,39,26,71,64,0,0,0,88,107,146,0,0,0,0,50,35,48,86,81,-5,0,197,236,323,0,0,0,0,83,115,13

7,0,0,0,0,101,133,167,0,0,0,0,54,40,52,96,89,1,0,-155,-166,-256,-255,-165,0,0,-159,-143,-

282,-262,-189,0,0,-197,-197,-313,-324,-162,0,0,-125,-122,-203,-206,-69,0,0,67,53,68,116,

110,3,0,43,41,69,70,0,0,0,-142,-132,-241,-234,-137,0,0,85,75,135,140,0,0,0,-116,-125,-19

9,-190,-34,0,0,-100,-88,-140,-164,0,0,0,-21,-19,-35,-34,0,0,0,34,29,52,57,0,0,0,44,32,72,7

3,0,0,0,6,1,2,9,0,0,0,64,48,105,107,0,0,0,51,43,86,86,0,0,0,82,79,135,137,0,0,0,-63,-68,-8

9,-105,0,0,0,-57,-56,-100,-94,0,0,0,-19,-26,-26,-32,0,0,0,-30,-34,-44,-50,0,0,0,13,14,22,22,

0,0,0,-41,-45,-61,-68,0,0,0,41,56,44,67,0,0,0,-120,-117,-233,-198,0,0,0,4,4,14,6,0,0,0,68,6

3,122,112,0,0,0,3,4,5,4,0,0,0,17,34,0,0,0,0,0,-39,-76,0,0,0,0,0,53,102,0,0,0,0,0,-47,-83,0,0,

0,0,0,-76,-138,0,0,0,0,0,-15,-28,0,0,0,0,0,3,9,0,0,0,0,0,198,362,0,0,0,0,0,161,292,0,0,0,0,0,

\-75,-137,0,0,0,0,0,-90,-163,0,0,0,0,0,51,94,0,0,0,0,0,-26,-47,0,0,0,0,0,58,105,0,0,0,0,0,-52,

\-98,0,0,0,0,0,69,120,0,0,0,0,0,-57,-108,0,0,0,0,0,56,105,0,0,0,0,0,-60,-108,0,0,0,0,0,-83,-1 49,0,0,0,0,0,-78,-79,-128,-112,0,0,0,-62,-66,-99,-111,0,0,0\*54a25c17

表 7-163 L6MDCTYPE4 数据结构

| ID  | 字段               | 数据描述                                                                                              | 类型                        | 字节数      | 字节偏移      |
|-----|--------------------|-------------------------------------------------------------------------------------------------------|-----------------------------|-------------|---------------|
|   1 |  L6MDCTYPE4 header | 消息头，二进制消息头结 构请参考[表 7-50](#_bookmark210)，ASCII消息头结构请参考[表7-51](#_bookmark211) |                             |   H1        |   0           |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头 结构参考[表7-160](#_bookmark403)                                              |                             |  H2         |  H1           |
|  3  |  CodeBias          |  码间偏差数据                                                                                         | StL6PPPSatCod eBias[CorNum] | 14\*CorN um |  H(H1+H2)     |
|  4  |  Xxxx              |  32 位 CRC 校验                                                                                       |  HEX                        |  4          | H+14\*Cor Num |
| 5   | [CR][LF]           | 语句结束符(仅 ASCII)                                                                                  |                             |             |               |

typedef struct

{

SHORT sCBias[7]; //

}_PACKED\_ StL6PPPSatCodeBias;

#### L6MDCTYPE5 相位偏差改正数

本指令包含 QZSS MADOCA-PPP 信息类型 5，包含相位偏差改正数信息，详细可参考 QZSS L6 ICD 文件。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2329 ASCII 输出语法：

L6MDCTYPE5A ONCHANGED

Binary 输出语法：

L6MDCTYPE5B ONCHANGED

适用产品： UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE5A,89,GPS,FINE,2331,121676000,16071,0,18,29;36,4073,5,0,5,0,11,0, 0,2875,68,20,1838,459,-16185,0,0,0,0,2,3,0,0,0,0,0,-343,8106,10223,-15877,-3969,0,0,0,

3,2,3,0,0,0,1593,398,8291,-14303,-1528,16002,0,0,3,1,0,0,0,0,114,28,-14343,-1538,0,0,0,

1,3,3,0,0,0,0,-692,8019,1987,12784,-4997,0,0,1,2,2,3,0,0,0,-1026,7935,-14422,6634,0,0,0,

2,0,3,0,0,0,0,-2114,7663,-14523,4561,9332,0,0,0,0,2,3,0,0,0,-1045,7930,-6233,10729,-55

11,0,0,3,3,3,1,0,0,0,-77,8172,-6149,6650,-4994,-9441,0,3,1,1,2,3,0,0,553,138,8235,2058,

0,0,0,3,0,1,0,0,0,0,-285,8120,-6190,0,0,0,0,1,3,0,0,0,0,0,383,95,-8188,-12287,0,0,0,0,2,2,

0,0,0,0,1235,308,-8080,0,0,0,0,1,2,0,0,0,0,0,-8,8190,2047,-15879,-1410,16031,0,3,0,0,2,1,

0,0,1266,316,-16274,0,0,0,0,2,3,0,0,0,0,0,-884,7971,1968,0,0,0,0,3,3,0,0,0,0,0,1099,274,-

8039,0,0,0,0,1,1,0,0,0,0,0,-143,8156,10231,2552,-14722,4511,0,2,0,3,0,2,0,0,-228,8135,1

996,14835,3708,0,0,1,1,1,1,0,0,0,290,72,-16361,-16379,-3969,0,0,3,1,1,2,0,0,0,743,185,-

8131,10255,10755,0,0,2,1,0,1,0,0,0,-477,8072,-6181,6646,-6531,0,0,3,2,3,0,0,0,0,483,12

0,-8162,6157,-3581,15489,0,0,3,0,2,3,0,0,-670,8024,-14383,14836,0,0,0,1,1,3,0,0,0,0,-22

50,7629,-14520,-1582,7796,0,0,3,3,2,0,0,0,0,-498,8067,-14384,12788,0,0,0,0,1,2,0,0,0,0,-

256,8128,2022,4601,-15234,0,0,0,0,1,2,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,

0,0,0,1238,366,0,0,0,0,0,0,0,0,0,0,0,0,2179,620,0,0,0,0,0,0,0,0,0,0,0,0,1079,526,0,0,0,0,0,

3,0,0,0,0,0,0,338,219,0,0,0,0,0,1,0,0,0,0,0,0,708,87,0,0,0,0,0,1,0,0,0,0,0,0,982,429,0,0,0,0,

0,0,0,0,0,0,0,0,-1561,7588,0,0,0,0,0,3,0,0,0,0,0,0,-4978,6048,0,0,0,0,0,2,0,0,0,0,0,0,-459,

7680,0,0,0,0,0,2,0,0,0,0,0,0,-55,14,0,0,0,0,0,2,0,0,0,0,0,0,1422,528,0,0,0,0,0,2,0,0,0,0,0,0,

\-2492,7672,0,0,0,0,0,2,0,0,0,0,0,0,335,91,0,0,0,0,0,0,0,0,0,0,0,0,-283,8062,0,0,0,0,0,3,0,0,

0,0,0,0,48,6,0,0,0,0,0,2,0,0,0,0,0,0,-153,483,0,0,0,0,0,2,0,0,0,0,0,0,-2045,7279,0,0,0,0,0,3,

0,0,0,0,0,0,-1053,7954,0,0,0,0,0,0,0,0,0,0,0,0,1391,664,0,0,0,0,0,1,0,0,0,0,0,0,569,143,0,

0,0,0,0,0,0,0,0,0,0,0,103,25,-6188,510,0,0,0,2,3,0,0,0,0,0,-103,8166,8236,1,0,0,0,1,1,0,0,

0,0,0\*dce04286

表 7-164 L6MDCTYPE5 数据结构

| ID  | 字段               | 数据描述                                                                                               | 类型                          | 字节数         | 字节偏移      |
|-----|--------------------|--------------------------------------------------------------------------------------------------------|-------------------------------|----------------|---------------|
|   1 |  L6MDCTYPE5 header | 消息头，二进制消息头结构请 参考[表 7-50](#_bookmark210)，ASCII 消息头结构请参考[表7-51](#_bookmark211) |                               |   H1           |   0           |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头结 构参考[表7-160](#_bookmark403)                                               |                               |  H2            |  H1           |
|   3 |   PhaseBias        |   相位偏差数据                                                                                         | StL6PPPSat PhaseBias[ CorNum] |  H+28\*C orNum |   H(H1+H2)    |
|  4  |  Xxxx              |  32 位 CRC 校验                                                                                        |  HEX                          |  4             | H+28\*CorN um |
| 5   | [CR][LF]           | 语句结束符(仅 ASCII)                                                                                   |                               |                |               |

typedef struct

{

SHORT sPBias[7]; // USHORT usIndicator[7]; //

}_PACKED_StL6PPPSatPhaseBias;

#### L6MDCTYPE7 用户测距精度

本指令包含 QZSS MADOCA-PPP 信息类型 7，包含用户测距精度信息，详细可参考 QZSS L6 ICD 文件。命令输入仅支持 ONCHANGED 请求方式。

Message ID：2330 ASCII 输出语法：

L6MDCTYPE7A ONCHANGED

Binary 输出语法：

L6MDCTYPE7B ONCHANGED

适用产品：UM981、UB9A0、UM980消息输出：

\#L6MDCTYPE7A,89,GPS,FINE,2331,121691000,16071,0,18,30;36,4073,7,0,5,0,11,0,0

,2890,0,68,21,22,22,24,21,21,23,22,23,22,24,24,23,21,21,24,22,22,21,22,23,23,22,22,22,

22,22,26,26,25,26,27,27,26,26,26,26,27,27,27,26,26,26,26,27,26,25,24,24,24,25,24,24,24

,24,24,23,24,25,24,25,24,24,24,24,24,33,32,0,0,0,0,0,0,0,0,0,0,0,0\*98499c0d

表 7-165 L6MDCTYPE7 数据结构

| ID  | 字段               | 数据描述                                                                                              | 类型        | 字节数 | 字节偏移  |
|-----|--------------------|-------------------------------------------------------------------------------------------------------|-------------|--------|-----------|
|   1 |  L6MDCTYPE7 header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构 请参考[表7-51](#_bookmark211) |             |   H1   |   0       |
|  2  |  L6Corrheader      | L6 改正数消息头，消息头结构 参考[表7-160](#_bookmark403)                                              |             |  H2    |  H1       |
|  3  |  URA               |  用户测距精度数据                                                                                     |  ausURA[80] |  160   | H(H1+H2 ) |
| 4   | Xxxx               | 32 位 CRC 校验                                                                                        | HEX         | 4      | H+160     |

| ID | 字段     | 数据描述             | 类型 | 字节数 | 字节偏移 |
|----|----------|----------------------|------|--------|----------|
| 5  | [CR][LF] | 语句结束符(仅 ASCII) |      |        |          |

#### ENVINFO 环境信息

本指令用于输出基站所处环境的分值以及基站是否移动等信息。

基站打分的使用方法如下：

1.  将基站设置为 BASE 模式
2.  基站端请求 ENVINFO 并保存
3.  将基站放置在准备架设的位置上保持 30s 左右
4.  ENVINFO 中可显示当前环境位置的分值

    Message ID：11779 ASCII 输出语法：

    ENVINFOA 1

Binary 输出语法：

ENVINFOB 1

适用产品：UM980

消息输出：

\#ENVINFOA,84,GPS,FINE,2302,466453000,0,0,18,23;88,90.00,89,92,0,0,0.118,NARRO W_INT,53,51,0.022,46,44,50,56,0,0,0,25751,0.0027,0.432,0.385,0,0,0.000,0.007\*803048db

表 7-166 ENVINFO 数据结构

| ID  | 字段             | 数据描述                                                                                                      | 类型     | 字节数 | 字节偏移 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------|----------|--------|----------|
|   1 |   ENVINFO header | 消息头，二进制消息头结构请参考[表7-50](#_bookmark210)，ASCII 消息头结构请 参考[表7-51](#_bookmark211)         |          |   H    |   0      |
|   2 |   Base Score     | 基站所处环境的好坏（适用于 BASE 模式），更多信息见[表](#_bookmark416) [7-167 基站打分分值标准](#_bookmark416) |   USHORT |   2    |   H      |

| ID     | 字段                         | 数据描述                                                                                                                      | 类型      | 字节数 | 字节偏移  |
|--------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------|--------|-----------|
|  3     | Confidence level of solution | 解的置信度 （适用于 ROVER 模式）                                                                                              |  DOUBLE   |  8     |  H+2      |
|  4     |  Sat vis                     | 卫星可视率 （适用于 ROVER 模式）                                                                                              |  USHORT   |  2     |  H+10     |
|  5     |  Sat Slo                     | 卫星参与解算率 （适用于 ROVER 模式）                                                                                          |  USHORT   |  2     |  H+12     |
|      6 |      Moved Flag              | 是否移动过： 0：未移动； 1：和断电前相比或者上电过程中有过移动； 2：此功能不可用（由于环境太差或者位置偏差过大导致无法判 断） |      CHAR |      1 |      H+14 |
|   7    |   Moving Flag                | 是否在移动： 0：静止 1：正在移动                                                                                              |   CHAR    |   1    |   H+15    |
|  8     |  Pos Diff                    | 当前位置与固定坐标的距离；若 为非基站模式，该字段值为 0                                                                       |  DOUBLE   |  8     |  H+16     |
| 9      | Slo Type                     | 解的状态                                                                                                                      | ENMU      | 4      | H+24      |
| 10     | Base sat Num                 | 基站收到的卫星数                                                                                                              | INT       | 4      | H+28      |
| 11     | Pub sat Num                  | 基站和移动站的共视卫星数                                                                                                      | INT       | 4      | H+32      |
| 12     | 保留字段，共占 78 个字节     | 78                                                                                                                            | H+36      |        |           |
| 13     | XXXX                         | 32 位 CRC 校验                                                                                                                | Hex       | 4      | H+114     |
| 14     | [CR][LF]                     | 语句结束符（仅 ASCII）                                                                                                        | -         | -      | -         |

表 7-167 基站打分分值标准

| 分值    | 基站应用判断标准 |
|---------|------------------|
| 90\~100 | 优秀             |

| 分值   | 基站应用判断标准 |
|--------|------------------|
| 85\~90 | 较优             |
| 80\~85 | 一般             |
| 1\~80  | 不适合建站       |

# 其它指令

### Unlog 停止串口输出

本指令用于停止串口输出特定的数据信息。可配置参数[语句]停止输出对应的数据信息；可配置参数[端口]，停止端口输出。若无指定端口，一般默认为当前接收该指令的端口；如果没有指定消息名称，将停止所有信息输出。

命令格式为：

UNLOG [port] [message]

简化ASCII 语法：

UNLOG 对当前串口停止输出所有的信息 UNLOG GPGGA 对当前串口停止输出 GPGGA 语句 UNLOG COM1 停止com1 所有的信息输出 UNLOG COM2 GPGGA 停止com2 输出的 GPGGA 语句

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 8-1 Unlog 指令参数

| 指令头  | 端口号         | 描述                   |
|---------|----------------|------------------------|
|   UNLOG | COM1 COM2 COM3 |   将停止输出的信息名称 |

### Freset 清除 NVM 中的数据并重新启动接收机

本指令清除所有储存于非易失性存储器中的用户特定配置和卫星星历、位置信息，串口波特率变为 115200bps。该指令将强制接收机重启。

命令格式为：

FRESET

简化ASCII 语法：

FRESET

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 8-2 Freset 指令参数

| 指令头  | 指令参数 | 描述                                                                  |
|---------|----------|-----------------------------------------------------------------------|
|  FRESET |  -       | 清除保存的接收机设置、卫星星历、位置信 息等，串口波特率变为 115200bps |

### Reset 重启接收机

本指令用于使接收机重启，也可重启接收机同时清除保存在接收机中的卫星星历、位置信息、卫星历书、电离层和 UTC 参数等数据。

命令格式为：

RESET [参数]

简化ASCII 语法：

RESET

RESET EPHEM

RESET EPHEM ALMANAC IONUTC POSITION XOPARAM RESET ALL

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、

UM982、UMD982

表 8-3 Reset 指令参数

| 指令头        | 指令参数              | 描述                                                     |
|---------------|-----------------------|----------------------------------------------------------|
|         RESET | -                     | 重启接收机                                               |
|               | EPHEM                 | 重启接收机，清除保存的卫星星历                           |
|               | IONUTC                | 重启接收机，清除电离层和 UTC 参数                        |
|               | ALMANAC               | 重启接收机，清除历书                                     |
|               | POSITION              | 重启接收机，清除位置                                     |
|               | XOPARAM 或 CLOCKDRIFT |  重启接收机，清除模组晶振参数                            |
|               |  ALL                  | 重启接收机，清除以上所有信息，XOPARAM 或 CLOCKDRIFT 除外 |

-   在使用过程中，如果接收机需要进行模拟信号与实际信号的切换，建议清除接收机的星历

    （EPHEM）、历书（ALMANAC）、电离层和 UTC 参数（IONUTC）以及接收机位置

    （POSITION），否则接收机可能会出现不定位或定位异常现象。

-   在天线与射频链路没有异常的情况下，若模组在使用过程中出现长时间无法正常定位，可以使用 XOPARAM 或 CLOCKDRIFT 指令将模组内部存储的晶振参数删除重新进行收敛。

### Saveconfig 保存用户配置至非易失性存储器（NVM）

本指令将当前的用户配置保存到非易失性存储器（NVM）中，包括 LOG（触发器为 ONCE 的除外）、端口配置等。

命令格式为：

SAVECONFIG

简化ASCII 语法：

SAVECONFIG

适用产品：UM960、UMD960、UM960L、UM980、UMD980、UB9A0、UBD9A0、 UM982、UMD982

表 8-4 Saveconfig 指令参数

| 指令头     | 指令参数 | 描述                                  |
|------------|----------|---------------------------------------|
| SAVECONFIG | -        | 保存用户配置到非易失性存储器（NVM）中 |

# 附录 1：32 位 CRC 校验

ASCII 和二进制格式的 log 消息都包含 32 位 CRC 校验, 以进一步确保数据的发送和接收。下面提供生成 CRC 校验位的 C 语言示例：

const ULONG aulCrcTable[256] =

{

0x00000000UL, 0x77073096UL, 0xee0e612cUL, 0x990951baUL, 0x076dc419UL,

0x706af48fUL,

0xe963a535UL, 0x9e6495a3UL, 0x0edb8832UL, 0x79dcb8a4UL, 0xe0d5e91eUL, 0x97d2d988UL,

0x09b64c2bUL, 0x7eb17cbdUL, 0xe7b82d07UL, 0x90bf1d91UL, 0x1db71064UL, 0x6ab020f2UL,

0xf3b97148UL, 0x84be41deUL, 0x1adad47dUL, 0x6ddde4ebUL, 0xf4d4b551UL, 0x83d385c7UL,

0x136c9856UL, 0x646ba8c0UL, 0xfd62f97aUL, 0x8a65c9ecUL, 0x14015c4fUL,

0x63066cd9UL,

0xfa0f3d63UL, 0x8d080df5UL, 0x3b6e20c8UL, 0x4c69105eUL, 0xd56041e4UL,

0xa2677172UL,

0x3c03e4d1UL, 0x4b04d447UL, 0xd20d85fdUL, 0xa50ab56bUL, 0x35b5a8faUL, 0x42b2986cUL,

0xdbbbc9d6UL, 0xacbcf940UL, 0x32d86ce3UL, 0x45df5c75UL, 0xdcd60dcfUL, 0xabd13d59UL,

0x26d930acUL, 0x51de003aUL, 0xc8d75180UL, 0xbfd06116UL, 0x21b4f4b5UL,

0x56b3c423UL,

0xcfba9599UL, 0xb8bda50fUL, 0x2802b89eUL, 0x5f058808UL, 0xc60cd9b2UL, 0xb10be924UL,

0x2f6f7c87UL, 0x58684c11UL, 0xc1611dabUL, 0xb6662d3dUL, 0x76dc4190UL,

0x01db7106UL,

0x98d220bcUL, 0xefd5102aUL, 0x71b18589UL, 0x06b6b51fUL, 0x9fbfe4a5UL, 0xe8b8d433UL,

0x7807c9a2UL, 0x0f00f934UL, 0x9609a88eUL, 0xe10e9818UL, 0x7f6a0dbbUL,

0x086d3d2dUL,

0x91646c97UL, 0xe6635c01UL, 0x6b6b51f4UL, 0x1c6c6162UL, 0x856530d8UL,

0xf262004eUL,

0x6c0695edUL, 0x1b01a57bUL, 0x8208f4c1UL, 0xf50fc457UL, 0x65b0d9c6UL,

0x12b7e950UL,

0x8bbeb8eaUL, 0xfcb9887cUL, 0x62dd1ddfUL, 0x15da2d49UL, 0x8cd37cf3UL, 0xfbd44c65UL,

0x4db26158UL, 0x3ab551ceUL, 0xa3bc0074UL, 0xd4bb30e2UL, 0x4adfa541UL, 0x3dd895d7UL,

0xa4d1c46dUL, 0xd3d6f4fbUL, 0x4369e96aUL, 0x346ed9fcUL, 0xad678846UL, 0xda60b8d0UL,

0x44042d73UL, 0x33031de5UL, 0xaa0a4c5fUL, 0xdd0d7cc9UL, 0x5005713cUL,

0x270241aaUL,

0xbe0b1010UL, 0xc90c2086UL, 0x5768b525UL, 0x206f85b3UL, 0xb966d409UL,

0xce61e49fUL,

0x5edef90eUL, 0x29d9c998UL, 0xb0d09822UL, 0xc7d7a8b4UL, 0x59b33d17UL, 0x2eb40d81UL,

0xb7bd5c3bUL, 0xc0ba6cadUL, 0xedb88320UL, 0x9abfb3b6UL, 0x03b6e20cUL, 0x74b1d29aUL,

0xead54739UL, 0x9dd277afUL, 0x04db2615UL, 0x73dc1683UL, 0xe3630b12UL,

0x94643b84UL,

0x0d6d6a3eUL, 0x7a6a5aa8UL, 0xe40ecf0bUL, 0x9309ff9dUL, 0x0a00ae27UL, 0x7d079eb1UL,

0xf00f9344UL, 0x8708a3d2UL, 0x1e01f268UL, 0x6906c2feUL, 0xf762575dUL,

0x806567cbUL,

0x196c3671UL, 0x6e6b06e7UL, 0xfed41b76UL, 0x89d32be0UL, 0x10da7a5aUL, 0x67dd4accUL,

0xf9b9df6fUL, 0x8ebeeff9UL, 0x17b7be43UL, 0x60b08ed5UL, 0xd6d6a3e8UL, 0xa1d1937eUL,

0x38d8c2c4UL, 0x4fdff252UL, 0xd1bb67f1UL, 0xa6bc5767UL, 0x3fb506ddUL, 0x48b2364bUL,

0xd80d2bdaUL, 0xaf0a1b4cUL, 0x36034af6UL, 0x41047a60UL, 0xdf60efc3UL, 0xa867df55UL,

0x316e8eefUL, 0x4669be79UL, 0xcb61b38cUL, 0xbc66831aUL, 0x256fd2a0UL, 0x5268e236UL,

0xcc0c7795UL, 0xbb0b4703UL, 0x220216b9UL, 0x5505262fUL, 0xc5ba3bbeUL,

0xb2bd0b28UL,

0x2bb45a92UL, 0x5cb36a04UL, 0xc2d7ffa7UL, 0xb5d0cf31UL, 0x2cd99e8bUL, 0x5bdeae1dUL,

0x9b64c2b0UL, 0xec63f226UL, 0x756aa39cUL, 0x026d930aUL, 0x9c0906a9UL,

0xeb0e363fUL,

0x72076785UL, 0x05005713UL, 0x95bf4a82UL, 0xe2b87a14UL, 0x7bb12baeUL,

0x0cb61b38UL,

0x92d28e9bUL, 0xe5d5be0dUL, 0x7cdcefb7UL, 0x0bdbdf21UL, 0x86d3d2d4UL, 0xf1d4e242UL,

0x68ddb3f8UL, 0x1fda836eUL, 0x81be16cdUL, 0xf6b9265bUL, 0x6fb077e1UL, 0x18b74777UL,

0x88085ae6UL, 0xff0f6a70UL, 0x66063bcaUL, 0x11010b5cUL, 0x8f659effUL, 0xf862ae69UL,

0x616bffd3UL, 0x166ccf45UL, 0xa00ae278UL, 0xd70dd2eeUL, 0x4e048354UL,

0x3903b3c2UL,

0xa7672661UL, 0xd06016f7UL, 0x4969474dUL, 0x3e6e77dbUL, 0xaed16a4aUL,

0xd9d65adcUL,

0x40df0b66UL, 0x37d83bf0UL, 0xa9bcae53UL, 0xdebb9ec5UL, 0x47b2cf7fUL, 0x30b5ffe9UL,

0xbdbdf21cUL, 0xcabac28aUL, 0x53b39330UL, 0x24b4a3a6UL, 0xbad03605UL, 0xcdd70693UL,

0x54de5729UL, 0x23d967bfUL, 0xb3667a2eUL, 0xc4614ab8UL, 0x5d681b02UL,

0x2a6f2b94UL,

0xb40bbe37UL, 0xc30c8ea1UL, 0x5a05df1bUL, 0x2d02ef8dUL

};

// Calculate and return the CRC for usA binary buffer ULONG CalculateCRC32(UCHAR \*szBuf, INT iSize)

{

int iIndex;

ULONG ulCRC = 0;

for (iIndex=0; iIndex\<iSize; iIndex++)

{

ulCRC = aulCrcTable[(ulCRC \^ szBuf[iIndex]) & 0xff] \^ (ulCRC \>\> 8);

}

return ulCRC;

}

# 附录 2：RTCM V3 差分电文

RTCM 委员会推荐的 GNSS (Global Navigation Satellite Systems) 差分信息标准 Version 3,当前支持 3.0 和 3.2 的一些信息，请参见<http://www.rtcm.org/overview.php>。

本指令输出遵循 RTCM 标准格式，包括 1004，1006，1007，1012，1019，1033， 1104 等电文，被定义为 RTCM1004，RTCM1006，RTCM1007，RTCM1012，RTCM1019， RTCM1033 和 RTCM1104 等。

消息请求方法：

RTCM 消息号[请求频率]

例如：

RTCM1005 1 //按 1Hz 输出 RTCM1005 消息 RTCM1033 1 //按 1Hz 输出 RTCM1033 消息

RTCM1019 60 //每 60s 输出一次 RTCM1019 消息 RTCM1074 0.2 //按 5Hz 输出 RTCM1074 消息

支持的 RTCM V3 消息如下:

Group 1 –观测值:

RTCM1001 GPS RTK L1 观测值 RTCM1002 扩展的 GPS RTK L1 观测值 RTCM1003 GPS RTK L1 和 L2 观测值

RTCM1004 扩展的 GPS RTK L1 和 L2 观测值

RTCM1009 GLONASS RTK L1 观测值 RTCM1010 扩展的 GLONASS RTK L1 观测值 RTCM1011GLONASS RTK L1 和 L2 观测值

RTCM1012 扩展的 GLONASS RTK L1 和 L2 观测值

RTCM1074 GPS MSM4（全部伪距、载波和 CNR 观测值） RTCM1075 GPS MSM5（全部伪距、载波、多普勒和 CNR 观测值）

RTCM1084 GLONASS MSM4（全部伪距、载波和 CNR 观测值） RTCM1085 GLONASS MSM5（全部伪距、载波、多普勒和 CNR 观测值）

RTCM1123 BDS MSM3（北斗伪距和相位伪距信息） RTCM1124 BDS MSM4（全部伪距、载波和 CNR 观测值）

RTCM1125 BDS MSM5（全部伪距、载波、多普勒和 CNR 观测值） RTCM1126 BDS MSM6（完整北斗伪距，相位伪距及 CNR（高精度解算））

RTCM1127 BDS MSM7（完整北斗伪距，相位伪距，相位伪距速率及 CNR（高精度解算））

RTCM1104BDS RTK 观测值（国内行业定义，不可与国外其它产品混用）

Group 2 –基准站坐标:

RTCM1005 RTK 基准站天线参考点坐标（ARP） RTCM1006 RTK 基准站天线参考点坐标（含天线高）

Group 3 –基准站天线描述:

RTCM1007 天线描述和安装信息（当前仅支持编码）

Group 4 –辅助信息:

RTCM63 BDS 星历（测试电文） RTCM1042 BDS 星历 RTCM1019 GPS 星历 RTCM1020 GLONASS 星历 RTCM1045 GALILEO F/NAV 星历 RTCM1046 GALILEO I/NAV 星历

RTCM1033 接收机与天线说明

RTCM1105 内部定向应用，定向端向移动基站端传送定向信息（和芯星通自定义）

# 附录 3：EVENT 输出

### EVENTFLAG EVENT 位置信息

本 指 令 输 出 EVENT 发 生 时 刻 的 精 确 绝 对 时 间 及 相 对 时 间 。 支 持 ASCII/ABBASCII/BINARY 格式，支持 once 和 onchanged 输出。EVENTFLAG 指令必须配合输出 GGA 使用。

Message ID：312

命令格式为：

EVENTFLAG [参数]

简化ASCII 语法： EVENTFLAGB ONCHANGED EVENTFLAGA ONCHANGED

适用产品：UM980、UMD980、UB9A0、UM982、UMD982

消息示例：

\#EVENTFLAGA,97,GPS,FINE,2227,210352000,0,0,18,0;2,43,0,0,2227,210351,999532 091,0,-1,-1\*405dd7fe

表 0- 1 EVENTFLAG 数据结构

| ID     | 类型                 | 数据描述                                                                                                                                                                                                                    | 类型   | 字节数 | 字节偏移 |
|--------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
|      1 |     EVENTFLAG header | Log 头，参考[表 7-50 二进制](#_bookmark210)[数据格式 Header（头）结构](#_bookmark210)和[表 7-51 ASCII 数据格式](#_bookmark211) [Header（头）结构](#_bookmark211) 注： Header 部分的时间由 EVENT 触发时刻经过四舍五 入后输出 |        |      H |      0   |
|  2     |  eventID             | 事件编码（Event 1 或 Event 2）                                                                                                                                                                                              |  UCHAR |  1     |  H       |
|  3     |  status\*            | 模组当前状态，详见[表 0- 2](#_bookmark431) [STATUS 字段比特位说明](#_bookmark431)                                                                                                                                           |  UCHAR |  1     |  H+1     |
| 4      | Reserved             | 保留                                                                                                                                                                                                                        | UCHAR  | 1      | H+2      |
| 5      | Reserved             | 保留                                                                                                                                                                                                                        | UCHAR  | 1      | H+3      |
| 6      | week                 | 周                                                                                                                                                                                                                          | UINT   | 4      | H+4      |
| 7      | second               | 秒                                                                                                                                                                                                                          | UINT   | 4      | H+8      |
| 8      | subSecond            | 纳秒                                                                                                                                                                                                                        | UINT   | 4      | H+12     |
| 9      | Reserved             | 保留位                                                                                                                                                                                                                      |        | 4      | H+16     |
|    10  |    offset_second     | 按当前 GGA 输出频率， EVENT 时刻与最接近的 GGA输出的绝对时间之间的偏移值(second)。若该值无效， 则输出-1。                                                                                                                   |    INT |    4   |    H+20  |
|    11  |    offset_SubSecond  | 按当前 GGA 输出频率， EVENT 时刻与最接近的 GGA输出的绝对时间之间的偏移 (nanosecond) 。 若 该 值 无 效，则输出-1。                                                                                                           |    INT |    4   |    H+24  |

| ID  | 类型     | 数据描述                           | 类型 | 字节数 | 字节偏移 |
|-----|----------|------------------------------------|------|--------|----------|
|  12 |  xxxx    | 32 位 CRC 校验(仅 ASCII 和 二进制) |  Hex |  4     |  H+28    |
| 13  | [CR][LF] | 语句结束符(仅 ASCII)               | -    | -      | -        |

\* 字段 3（status）：UM982 Build9669 及之后的版本支持

表 0- 2 STATUS 字段比特位说明

| 比特位 | 定义                           |
|--------|--------------------------------|
| Bit0   | 周内秒有效标志：0=无效；1=有效 |
| Bit1   | PPS 有效标志：0=无效；1=有效   |
| Bit2   | 保留位                         |
| Bit3   | 周有效标志：0=无效；1=有效     |
| Bit4   | 保留位                         |

### EVENTSLN EVENT 位置及时间信息

输出EVENT 发生时刻的时间、位置、速度以及解状态等详细信息。EVENTSLN 指令必须配合输出 GGA 使用。

Message ID：311

命令格式为：

EVENTSLN [参数]

简化ASCII 语法： EVENTSLNB ONCHANGED EVENTSLNA ONCHANGED

适用产品：UM980、UMD980、UB9A0、UM982、UMD982

消息示例：

\#EVENTSLNA,97,GPS,FINE,2227,210381000,0,0,18,0;2,43,0,0,2227,210380,9995320 81,0,-1,-1,SOL_COMPUTED,SINGLE,40.07896911523,116.23651480774,67.0271,-

8.4925,WGS84,1.7728,1.6873,4.7070,48,0.000,0.000,50,28,0,0,-0.009,-0.004,-

0.116\*8f231ab8

表 0- 3 EVENTSLN 数据结构

| ID     | 类型                | 数据描述                                                                                                                                                                                                                                            | 类型   | 字节数 | 字节偏移 |
|--------|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------|----------|
|      1 |     eventsln header | Log 头，参考[表 7-50 二进制数](#_bookmark210)[据格式 Header（头）结构](#_bookmark210)和[表](#_bookmark211) [7-51 ASCII 数据格式 Header](#_bookmark211) [（头）结构](#_bookmark211)； 注： Header 部 分 的 时 间 由 EVENT 触发时刻经过四舍五入后输出 |        |      H |      0   |
|  2     |  eventID            | 事件编码（Event 1 或Event 2）-- 目前仅支持 Event 1                                                                                                                                                                                                  |  UCHAR |  1     |  H       |
|  3     |  status\*           | 模组当前状态， 详见[表 0- 2](#_bookmark431) [STATUS 字段比特位说明](#_bookmark431)                                                                                                                                                                  |  UCHAR |  1     |  H+1     |
| 4      | Reserved            | 保留位                                                                                                                                                                                                                                              | UCHAR  | 1      | H+2      |
| 5      | Reserved            | 保留位                                                                                                                                                                                                                                              | UCHAR  | 1      | H+3      |
| 6      | Week                | 周                                                                                                                                                                                                                                                  | UINT   | 4      | H+4      |
| 7      | second              | 秒                                                                                                                                                                                                                                                  | UINT   | 4      | H+8      |
| 8      | subSecond           | 纳秒                                                                                                                                                                                                                                                | UINT   | 4      | H+12     |
| 9      | reserved2           | 保留                                                                                                                                                                                                                                                |        | 4      | H+16     |
|    10  |   offset_secon d    | 按当前 GGA 输出频率，EVENT时刻与最接近的 GGA 输出的绝对时间之间的偏移值( 单位： 秒)。若该值无效，则输出-1。                                                                                                                                         |    INT |    4   |    H+20  |

| ID    | 类型                | 数据描述                                                                                                     | 类型    | 字节数 | 字节偏移 |
|-------|---------------------|--------------------------------------------------------------------------------------------------------------|---------|--------|----------|
|    11 |   offset_subSe cond | 按当前 GGA 输出频率，EVENT时刻与最接近的 GGA 输出的绝对时间之间的偏移值(单位：纳 秒)，若该值无效，则输出-1。 |    INT  |    4   |    H+24  |
| 12    | sol status          | 解算状态，参考[表 0- 5 解的状](#_bookmark435) [态](#_bookmark435)                                            | Enum    | 4      | H+28     |
| 13    | pos type            | 位置类型（参考[表 0- 4 位置或](#_bookmark434) [速度类型](#_bookmark434)）                                    | Enum    | 4      | H+32     |
| 14    | Lat                 | 纬度，deg                                                                                                    | Double  | 8      | H+36     |
| 15    | lon                 | 经度，deg                                                                                                    | Double  | 8      | H+44     |
| 16    | hgt                 | 海拔高，m                                                                                                    | Double  | 8      | H+52     |
|  17   |  undulation         | 大地水准面差距 - 大地水准面和 WGS84 椭球面之间的关系，m                                                      |  Float  |  4     |  H+60    |
| 18    | datum id\#          | 坐标系 ID，当前仅支持 WGS84                                                                                  | Enum    | 4      | H+64     |
| 19    | lat σ               | 纬度标准差，m                                                                                                | Float   | 4      | H+68     |
| 20    | lon σ               | 经度标准差，m                                                                                                | Float   | 4      | H+72     |
| 21    | hgt σ               | 高度标准差，m                                                                                                | Float   | 4      | H+76     |
| 22    | stn id              | 基站 ID                                                                                                      | Char[4] | 4      | H+80     |
| 23    | diff_age            | 差分龄期，s                                                                                                  | Float   | 4      | H+84     |
| 24    | sol_age             | 解的龄期，s                                                                                                  | Float   | 4      | H+88     |
| 25    | \#SVs               | 跟踪的卫星数                                                                                                 | Uchar   | 1      | H+92     |
| 26    | \#solnSVs           | 使用的卫星数                                                                                                 | Uchar   | 1      | H+93     |
| 27    | reserved            | 保留位                                                                                                       | Uchar   | 1      | H+94     |
| 28    | reserved            | 保留位                                                                                                       | Uchar   | 1      | H+95     |
|   29  |   EastVel           | 东向速度：地理坐标系下的东向速度，小数点后3 位，单位： Km/h(如无为空)                                        |   Float |   4    |   H+96   |

| ID   | 类型       | 数据描述                                                                 | 类型    | 字节数 | 字节偏移 |
|------|------------|--------------------------------------------------------------------------|---------|--------|----------|
|   30 |   northVel | 北向速度：地理坐标系下的北 向速度，小数点后3 位，单位： Km/h(如无为空)   |   Float |   4    |   H+100  |
|   31 |   upVel    | 天向速度：地理坐标系下的天顶向速度，小数点后 3 位，单 位：Km/h(如无为空) |   Float |   4    |   H+104  |
|  32  |  xxxx      | 检验位： 32 位 CRC 校验( 仅 ASCII 和二进制)                              |  Hex    |  4     |  H+108   |
| 33   | [CR][LF]   | 语句结束符(仅 ASCII)                                                     |         |        |          |

\* 字段 3（status）：UM982 Build9669 及之后的版本支持

表 0- 4 位置或速度类型

| 十进制 | ASCII            | 描述                         |
|--------|------------------|------------------------------|
| 0      | NONE             | 无解                         |
| 1      | FIXEDPOS         | 位置由 FIX POSITION 命令指定 |
| 2      | FIXEDHEIGHT      | 暂不支持                     |
| 8      | DOPPLER_VELOCITY | 速度由即时多普勒信息导出     |
| 16     | SINGLE           | 单点定位                     |
| 17     | PSRDIFF          | 伪距差分解                   |
| 18     | SBAS             | SBAS 定位                    |
| 32     | L1_FLOAT         | L1 浮点解                    |
| 33     | IONOFREE_FLOAT   | 消电离层浮点解               |
| 34     | NARROW_FLOAT     | 窄巷浮点解                   |
| 48     | L1_INT           | L1 固定解                    |
| 49     | WIDE_INT         | 宽巷固定解                   |
| 50     | NARROW_INT       | 窄巷固定解                   |
| 52     | INS              | 纯惯导定位解                 |

| 十进制 | ASCII          | 描述                           |
|--------|----------------|--------------------------------|
| 53     | INS_PSRSP      | 惯导与单点定位组合解           |
| 54     | INS_PSRDIFF    | 惯导与伪距差分定位组合解       |
| 55     | INS_RTKFLOAT   | 惯导与载波相位差分浮点解组合解 |
| 56     | INS_RTKFIXED   | 惯导与载波相位差分固定解组合解 |
| 68     | PPP_CONVERGING | PPP 状态收敛中                 |
| 69     | PPP            | PPP 定位                       |

表 0- 5 解的状态

| 解状态 | 描述             |                                         |
|--------|------------------|-----------------------------------------|
| 0      | SOL_COMPUTED     | 已解出                                  |
| 1      | INSUFFICIENT_OBS | 观测数据不足                            |
| 2      | NO_CONVERGENCE   | 无法收敛，输出解无效                    |
| 4      | COV_TRACE        | 协方差矩阵的迹超过最大值（迹\>1000 米） |

和芯星通科技（北京）有限公司

Unicore Communications, Inc.

北京市海淀区丰贤东路 7 号北斗星通大厦三层

F3, No.7, Fengxian East Road, Haidian, Beijing, P.R.China,

100094

[www.unicore.com](http://www.unicore.com/)

Phone: 86-10-69939800

Fax: 86-10-69939888

[info@unicorecomm.com](mailto:info@unicorecomm.com)

![](media/d511c0bc7096ec0fcb40ec2115ecf5d9.png)
