# AJA-Tours-turisticka-agencija

	PROJEKTNA DOKUMENTACIJA I
UPUTSTVO ZA KORIŠTENJE WEB APLIKACIJE TURISTIČKA AGENCIJA “AJA Tours”

Članovi tima:

1. Aida Hondo,
2. Jasmina Gazija i
3. Almir Ustamujić



SADRŽAJ

Contents
SADRŽAJ	2
ARHITEKTURA WEB APLIKACIJE	3
UVOD	4
Opis realizirane aplikacije	4
Korisničke priče	5
Plan projekta - SCRUM METODOLOGIJA	7
SPRINT	7
Sprint planning	7
Sprint review	7
SPRINTOVI	9
DIJAGRAM BAZE	9
HEADER	10
LOGIN	11
FOOTER	13
POČETNA STRANICA	14
O NAMA	15
DESTINACIJE	16
USLOVI PUTOVANJA	17
KATALOZI	19
REZERVACIJE	20
KONTAKT	23
ADMIN PANEL	23


ARHITEKTURA WEB APLIKACIJE

Uvođenjem dinamičnosti u web, sve više govorimo o web aplikacijama umjesto o web stranicama.
Web aplikacija predstavlja aplikaciju kojoj se pristupa preko Internet mreže. To je kompjuterski program koji se odvija unutar web preglednika, a koji je pisan programskim kodom koji podržava web preglednike.
Web aplikacije su popularne zbog velike prisutnosti web preglednika i jednostavnih mogućnosti njihovog korištenja. Razlog njihove popularnosti je mogućnost ažuriranja i održavanja web aplikacija, bez potrebe za instalacijom aplikacije na hiljade potencijalnih računara korisnika. Također tu je i nasljeđena kompatibilnost za više različitih preglednika.

Aplikacija se sastoji iz tri logičke cijeline koje možemo nazvati razinama. Prvu razinu predstavlja web preglednik, drugu razinu predstavlja srednji sloj tj aplikacijska logika i treću razinu predstavlja pohrana, tj.baza podataka.
Web preglednik šalje zahtjev srednjem sloju, koji ga procesuira i šalje upit u bazu, ili radi odgovarajuću izmjenu baze i vraća odgovor.

Arhitektura web aplikacije predstavlja izbor suštinskih strukturnih elemenata koji će činiti jednu web aplikaciju. Prilikom izrade web aplikacije za AJA Tours koristili smo sljedeće tehnologije :
Frontend: HTML 5, CSS 3, JAVA SCRIPT, JQUERYY 1.10.2. i 1.10.3., ANGULAR 1.6.9. , BOOTSTRAP 3.3.7. , HOVER
Backend: PHP, .NET FRAMEWORK 4.5, RAZOR V3, 
Baza podataka: SQL, 
Alati: Visiual Studio 2017, SQL MANAGMENT STUDIO, COMPACT VIEW
NUGETS: Facebook, MicrosoftOwinSecurityAuth
API: Facebook, Google




UVOD

Turistička agencija se definiše kao subjekt trgovačkog prava, čija je osnovna djelatnost organizovanje prevoza, smještaja, izleta i drugih usluga za turiste.
Da bi se razmotrili potrebni aspekti za realizaciju aplikacije za turističku agenciju, potrebno je definisati poslove odnosno usluge koje se nalaze u ponudi turističke agencije.
Usluge turističke agencije za koju radimo aplikaciju su sljedeće:
- organiziranje, prodaja i provođenje paketa aranžmana
- prodaja i posredovanje u prodaji ugostiteljskih i turističkih usluga
- posredovanje u pružanju usluge putovanja i boravka
- prihvat i prevoz putnika
- rezervacija smještaja i druge usluge
- davanje turističkih obavjesti i drugih promotivnih materijala
Iz priloženog popisa proizilaze i potrebne funkcionalnosti aplikacije koju radimo.

Prednosti Interenta u poslovanju turističkih agencija:
- Internet je izuzetno napredan i isplativ medij promocije i prodaje
- vizualizacija prilikom promocije turističkih usluga putem mulitmedijalne tehnologije omogućava apsolutni prostorni doživljaj destinacija i svih usluga što znatno ostavlja bolji dojam od brošura i kataloga na klijenta.
- automatizacija omogućava prodaju na upit što znači da se istovremeno mogu prodati sve usluge, a ne samo ograničeni ugovoreni paket
- nemoguć je overbooking jer su uklonjeni svi komunikacijski problemi koji mogu biti uzrok overbooking-a.
- internet nudi neograničen marketinški prostor za promociju turističkih usluga
- informacije o turističkim ponudama na ovaj način mogu doprijeti do milionskih korisnika, što nije bilo moguće postići sa brošurama i katalozima.

