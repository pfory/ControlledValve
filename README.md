# ControlledValve

- prepnu polaritu pomoci rele
- zapnu motor pomoci rele
- zresetuji promennou pro delku pulzu
- pokud do urcite doby neprijde impulz od rotacniho snimace tak vypnu proud do motoru
- pokud prijde impulz zresetuju promennou pro delku pulzu
- opakuji dokud do urcite doby neprijde impulz od rotacniho snimace - pak vypnu proud do motoru

Relé se spínají jedno po druhém
Každé relé lze zavřít/otevřít samostatně bez vazby na ostatní

Každý ventil potřebuje 3 relé, 2 pro přepínání polarity a jedno pro seputí napájení
pro 5 ventilů potřebuji tedy 5 výstupů pro spínání a 2 pro přepínání polarity
Pro každý ventil jsou zapotřebí 2 vstupy od snímače pulsů
Celkem 2+5=7 výstupů a 2x5=10 vstupů = 17 IO

ventil vodiče
GND
+5V
+12V k motoru
CLK
DT
datová 4 linka
silová 2 linka

ovládání bude z řídící jednotky soláru přes 2 vodiče
L L - vypnuto
H L - zavři
L H - otevři

V1 solár radiátor
V2 solár bojler vstup
V3 solár bojler výstup
V4 kamna bojler vstup
V5 kamna bojler výstup

Možné scénáře
1 - topím solárem do bojleru      V1C V2O V3O V4C V5C
Podmínka - solár topí
2 - topím kamny do bojleru        V1O V2C V3C V4O V5O
Podmínka - kamna topí
3 - topím solárem do radiátoru    V1O V2C V3C V4C V5C
Podmínka - Kamna i solár topí
O open
C Close


http://navody.arduino-shop.cz/navody-k-produktum/rotacni-enkoder-ky-040.html
