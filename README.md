# TizenTube FARA RECLAME (launcher)

Aplicație pentru televizoare Samsung (Tizen) care pornește serviciul de blocare a reclamelor
din [TizenTube](https://github.com/reisxd/TizenTube), închide orice instanță TizenTube pornită
fără serviciu, apoi deschide TizenTube. Workaround pentru
[reisxd/TizenTube#712](https://github.com/reisxd/TizenTube/issues/712).

Testat pe Samsung QE55Q80AATXXH (Tizen 6.0) cu TizenTube Cobalt v2.1.1.

## Instalare

Fișierul gata de instalat, `TizenTubeLauncher.wgt`, e în secțiunea **Releases**.

1. TizenTube Cobalt (`xvvl3S1TT1`) trebuie să fie deja instalat pe TV.
2. În Apps2Samsung → Settings: alege un certificat **Partner** (sau bifează
   „Always create new certificate”), activează „Force Samsung Certificate” și „Partner Signing”.
3. Release → Custom WGT File → `TizenTubeLauncher.wgt` → Install.
   Dacă apare `MISMATCHED_PRIVILEGE_LEVEL ... appmanager.kill`, certificatul folosit e încă de nivel public.
4. Pe TV deschide aplicația verde **„TizenTube FARA RECLAME”** în loc de TizenTube.

## Conținut

- `config.xml`, `index.html`: launcher-ul.
- `service/dist/index.js`: copie nemodificată a serviciului TizenTube v2.1.1 (GPL-3.0).

Fișierul `.wgt` e un zip simplu cu aceste fișiere, nesemnat; Apps2Samsung îl semnează la instalare.
Ca să-l refaci din sursă: `zip -r TizenTubeLauncher.wgt config.xml index.html icon.png icon_16b9.png service`