Opis realizirane aplikacije

Uzevši u obzir potrebe turističke agencije, kao i zakonom propisane usluge koje agencija ima mogućnost nuditi, izradili smo logički model funkcionalnosti rastavljenih u module web aplikacije za upravljanje poslovanjem turističke agencije. Na ovaj način smo dobili sljedeće module:
1. Početna - index strana
2. Naš tim
3. Destinacije
4. Katalozi
5. Rezervacije
6. Kontakt
7. Registracija
8. Log-in
Korisničke priče

Korisnička priča	Uvjeti prihvatljivosti
Kao korisnik želim biti u mogućnosti mijenjati AJA kod	Unutar aplikacije mora biti omogućeno mijenjanje unešenog koda povlačenjem iz baze ili preko admin panela
Kao korisnik želim biti u mogućnosti dodati nove funkcionalnosti stranica	Unutar aplikacije korisniku mora biti omogućeno prilikom pritiska na određeno dugme pravilno proslijediti upisane podatke
Kao korisnik želim biti u mogućnosti urediti pojedinosti svakog dijela web aplikacije	Prilikom odabira ove mogućnosti u web aplikaciji se mora otvoriti popis sa svom strukturom, pritiskom na određeni dio otvara se novi zaslon gdje je moguće urediti konkretni dio stranice aplikacije
Kao korisnik želim biti u mogućnosti učitati informacije o svakom pojedinom dijelu koda	Nakon učitavanja koda aplikacija mora biti u stanju točno očitati kod i prikazati zajedno sa informacijama o konkretnoj stranici
Kao korisnik želim da se podaci sa web servisa ažuriraju te spreme lokalno	Prilikom pokretanja aplikacije podaci sa web servisa se moraju sinhronizirati sa podacima u lokalnoj bazi podataka
Kao korisnik želim biti mogućnosti dodati nove dijelove koda te urediti njihove osnovne značajke	Odabirom ove mogućnosti mora biti moguće unijeti osnovne podatke o novom kodu, nakon unešenih informacija moraju se spremiti na web servis
Tablica 1. Korisničke priče za projekat "AJA Tours” turističku agenciju


Red.
broj	NAZIV MODULA
Modul	PODMODULI
Submodul	Vrijeme potrebno za izvršavanje modula
Time estimate
1.	Registrovanje korisnika	1. Dodavanje, editovanje i brisanje korisnika: Ime i prezime, username, password, broj mobitela, e-mail	Jedan dan
Testiranje: jedan dan


2.	

Log-in i verifikacija korisnika 	
1. Provjera da li postoji korisnik
2. Ukoliko postoji korisnik, provjera permisija	Jedan dan
Testiranje: jedan dan


3.	

Rezervacija	1. Provjera da li je korisnik prijavljen
2. Ukoliko je prijavljen nuditi rezervaciju
3. Dodavanje, editovanje i brisanje rezervacija
4. Fiksiranje datuma za svaku ponudu destinacije
5. Odobravanje destinacije u admin panelu	Dva dana
Testiranje: jedan dan

4.	
Index strana	1. Video - Sarajevo promo
2. Top tri destinacije
3. Novosti iz svijeta turizma u vidu sladjera	Dva dana
Testiranje: jedan dan
5.	O nama	1. Predstavljanje tima
2. Slike i funkcije clanova tima
3. Kontakt linkovi za facebook, instagram 	Jedan dan
Testiranje: nije potrebno
6.	Destinacije 	1. Kreirati 8 destinacija
2. Kreirati datume polaska i povratka
3. Odabrati po 3 slike za svaku destinaciju	5 dana
Testiranje: 2 dana
7.	Katalog	1. Preuzeti i postaviti katalogsa ponudama destinacija  u pdf-u 	Jedan dan
Testiranje: nije potrebno
8.	Uslovi putovanja	Kreirati pravila i uslove putovanja sa agencijom	Jedan dan
Testiranje: nije potrebno
9.	Kontakt forma	Kreirati kontakt formu koja će popunjene podatke prosljedjivati na email agencije.	Jedan dan
Testiranje: jedan dan
10.	Kreirati header	Header treba sadržavati logo, navigaciju i linkove za login i registraciju.	Dva dana
Testiranje: jedan dan
11.	Kreirati footer	Footer treba sadržavati mapu lokacije, logo, naziv agencije, adresu, email i broj telefona	Jedan dan
Testiranje: jedan dan
12. 	Kreiranje baze podataka	Baza podataka treba da sadrži tabele: 
- Registrovani korisnici (ID, ime, prezime, username, password, email, broj telefona, create, edit, delete)
- Destinacije (ID, Naziv destinacije, dugi opis, kratki opis, trajanje putovanja, datum polaska, datum odlaska, cijena, 5 fotografija)
- Top tri destinacije (Naziv destinacije, trajanje putovanja, datum polaska, datum odlaska, cijena, jedna fotografija)
- Rezervacije (Ime, Prezime, E-mail, Destinacija-drop down meni sa destinacijama, Datum putovanja: datum polaska i datum povratka - fiksno, komentar)
	10 dana
