# IZUM - Priporočilni seznami za branje

![COBISS](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQMeLzYP5Rk0-rVINtYQzPESAtHSt1rvogTtg&s)

## Člani ekipe: 
- Adam Kac
- Gaja Gujt
- Tevž Starovasnik


## Kratka vizija: 
- Informacijska rešitev za priporočilne sezname branja, ki uporabnikom omogoča odkrivanje novih knjig na podlagi izposojenih knjig v slovenskih knjižnicah.📚🔍

## Namen informacijske rešitve: 
- Namen rešitve je omogočiti uporabnikom, da na podlagi izbrane knjige prejmejo priporočila za nadaljnje branje. Sistem vrne nekaj naslovov knjig (3 ali 5 COBISS-ID), ki so jih brali tudi drugi uporabniki, ki so brali izbrano knjigo. 📖

## Predvideni uporabniki:
- Vsi uporabniki, ki si izposojajo knjige v slovenskih knjižnicah preko sistema COBISS+ 👩‍💼
- Po iskanju gradiva se za naslov knjige, ki ga uporabnik poišče/izbere, izpiše seznam priporočenih knjig za branje 👨‍💼

## Glavne funkcionalnosti:
  - Po iskanju gradiva se za posameznega uporabnika, glede na zgodovino iskanja, izpiše seznam priporočenih knjig za branje. 🕵️‍♂️📑
  - Pri iskanju gradiva se ob kliku na gradivo, prikaže seznam priporočenih knjig za branje. 🛠️💾

## Predvideni uporabniški vmesniki:
- Spletni vmesnik za uporabnike sistema COBISS+ 🌐💻
- REST storitev za avtomatizirano pridobivanje priporočenih knjig 🌐🔄

## Tehnološki sklad:
| Java JDK                                                                                         | Wildfly strežnik                                                                 | Python                                                                                     | React                                                                                            | SQL                                                                                   |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| ![Java JDK](https://kinsta.com/wp-content/uploads/2023/01/Java-logo.png) |![Wildfly](https://www.tothenew.com/blog/wp-ttn-blog/uploads/2016/10/image00.png) | ![Python](https://www.python.org/static/community_logos/python-logo.png) | ![React](https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg) | ![SQL](https://d1.awsstatic.com/asset-repository/products/amazon-rds/1024px-MySQL.ff87215b43fd7292af172e2a5d9b844217262571.png) |


- **Backend:**
  - Java (uporablja strežnik Wildfly za izvajanje REST storitev)🌍🪰
  - Python za izdelavo algoritmov za priporočilni sistem 🐍

- **Frontend:**
  - Typescript (prikaz in uporabniški vmesnik) 🖥️
  
## Vhodni podatki 
- Vhod v sistem so izvoženi podatki vseh izposoj za zadnjih 5 let v vseh slovenskih knjižnicah z naslednjimi podatki za vsako izposojo: datum izposoje, COBISS-ID (id knjige), "hash" id člana, starost člana, UDK ⏳📅📊🔑

## Izhodni podatki: 
- Izhod sistema je seznam priporočil - 5 priporočenih knjig.

## Kako zagnati aplikacijo

### 1. Priprava okolja

Poskrbite, da imate nameščene naslednje tehnologije:
- Java JDK
- Wildfly strežnik
- Python
- SQL
- React
  
### 2. Nastavitev strežnika

1. Prenesite in namestite Wildfly strežnik. Sledite [uradni dokumentaciji](https://docs.wildfly.org/25/Getting_Started_Guide.html) za nastavitve potrebne za zagon strežnika.

### 3. Namestitev odvisnosti

Za backend:

```bash
# Premaknite se v mapo api1/src
# Namestite odvisnosti za Java projekte
```

Za frontend:

```bash
# Premaknite se v mapo api1/react/izum-cobiss in namestite npm odvisnosti
npm install
```

### 4. Zagon aplikacije

Zaženite backend storitve:

```bash
# Zaženite Wildfly strežnik
```

Zaženite frontend aplikacijo:

```bash
# Premaknite se v mapo api1/react/izum-cobiss
npm run dev
```

## Deployment
**Backend**
  - Java strežnik in mySQL podatkovna baza sta v Docker containerju, kateri je potem bil deploy-an na Render
  <img width="1715" alt="slika" src="https://github.com/adam8kac/IZUM/assets/132885507/039ce9ad-923f-4117-9082-d1bfb3d1613a">

  **Frontend**
  - React app je deploy-an na firebase-u
  <img width="972" alt="firebase2" src="https://github.com/adam8kac/IZUM/assets/132885507/ffc33acd-c9f9-4482-b02f-6af53a315f4e">

  **Arhitektura deploymenta**
  
  <img width="729" alt="fb3" src="https://github.com/adam8kac/IZUM/assets/132885507/36668f72-0ce4-49ee-8ec9-5ddbd40cd0e5">

  
  ## Najnovejša različica je na voljo: 
   - https://izum-c3093.web.app/



## Končni izgled aplikacije
![HomePage](https://github.com/adam8kac/IZUM/assets/115952277/d5a7990b-ab85-4c92-9b8d-7123c437f6b1)
![PordrobnostiOKnjigi](https://github.com/adam8kac/IZUM/assets/115952277/784b69c7-5d9a-443b-b047-e539a436c4f4)
![Profil](https://github.com/adam8kac/IZUM/assets/115952277/4c926789-9d98-4625-a914-16427487692a)
![Iskanje](https://github.com/adam8kac/IZUM/assets/115952277/0a60803f-ac11-41b6-8268-c0a4152c9cc4)



## Dokumentacija

- Vse knjige so dostopne na [COBISS+](https://plus.cobiss.net/cobiss/si/sl/bib/search) 📚
- [Java dokumentacija](https://docs.oracle.com/en/java/)
- [Wildfly dokumentacija](https://docs.wildfly.org/)
- [Python dokumentacija](https://docs.python.org/3/)
- [React dokumentacija](https://reactjs.org/)
- [SQL dokumentacija](https://dev.mysql.com/doc/)
---

🔧 **Potrebujete pomoč? Oglejte si našo dokumentacijo ali stopite v stik z nami.**
