<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/esp32pcb/hodiny/blob/main/cas%20vecer.jpg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/esp32pcb/hodiny/blob/main/hodiny%20svitici%20light.jpg">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# HODINY NA MATICOVEM DISPLEJI RIZENE SNTP Z INTERNETU VERZE 2
## hodiny na led displeji 32x8 s max7219

Druha verze otevreneho projektu **Hodiny**, tentokrat postavena na mikrokontroleru **ESP32-S3 N16/R8** čímž se zvětšila jak FLASH na 16MB tak PS-RAM na 8 MB.
Rozmerove i funkcne je projekt stejny jako [prvni verze hodin](https://github.com/esp32pcb/hodiny) (ESP32-WROOM), meni se pouze pouzity modul a chip.
Je přidán ještě výstup pro piezo nebo jiný pípání když se bude nastavovat budík.
## UPOZORNENI
29.1.2026
- naflashujte si novy [firmware](https://github.com/esp32pcb/hodiny_v2/wiki/firmware)! 
## Funkce
- webove rozhrani pro nastavovani hodin.
- nastaveni wifi pomoci mobilni aplikace ESPTOUCH SMARTCONFIG. funguje take [ESP CONFIG](https://play.google.com/store/apps/details?id=com.techbot.smart_config)
- upgrade firmware pres OTA
- nastaveni intensity displeje podle okolniho svetla ( na to je tam ta ledka )
- cas je rizeny z SNTP
- datum a kdo ma svatek co 1 minutu
- pokud je pridan [senzor HDC1080](https://github.com/esp32pcb/hodiny/blob/main/senzorHDC1080_1.jpg) na I2C sbernici tak zobrazuje take teplotu a vlhkost
- stopky - [časomíra](https://youtu.be/6PLG5gm5gp4) 0-99s po milisekundách  

## Hardware
- ESP32-S3 (N16/R8)  
- LED displej matice  
- dioda pro mereni okolniho svetla  
- (volitelne) senzor **HDC1080** na I2C sbernici  
- přidán výstup pro ovládání pieza (počítá se s budíkem)

  ## wifi
- po spusteni hodin poprve je wifi prednastavena na SSID "IOT" a password "12345678".
  Pokud si nastavite mobilni hotspot s temito parametry tak se hodiny pripoji a zacnou ukazovat cas, datum a svatky.

  ## nastaveni wifi
- wifi se nastavuje pomoci aplikace ESPTOUCH SMARTCONFIG, ktera je jak pro android a tak pro iphone
- pripojite se mobilem na 2,4 Gb sit na ktere budou pripojeny take vase hodiny. Musi byt 2.4 Gb! 5Gb ESP neumi!

- Neni li v okoli znama wifi sit zustanou hodiny tmave a svítí led v pravém horním rohu. Pozdejsi verze uz maji napis "wifi?"
- stisknete tlacitko SW2 na dobu delsi nez 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite aplikaci ESPTOUCH SMARTCONFIG, vyplnite heslo k vasi wifi a stisknete connect.
- hned aktualizujte firmware pro nejnovejsi firmware.

  ## aktualizace firmware
Po připojení na WiFi si zkuste aktualizovat firmware.
Tlacitko SW1 držte déle než 5s a aktualizace se spustí.

## jak se dostat na webove rozhrani hodin
- po restartu hodin se na displeji ukaze IP adresa kde naleznete webove stranky hodin. napr. IP: 192.168.1.23.
- spustite svuj oblibeny webovy prohlizec a do adresniho radku zadate jenom 192.168.1.23.
- prohlizec sice nahlasi, ze stranky jsou nezabezpecene ale klidne se na ne pripojte.
- muzete si prochazet nastaveni (casem se budou pridavat funkce)
- naleznete tam take browser, kdo to umi muze si editovat webove stranky, napr menit barvy atd.
- pokud cokoliv zkazite tak si muzete znovu upgradovat firmware pomoci SW1 a stranky se obnovi do puvodniho stavu.

## vice informaci
- najdete na [WIKI](https://github.com/esp32pcb/hodiny_v2/wiki)
# kontakt
Marcel Juchelka
esp32hodiny@gmail.com
tel.: +420 733 255 252