Testiranje: 3 dana

Plan projekta - SCRUM METODOLOGIJA


Ljudski resursi: 
1 project menager: Aida Hondo,
 3 front-end developera: Jasmina Gazija, Aida Hondo, Almir Ustamujic, 
2 back-end developera: Jasmina Gazija, Almir Ustamujic 

Tehnologije koje će se koristiti prilikom izdrade aplikacije: 
JavaScript, Angular, JQuerry, Bootstrap, HTML, CSS, Bootstrap, SQL, ASP.net.
Predvidjeno trajanje izrade aplikacije 40 dana. Broj planiranih sprintova: 4.
SPRINT
Sprint planning
Na kraju svakog sprinta održan je sprint review gdje su bili prisutni članovi razvojnog tima, scrum master i vlasnik proizvoda. Na ovim sastancima SCRUM tim razgovarao je o završenim zadacima u proteklom sprintu te su se dodavale izmjene po potrebi. Ovo su bili sastanci koji su se održavali uživo ili putem mailova. U ovom su segmentu članovi SCRUM tima izjašnjavali o rješavanju pojedinih zadataka unutar sprinta, koji su se rješavali s blagom poteškoćom ali i lakoćom.
Sprint review
Nakon odrađenog Sprint Reviewa koji je trajao otprilike 45 minuta prelazi se na sprint planning u kojem se odlučuje koje će se sljedeće funkcionalnosti implementirati, kao i kod reviewa na sprint planningu bio je uključen cijeli SCRUM tim. U ovoj aktivnosti SCRUM tim procjenjuje koje će funkcionalnosti biti moguće za implementirati, kod ove aktivnosti, SCRUM tim (SCRUM master i razvojni tim) je određivao koje će funkcionalnosti biti moguće implementirati. Nakon dogovora članovi razvojnog tima su se dobrovoljno javljali za svaki pojedini zadatak, te im je dodjeljen pripadajući zadatak. Kao i sprint review ova aktivnost je trajala 30-45 minuta.
   
Daily meeting i slike koje potvrđuju timski rad 
Screenshoot daily meetinga:
		      
Slika1. i 2. dogovor u vezi nalaženja i zajedničkog rada na web aplikaciji

 
Slika 4. Korištenje Trello za organizaciju rada na web aplikaciji







SPRINTOVI

Redni br.	SPRINT	Opis sadržaja sprinta	Vrijeme sprinta


1.	

Sprint 1	   Task 1 : Modul 1 - Jasmina
Task 2 : Modul 2 - Aida
 Task 3 : Modul 7 - Almir
       Modul 10 - Almir
       Modul 11 - Almir
	

10 dana

2.	

Sprint 2	Task 4 : Modul 3 - Aida
      Modul 4 - Aida
      Modul 5 - Aida
  Task 5 : Modul 8 - Jasmina
	

10 dana

3.	
Sprint 3	  Task 6 : Modul 6 - Jasmina
Task 7 : Modul 9 - Almir
             Task 8 : Modul 12 - Jasmina, Almir, Aida	
10 dana












DIJAGRAM BAZE

 
Prikaz dijagrama StarterSite baze podataka


HEADER

Shodno knjizi grafičkih  standarda u dogovoru sa krajnjim klijentom odabrane su standrdizovane boje predstavljene u kodnom formatu # . Header koristi navedeni # format. U sebi sadrži logo agencije (u gornjem lijevom uglu), navigacijske trake (O nama, Destinacije, Katalozi, Rezervacije, Uslovi putovanja, Kontakt i Admin panel), polja za pretragu i dugmad (registracija i log in). 

 

