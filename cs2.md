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
	 - `changelevel de-ancient`
	 - `changelevel de_anubis`
	 - `changelevel de_assembly`
	 - `changelevel de_dust2` ⚔
	 - `changelevel de_inferno` ⚔
	 - `changelevel de_memento`
	 - `changelevel de-mills`
	 - `changelevel de_mirage` ⚔
	 - `changelevel de_nuke`
	 - `changelevel de_overpass` ⚔
	 - `changelevel de_thera`
	 - `changelevel de_vertigo`
	 - `changelevel de_train`