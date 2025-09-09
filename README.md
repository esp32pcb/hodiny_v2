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

## Funkce
- nastaveni WiFi pomoci mobilni aplikace **ESPTOUCH SMARTCONFIG** (funguje take **ESP CONFIG**)  
- upgrade firmware pres **OTA**  
- nastaveni intensity displeje podle okolniho svetla  
- cas je rizeny z **SNTP**  
- datum a kdo ma svatek kazdou 1 minutu  
- podpora senzoru **HDC1080** (teplota a vlhkost)  
- **stopky – casomira 0–99 s po milisekundach**  

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
- stisknete tlacitko S2 na dobu delsi nez 5 sekund. na displeji projede napis "mobil - start smart config"
- spustite aplikaci ESPTOUCH SMARTCONFIG, vyplnite heslo k vasi wifi a stisknete connect.
- hned aktualizujte firmware pro nejnovejsi firmware.

  ## aktualizace firmware
Po připojení na WiFi si zkuste aktualizovat firmware.
Tlacitko S1 držte déle než 5s a aktualizace se spustí.

# kontakt
Marcel Juchelka
esp32hodiny@gmail.com
tel.: +420 733 255 252