Navigacijska traka je fiksirana na vrhu, a tipka Admin panel je sakrivena i pojavljuje se samo onda kada se uloguje admin korisnik. Pritiskom na sliku loga, vraća se na početnu stranicu.

 

Pritiskom na pretragu, pojavljuje se search bar i traka sa destinacijama. Search baru se može pristupiti sa svake stranice jer je fiksiran u navigaciji. Preko funkcije se filtriraju destinacije. Search bar se zatvara pritiskom na tipku “x”. Za izradu headera i navigacijskog bara za pretragu korišten CSS, bootstrap, javascript i angular (filter).

 

LOGIN

Ova stranica je jedna od unaprijed kreiranih stranica ako koristimo MVC Razor. Prilagođena je izgledom i formom ostalim stranicam s ciljem što kvalitetnijeg dizajna.
Prilikom klika na Login, u gornjem desnom ćošku svake stranice, ili odlaskom na stranicu Rezervacije, pristupa se Login stranici.
Također smo koristili bootstrapi formi 6-6. U lijevom dijelu je smještena login forma koja predviđa obavezna polja za unos podataka: email adresa (koja je ujedno i username), password, te potvrdu passworda. Tu je check box Upamti podatke, koji omogućava korisniku spremanje korisničkih podataka u svom browser-u.
Ispod se nalazi opcija Zaboravili ste password koja omogućava korisnicim koji su zaboravili svoj password da ga izmjene.
 
Slika: Zaboravili ste password
Sa desne strane nalazi se link za registraciju, ukoliko je riječ o korisniku koji još uvijek nije registrovan i na čiji klik se korisnik preusmjerava na stranicu Registracija.
Ispod se nalaze opcije uvidu dugmeta za prijavu, tj registraciju putem Facebook i Google servisa. 
Ove dvije funkcionalnosti su urađene tako što smo se registrovali kao developer na Facebook-u i Google-u te dobili svoju API kod. Postavili smo već unaprijed zadani html kod, preporučene skripte i instalirali zahtjevane nugete. Ova opcija nije funkcionalna u potpunosti jer zahjeva postavljanje aplikacije na hosting, te dostavljanje url linka Facebook i Google servisima.
 
Slika: Login stranica
Nakon uspješnog logovanja ili registracije, korisnik se preusmjerava na stranicu Rezervacije jer se predpostavlja da je cilj registracije ili prijave upravo pristup ovoj stranici. U gornjem desnom ćošku, na mjestu login opcije, se sada prikazuje Dobrodošli + korisničko ime, kao na slici ispod:

 
Slika: Potvrda prijave/registracije i poruka dobrodošlice
Također prilikom logovanja, radi se autentifikacija korisnika. Ukoliko je korisnik prepoznat kao administrator, prikazuje mu se ikonica za editovanje sadržaja u ulozi administratora u navigaciji.

 
Slika: Prikaz linka za AdminPanel korisniku koji je prepoznat kao administrator

U bazi su predviđene sljedeće tabele vezane za login i registraciju, te autentifikaciju korisnika: 
-	UserProfile (popunjavaju je korisnici koji su se registrovali putem registracijske forme na stranici Registracija),
-	Memebership (popunjavaju korisnici koji se registruju preko Facebook servisa), 
-	O.AuthMembership (popunjavaju korisnici koji se registruju preko Google servisa), 
-	Roles (IdRoles kolona sadrži id=1 za admina i id=2 za korisnika)
-	UsersInRole. (Povezuje UserProfile i Roles tabele, preko Id-a. IdUser-a se unosi i ukoliko je administrator dodjeljuje mu se IdRole=1, a ukoliko je korisnik dodjeljuje mu se IdRole=2 s napomenom da za obične korisnike nije potrebno raditi ovu dodjelu, već su automatski prepoznati kao korisnici.)

               
      Slika: Tabele u bazi                                     Slika: Tabela UserProfile


       
          Slika: Tabela Roles                              Slika: Tabela UsersInRoles                                           

FOOTER

Za pravljenje footera korišten bootstrap i hover css. U lijevom gornjem uglu smještena tipka “Povratak na vrh stranice”, Logo je smješten na desnoj strani, zajedno sa kontakt informacijama. Sa lijeve strane stavljena slika mape (pritiskom na nju otvara se Google map u novom prozoru). Pritiskom na mail adresu može se direkto iz futera poslati poruka (mail).

 

