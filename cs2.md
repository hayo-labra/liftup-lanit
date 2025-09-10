# CS2-server

CS2-serverille on asennettu ja määritelty Linux Game Serverin CS2 -palvelin. 
## Komentorivi

Avaa palvelimella komentorivi (PowerShell / Windows Terminal) tai ota toistalta koneelta SSH-yhteys komennolla `ssh steam@192.168.1.10`. Käyttäjän salasana löytyy tunnuslistasta.

## Serverin päivitys

Tarkista ennen turnausta onko palvelimelle tullut päivitys komennolla `./cs2server update`. Tämä päivittää serverin uusimpaan versioon.

## Serverin konsoli

Serverin konsolinäkymän saat avattua komennolla `./cs2server console`. Avautuvaan konsoliin voi antaa ohjauskomentoja. Konsolista voi poistua näppäinyhdistelmällä `CTRL+B` ja `D`.

 - `mp_warmup_start` - Käynnistää kahden minuutin lämmittelyn.
 - `mp_warmup_end` - Lopettaa lämmittelyn ja aloittaa turnauksen.
 - `changelevel` - Vaihtaa turnauksessa pelattavan kentän. Valittavana on seuraavat kentät, ⚔-symbolilla merkityt ovat tasapainoisia kenttiä, muissa kentissä saattaa painottaa enemmän toista osapuolta.
	 - `changelevel de_ancient` (kilpailu)
	 - `changelevel de_anubis` (community)
	 - `changelevel de_dust2` ⚔ (kilpailu)
	 - `changelevel de_inferno` ⚔ (kilpailu)
	 - `changelevel de_mirage` ⚔ (kilpailu)
	 - `changelevel de_nuke` (kilpailu)
	 - `changelevel de_overpass` ⚔ (kilpailu)
	 - `changelevel de_vertigo` (community)
	 - `changelevel de_train` (kilpailu)
