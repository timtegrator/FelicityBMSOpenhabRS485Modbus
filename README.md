Some rough estimates what the registers might be. 

==============================================================
   FELICITY BMS – REGISTERMAP (Modbus Holding Registers)
==============================================================

--------------------------------------------------------------
 BATTERY INFO BLOCK (Start 0x1300 = 4864) – Länge 42 Register
--------------------------------------------------------------
REQUEST: 01 03 13 00 00 2A C0 91 
(01 Slave‑ID, 03 Function Code (Read Holding Registers), 13 00 Startadresse (4864), 00 2A Anzahl Register = 42, C0 91 CRC‑16)
Dec     Hex     Beschreibung                         Skalierung        Verified
4864    1300    Unbekannt                             -
4865    1301    Unbekannt                             -
4866    1302    Unbekannt                             -
4867    1303    -
4868    1304    -
4869    1305    -
4870    1306    Batteriespannung                      ×0.01 V         OK
4871    1307    Batteriestrom (signed)                ×0.1 A          OK
4872    1308    -
4873    1309    -
4874    1310    Batterietemperatur                    °C
4875    1311    SOC                                   %               OK
4876    1312    SOH                                   %
4877    1313    Zyklen                                -               OK
4878    1314    -
4879    1315    -
4880    1316    -
4881    1317    -
4882    1318    -
4883    1319    -
4884    131A    -
4885    131B    -
4886    131C    -
4887    131D    -
4888    131E    -
4889    131F    -
4890    1320    -
4891    1321    -
4892    1322    -
4893    1323    -
4894    1324    Unbekannt                             -
4895    1325    Unbekannt                             -
4896    1326    Max Cell Voltage (raw)                ×0.001 V       OK
4897    1327    Max Cell Index                        -
4898    1328    Min Cell Voltage (raw)                ×0.001 V       OK
4899    1329    Min Cell Index                        -
4900    132A    Cell Count                            -
4901    132B    -
4902    132C    NTC Count                             -
4903    132D    -
4904    132E    Temp (min/avg/max)                    °C
4905    132F    Temp (min/avg/max)                    °C


--------------------------------------------------------------
 CELL INFO BLOCK (Start 0x132A = 4906) – Länge 32 Register
--------------------------------------------------------------
REQUEST: 01 03 13 2A 00 20 61 5E
Dec     Hex     Beschreibung                         Skalierung        Verified
4906    132A    Max Cell Voltage (raw)                ×0.001 V
4907    132B    Max Cell Index                        -
4908    132C    Min Cell Voltage (raw)                ×0.001 V
4909    132D    Min Cell Index                        -
4910    132E    Temp Sensor 1                         °C               OK
4911    132F    Temp Sensor 2                         °C               OK
4912    1330    Temp Sensor 3                         °C               OK
4913    1331    Temp Sensor 4                         °C               OK

-- Zellspannungen (16 Zellen, je ×0.001 V)
4914    1332    Cell 1 Voltage                                         OK
4915    1333    Cell 2 Voltage                                         OK
4916    1334    Cell 3 Voltage                                         OK
4917    1335    Cell 4 Voltage                                         OK
4918    1336    Cell 5 Voltage                                         OK
4919    1337    Cell 6 Voltage                                         OK
4920    1338    Cell 7 Voltage                                         OK
4921    1339    Cell 8 Voltage                                         OK
4922    133A    Cell 9 Voltage                                         OK
4923    133B    Cell 10 Voltage                                        OK
4924    133C    Cell 11 Voltage                                        OK
4925    133D    Cell 12 Voltage                                        OK
4926    133E    Cell 13 Voltage                                        OK
4927    133F    Cell 14 Voltage                                        OK
4928    1340    Cell 15 Voltage                                        OK
4929    1341    Cell 16 Voltage                                        OK


--------------------------------------------------------------
 STATUS / LIMITS BLOCK (Start 0x2320 = 8992) – Länge 64 Register
--------------------------------------------------------------
REQUEST: 01 03 23 20 00 40 4E 74 
(01 Slave‑ID, 03 Read Holding Registers, 23 20 Startadresse (8992), 00 40 Anzahl Register = 64, 4E 74 CRC‑16)
Dec     Hex     Beschreibung                         Skalierung        Verified
8992    2320    Status                                -
8993    2321    -
8994    2322    Charge Limit (A×10)                   ×0.1 A
8995    2323    NTC Count                             -
8996    2324    Min Cell Voltage (raw)                ×0.001 V
8997    2325    Cell High Alarm                       ×0.001 V
8998    2326    Cell High Alarm Back                  ×0.001 V
8999    2327    -
9000    2328    -
9001    2329    Max Cell Voltage (Soll)               ×0.001 V        OK
9002    232A    95% SoC Voltage                       ×0.001 V        OK
9003    232B    5% SoC Voltage                        ×0.001 V        OK
9004    232C    Empty Voltage                         ×0.001 V        OK
9005    232D    Cell High Alarm                       ×0.001 V        OK
9006    232E    Temp High Alarm                       °C?
9007    232F    Temperatur                            °C
9008–9023        Diverse interne Werte                -

-- Temperatur-Rohwerte
9024    2360    Temp raw 1                            -
9025    2361    Temp raw 2                            -
9026    2362    Temp raw 3                            -
9027    2363    Temp raw 4                            -
9028    2364    Temp raw 5                            -
9029    2365    Temp raw 6                            -
9030    2366    Temp raw 7                            -
9031    2367    Temp raw 8                            -

-- Stromlimits
9032    2370    Charge Limit                          ×0.1 A
9033    2371    Charge Limit Back                     ×0.1 A
9034    2372    Discharge Limit                       ×0.1 A

9035–9055        Fehlerflags / Statusbits             -

==============================================================