POČETNA STRANICA

Na početnoj stranici kao i u cijelokupnoj aplikaciji koristili smo kombinaciju plavih i bijelih tonova, koji podsjećaju na more i fanastičan odmor i podstiču posjetitelja da napravi rezervaciju.
Dizaj je vrlo jednostavan i pregledan, kako je i planirano te je pogodan za sve generacije, koje se vrlo jednostavno mogu snaći i pristupiti sadržaju kojem žele.
Urađena je tako da bude user friendly  zahvaljujući malom broju stavki na ekranu koje su pregledno raspoređene. Istaknute su nazivom, odvojene okvirom i svaka odmah jasno asocira na njihovu namjenu.
Odmah nakon header-a se nalazi promo video Sarajeva. Video je preuzet sa Youtube servisa. Odlučili smo se da ne koristimo opciju autoplay jer su mnoga istraživanja pokazala da ta opcija mnoge korisnike nervira zbog čega odlaze sa stranice. 
Također je za izradu main dijela korišten bootstrap. Video je smješten u jednom redu, unutar svih 12 kolona.
 
Slika: Index stranica - video
Ispod videa nalaze se top tri ponude destinacija koje su aktuelne.  Destinacije su također postavljene pomoću bootstrapa, u tri kolone.
Za svaku destinaciju prisutna je slika, na koju je primjenjen hover efekat (hvr-pop), gdje se prilikom primicanja miša aktivna slika blago zumira, a zatim vrati u prvobitnu veličinu.
Ispod slike se nalazi link sa nazivom destinacije, periodom planiranog putovanja, cijenom i link na kojem mogu saznati više o toj destinaciji.
 
Slika: Index stranica – top tri destinacije
Ispod destinacija se nalazi slideshow čiji sadržaj čine vijesti i novosti iz oblasti turizma. Slide show je urađen pomoću HTML-a i CSS-a, uz upotrebu funkcije u JavaScriptu (JQuery).
Sadrži 6 fotografija i naslova, koji su ujedno i linkovi kako bi se pročitalo nešto više o turističkim novostima.
Pozicioniran je pomoću bootstrapa u formi 2-8-2. Ova stranica je statičnog karaktera.

O NAMA
Na stranici O nama se nalaze osnovni podaci o članovima tima kao što su ime i prezime, slika, predviđena pozicija u agenciji te ikonice za kontaktiranje putem društvenih mreža, konkretno Facebook-a i Instagrama.
 
Slika: stranica O nama
Nakon toga se nalazi prigodan tekst koji je sastavila kolegica Jasmina Gazija, a koji ima za cilj zahvalnost klijentima na ukazanom povjerenju i odabiru naše agencije.
Boje na ovoj stranici su takodjer plava i bijela, te je cijelokupan dizajn usklađen sa ostatkom aplikacije. I ova stranica je statičnog karaktera.
 
Slika: Tekst na stranici Onama

DESTINACIJE
U aplikaciji na stranici “Destinacije” i “Uslovi Putovanja” (za čiju funkcionalnost sam bila zadužena-Jasmina) trenutno je omogućeno korisniku da prilikom pokretanja aplikacije na izbor dobiva pristup sljedećim funkcionalnostima:
 
Stranica Destinacije
 

