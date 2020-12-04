# KIV/INS Informační systémy

## Creation Script for Target Tables

```sql
CREATE TABLE TRG_KATEDRY (
  KATEDRA_ID NUMERIC(16),
  KATEDRA_KOD VARCHAR(50) NOT NULL,
  KATEDRA_NAZEV VARCHAR(100),

  CONSTRAINT PK_TRG_KATEDRY PRIMARY KEY (KATEDRA_KOD)
);

CREATE TABLE TRG_HODNOCENI_DP (
  KATEDRA_KOD VARCHAR(50),
  OBOR_ID NUMERIC(10) NOT NULL,
  OBOR_NAZEV VARCHAR(55),
  HODNOCENI VARCHAR(50),

  CONSTRAINT PK_TRG_HODNOCENI_DP PRIMARY KEY (OBOR_ID),
  CONSTRAINT FK_KATEDRY_HONOCENI FOREIGN KEY (KATEDRA_KOD) REFERENCES TRG_KATEDRY (KATEDRA_KOD)
);
```

## Data

Export finálních dat z výstupních tabulek.

### TRG_KATEDRY

| KATEDRA\_ID | KATEDRA\_KOD | KATEDRA\_NAZEV                           |
| :---------- | :----------- | :--------------------------------------- |
| 52110       | KFY          | Katedra fyziky                           |
| 52130       | KMA          | Katedra matematiky                       |
| 52140       | KKY          | Katedra kybernetiky                      |
| 52120       | KME          | Katedra mechaniky                        |
| 52150       | KIV          | Katedra informatiky a výpočetní techniky |
| 52160       | KGM          | Katedra geomatiky                        |

### TRG_HODNOCENI_DP

| KATEDRA\_KOD | OBOR\_ID | OBOR\_NAZEV                                       | HODNOCENI |
| :----------- | :------- | :------------------------------------------------ | :-------- |
| KIV          | 2252     | Softwarové inženýrství                            | 2,25      |
| KGM          | 2309     | Geomatika                                         | 4         |
| KGM          | 2358     | Geomatika                                         | 1,875     |
| KKY          | 3808     | Automatické řízení a robotika                     | NULL      |
| KMA          | 2130     | Finanční informatika a statistika                 | 2,6667    |
| KMA          | 2172     | Finanční informatika a statistika                 | 2         |
| KKY          | 2389     | Kybernetika a řídicí technika                     | NULL      |
| KIV          | 2403     | Informatika                                       | 1,6667    |
| KIV          | 2404     | Výpočetní technika                                | 1         |
| KKY          | 2500     | Kybernetika a řídicí technika                     | 2         |
| KKY          | 3122     | Systémy pro identifikaci, bezpečnost a komunikaci | 1,6       |
| KIV          | 3526     | Počítačové systémy a sítě                         | 1         |
| KMA          | 3669     | Matematika a její aplikace                        | 3         |
| KIV          | 2166     | Softwarové inženýrství                            | 1,4727    |
| KIV          | 3102     | Informační systémy                                | 1,3809    |
| KMA          | 3672     | Matematika a finanční studia                      | 3         |
| KMA          | 3674     | Matematika a finanční studia                      | 1,6667    |
| KIV          | 4068     | Informatika                                       | 3         |
| KMA          | 2391     | Finanční informatika a statistika                 | 3         |
| KMA          | 2855     | Učitelství matematiky pro střední školy           | 2         |
| KKY          | 3121     | Počítačové řízení strojů a procesů                | 1,6       |
| KMA          | 3466     | Matematika a její aplikace                        | 1,6923    |
| KMA          | 3510     | Matematika a její aplikace                        | 1         |
| KKY          | 2174     | Kybernetika a řídicí technika                     | 1,5       |
| KMA          | 2206     | Matematika                                        | 1,1818    |
| KMA          | 2856     | Učitelství matematiky pro střední školy           | 1         |
| KME          | 3170     | Stavitelství                                      | 1         |
| KME          | 3288     | Stavitelství                                      | 1,75      |
| KIV          | 3525     | Medicínská informatika                            | 1,7272    |
| KMA          | 3559     | Matematika a finanční studia                      | 1,3333    |
| KGM          | 3671     | Strategické plánování měst a regionů              | NULL      |
| KIV          | 2239     | Výpočetní technika                                | 2         |
| KGM          | 2310     | Geomatika                                         | 3,5       |
| KGM          | 2392     | Geomatika                                         | 1,3333    |
| KMA          | 3024     | Matematika pro přírodní vědy                      | 2         |
| KME          | 3118     | Počítačové modelování                             | NULL      |
| KGM          | 3171     | Územní plánování                                  | 1         |
| KIV          | 3304     | Informační systémy                                | 1,6363    |
| KIV          | 479      | Informatika                                       | 1,6506    |
| KGM          | 2200     | Geomatika                                         | 1,5263    |
| KMA          | 3048     | Matematické výpočty a modelování                  | 1         |
| KKY          | 3123     | Inteligentní komunikace člověk - stroj            | 1,6667    |
| KKY          | 3310     | Řídicí a rozhodovací systémy                      | 1,125     |
| KMA          | 3560     | Matematika a finanční studia                      | NULL      |
| KKY          | 475      | Kybernetika a řídicí technika                     | 1,6       |
| KMA          | 2160     | Obecná matematika                                 | 2         |
| KMA          | 3012     | Matematika a finanční studia                      | 2         |
| KMA          | 3049     | Matematika a management                           | 3         |
| KIV          | 3188     | Informatika a výpočetní technika                  | NULL      |
| KIV          | 3529     | Počítačová grafika                                | 1         |
