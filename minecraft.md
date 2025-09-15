# Minecraft Build Battle -serveri

IP: 192.168.1.5/24

Minecraft Build Battle -serveri on rakennettu pterodactyl -asennuksen päälle. Palvelimelle on asennettu seuraavat palikat:
 - Purpur-server 
 - BuildBattle-plugin (BuildBattle-ympäristö)
 - LuckPerms-plugin  (oikeuksien jako)
 - WorldEdit-plugin (voi käyttää maailmojen rakentamiseen, WorldGuard vaatii toimiakseen)
 - WorldGuard-plugin (suojaa maailman tahattomalta rikkomiselta)

## Palvelimen käyttö

Avaa selaimessa pterodactyl paneeli osoiteesta http://192.168.1.5 ja kirjaudu sisään. Kirjauduttuasi sisään valitse paneelista minecraft server.

## Serverin käynnistys

Käynnistä serveri klikkaamalla paneelista start

## Serverin käyttö


## serverille liittyminen

pelaajat tarvitsevat minecraft version 1.21 Serverille liitytään minecraftin multiplayer kohdasta jossa lisätään severi ja annetaan osoiteeksi 192.168.1.5:25565.
### Pääkäyttäjän oikeuksien antaminen

Pelin sisällä pelaajalle voi antaa oikeudet vain jos pelaaja on jo serverillä. 
 - Pelin sisäinen komento on `/op pelaajanimi`. 
 - Konsolissa komento on `op pelaajanimi`.

### BuilbBattle -asetusten muokkaus

Asetuksissa pääset muokkaamaan mm. kuinka monta pelaajaa kilpailuun voi maksimissaan ja minimissään osallistua. Käyttäjällä tulee olla pääkäyttäjän oikeudet, anna ne tarvittaessa ennen.

Anna konsolissa komento `/bba setup edit liftup`. 

### Aiheiden vaihto

Kilpailun aiheet löytyvät *plugins/BuildBattle/themes.yml* -tiedostosta. Muokkaa aiheet haluamiksesi ja käynnistä palvelin uudelleen.

## Spectaaminen

Kun peli on käynnisssä, niin sinne liittyvä pelaaja on automaattisesti spectaaja.

## Serverin sammutus

Paina paneelissa stop nappia sammutaaksesi serverin.

## Kilpailun kulku

1. Pelialueelle liittyminen

   Jos pelaaja ei automaattisesti spawnaa pelialueelle, sinne liitytään komennolla `/bb join liftup`.

2. Kilpailuun liittyminen

   Pelialueelta löytyy kyltti. Kilpailuun liittyminen tapahtuu klikkaamalla oikealla näppäimellä kylttiä.

3. Rakennusteeman äänestys

   Pelaaja äänestää haluamaansa rakennusteemaa klikkaamalla aihetta. Eniten ääniä saanut teema voittaa.

4. Rakentaminen

   Pelaaja rakentaa teeman mukaisesti haluamansa rakennelman annetussa ajassa.

5. Voittajan äänestäminen

   Rakennusajan loputtua pelaajat arvioivat toistensa rakennelmat ottamalla käteen haluamansa blockin. Voittaja on se, joka sai parhaat arviot.

## Serverin ja pluginien päivitys

1. server-kansion varmuuskopiointi

   Ennen päivitystä tehdään varmuuskopio nykyisistä tiedostoista. Varmista, että server ei päällä, kun teet päivityksen.
  
   Tee kopio *paneelista backup kohdasta* ja anna sille nimeksi `server-backup-YYYYMMDD`. Esimerkiksi 17.10.2024 varmuuskopiokansion nimeksi tulisi `server-backup-20241017`.

2. Purpur-serverin päivitys
 
   Lataa uusin Purpur-serverin jar-tiedosto kotisivuilta https://purpurmc.org/, vie se työpöydällä olevaan *server*-kansioon.

   Muokkaa *server*-kansion `start.bat`-tiedoston komento viittaamaan uudempaan versioon.
  
   > Huomaa, että pluginit pitää päivittää samalla, kun serveri päivitetään.

3. Pluginien päivitys

   - Poista *server/plugins*-kansiossa olevat *jar*-tiedostot.
   - Lataa uusimmat versiot plugineista:
     - BuildBattle-plugin löytyy Spigotin sivuilta (https://www.spigotmc.org/resources/buildbattle-1-8.44703/).
     - LuckPerms-plugin löytyy sen omilta kotisivuilta (https://luckperms.net/).
     - WorldEdit-plugin löytyy EngineHubin sivuilta (https://enginehub.org/worldedit), kohdasta Go to downloads > Stable builds for Bukkit.
     - WorldGuard-plugin löytyy Bukkitin sivuilta (https://dev.bukkit.org/projects/worldguard).
   - Kopioi kaikki edellä lataamasi *jar*-tiedostot *server/plugins*-kansioon.

4. Päivitetyn version testaus

   Käynnistä server normaalisti ja testaa asennuksen toimivuus. 