USLOVI PUTOVANJA
•	Pregled svih destinacija/putovanja
•	Unos novih destinacija/putovanja (preko baze, unutar tabele Putovanje gdje je postavljena kolumna naziva status, s vrijednostima 0 i 1. Sa nulom regulisano je da se ne prikazuje određena ili sve destinacije, a sa 1 da prikazuje.
•	Tako da ukoliko dodje do prekida rada web aplikacije, postavljanjem na nulu u bazi, destinacije nece biti prikazane i stranica “Destinacije”neće biti funkcionalna.
•	Ažuriranje postojećih kolumna koje uređuju sadržaj destinacije
•	Prikaz detalja o svakoj pojedinačnoj destinaciji klikom na jednu od navedenih
•	Dohvaćanje podataka iz baze prema proslijeđenom id-u ili odgovarajućoj kolumni iz tabele “Putovanje”

 

Sadržaj stranice Destinacije koji je moguće mijenjati

 

Lista destinacija koje su dinamične u prikazu

 

Klikom na neku od destinacija dobija se detaljne informacije o putovanju

 

 



KATALOZI

Na stranici smještena dva kataloga u pdf format (mogućnost listanja, rotiranja, download-a, printanja, zumiranja i slično). Za pozicioniranje kataloga korišten bootstrap.

 


REZERVACIJE
Stranica rezervacije je jedna od ključnih u cijeloj aplikaciji, uz stranicu destinacija.
Ova stranica je specifična po tome što prije svega provjerava da li je korisnik prijavljen (logovan). Ukoliko nije, automatski korisnika preusmjerava na Login stranicu, kako bi se prijavio, ili registrovao, ukoliko nije već registrovan. 
Nakon prijave/registracije, omogućava korisniku pristup formi Rezervacije. U vrhu se nalazi logo agencije, a nakon toga forma za rezervaciju koja se sastoji od obaveznih polja: ime, prezime, e-mail, destinacija, datum polaska, datum povratka, broj putnika te komentar ukoliko korisnik želi osaviti neke dodatne napomene.
 
Slika: stranica Rezervacije
Ime, prezime i e-mail unosi korisnik prilikom pravljenja rezervacije.
Destinacija je urađena na način da povlači u select meniju sve dostupne destinacije iz baze, tačnije tabele Putovanja sa statusom = 1. Status 1 znači sve aktivne destinacije u bazi, a nevažeće destinacije imaju status 0.
 
Slika: Select meni koji povlačni destinacije iz baze, tabela Putovanja, kolona NazivPutovanja

Prilikom  odabira destinacije, polja Polazak i Povratak se sama ispisuju što je regulisano switch petljom u JavaSriptu.

              
  Slika: Defaultna destinacija bez datuma             Slika: Odabir destinacije i povlačenje datuma


Klikom na dugme rezerviši, ukoliko nisu sva polja popunjena, javit će se greška. Korisnik će trebati ispuniti sva polja, jer su definisana kao obavezna, kako bi uspješno  napravio rezervaciju.

 
Slika: Greška prilikom rezervacije (nisu sva polja popunjena)


Nakon što je korisnik uspješno popunio sva polja i kreirao rezervaciju, preusmjerava se na stranicu Potvrda rezervacije. Ova ga stranica obavještava da je uredno popunio rezervaciju i da će biti kontaktiran u roku od jednog radnog dana kako bi se dogovorili detalji rezervacije.

 
Slika: Potvrda rezervacije

Nakon 4 sekunde od prikaza Potvrde rezervacije, korisnik se automatski preusmjerava na glavnu, tj index stranicu.
Napravljena rezervacija se upisuje u bazu, u tabelu Rezervacije kao na slici ispod. Ovoj rezervaciji imaju pristup adiministratori putem admin panela. Administratori mogu mijenjati status rezervacije u odobreno ili otkazano. Prilikom kreiranja rezervacije, IdRezervacije se sam dodjeljuje jer je autoincrement. Također status svake rezervacije je po defaultu pending, sve dok administrator ne odluči drugačije. Ovo omogućava da više administratora može što efikasnije pratiti rezervacije i njihov status, te isključuje mogućnost greške prilikom otkazivanja rezervacije ili kontaktiranja klijenta.

 
Slika: Tabela Rezervacije u bazi, sa podacima koji su unešeni preko rezervacijske forme




KONTAKT

Prilikom otvaranja stranice, pojavljuje se kontakt forma (Ime i prezime, Email i Poruka) i pritiskom na dugme “Pošalji” poruka se šalje zajedno sa podacima direktno na mail agencije AJA Tours (ajatours2018@gmail.com). Korišten CSS, jQuery, Bootstrap, a PHP korišten za validaciju i provjeru prilikom slanja maila.

 

ADMIN PANEL

Admin panel napravljen tako da bude pregledan i jednostavan za korištenje. Sastoji se od četiri taba (Upravljanje destinacijama, upravljanje korisnicima, upravljanje rezervacijama i upravljanje headerom i footerom). Svaki tab korisniku nudi tri opcije (Dodavanje, Izmjenu i brisanje), a dugmad su fiksirana na lijevoj strani. Prilikom izmjena traži se dodatna “Potvrda” i mora se potvrditi. Sve izmjene se ažuriraju direkto u bazi. Admin panel je urađen u sivim tonovima i jednostavan je za korištenje. Prilikom izrade korišten CSS, Bootstrap i JavaScript.
 
