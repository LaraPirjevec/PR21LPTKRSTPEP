# Vinjenost in prometne nesreče: je smiselno zaostriti pogoje?
Podatkovno Rudarjenje 21/22 Skupina 9 Lara Pirjevec, Tilen Kelc, Rok Stanič, Tomaž Plešnik, Erik Poljšak

## Problem
Alkohol in njegovi učinki na voznika, je še vedno eden glavnih elementov pri povzročitvi prometnih nesreč. Alkohol omeji naše sposobnosti varnega sodelovanja v prometu, počasnejše zaznavamo, predvidevamo in presodimo situacije. Zato se zaradi vpliva alkohola že pri koncentraciji 0,5 promila verjetnost povzročitve prometne nesreče podvoji, pri 1,1 promila alkohola pa 8-krat poveča v primerjavi s treznim voznikom.
Zakoni glede omejitve koncentracije alkohola v krvi se čez leta spreminjajo. Vedno bolj se poostrujejo, ampak zaskrbljujoče je da več kot tretjina voznikov, ki povzročijo smrtno prometno nesrečo, vozi pod vplivom alkohola.
Leta 2019 je Agencija za varnost prometa (AVP) dala predlog, da bi znižali dovoljene meje alkohola za voznike s sedanjih 0,5 na 0,2 promila alkohola v krvi. Ministrstvu za infrastrukturo pa predlagajo tudi strožjo obravnavo voznikov, ki imajo v krvi več kot 1,1 promila alkohola.

Zanima nas če so spremembe zakonika res potrebne, pri zmanjšanju nesreč in izboljšanju situacije. Glavno vprašanje je "Ali se večina prometnih nesreč zaradi vinjenosti zgodi znotraj dovoljenih meja?", iz katerega pa sledijo tudi podvprašanja, kot so:
- Ali so ceste bolj varne s strožji ukrepi?,
- Kakšen tip nesreče je najbolj pogost zaradi vinjenosti?,
- Kakšne so starostne skupine v dotičnih nesrečah?,
- Kdaj se take nesreče zgodijo?,
- Ali obstaja povezava med vsebnostjo alkohola in resnostjo nesreč?,
- Kakšna je odvisnost števila nesreč od količine prometa, seveda še vedno v kontekstu vinjenih voznikov?

## Podatki
Podatke smo pridobili preko statističnega urada in sicer policijski zapisnik od leta 2009 dalje. 

Link: https://podatki.gov.si/data/search?open_data=True&all_podrocje=Promet+in+infrastruktura&publisher=ministrstvo_za_notranje_zadeve_policija 

Prvotni namen zbiranja podatkov je shranjevanje in objektivno prikazovanje podatkov glede prometnih nesreč v Sloveniji. 
Podatki  so nam podani v .cvs obliki, vzeli pa smo podatke za zadnjih 10 let nazaj, torej od 2011 do 2021. 

Podatki so nam podani v naslednji obliki: 

![alt text](/images/izgled.jpg)
 
Podatki za vsako leto so podani v posebej datoteki, zato pred analizo vse te datoteke preberemo in podatke združimo v en velik seznam slovarjev.

## Glavne ugotovitve in izvedene analize
Vsa koda se izvaja v nootebooku: https://github.com/LaraPirjevec/PR21LPTKRSTPEP/blob/main/jupyter/graphs.ipynb 

Ker so imeli podatki tudi lokacije nesreč, smo le te vizualno predstavili na zemljevidu, kjer je možno tudi videti, kje se te nesreče največkrat zgodijo. 

![alt text](/images/zemljevid.jpg)

Poskusili smo vzpostaviti povezavo med vsebnostjo alkohola v krvi in resnostjo nesreč. 
Nepresenetljivo so rezultati bili zaskrbljujoči. Možnost za smrt pri treznem vozniku v nesreči je bila 0.63%, pri alkoholiziranem pa 2.24%. Možnost težje poškodbe ali smrt pri treznem vozniku je bila 4.63% pri alkoholiziranem pa 11.07%.
 
![alt text](/images/podatki.jpg)

![alt text](/images/graf_podatki.jpg)

Naslednji korak je bil točno razvrstiti  število nesreč po količini alkohola v krvi in sicer za nad 0.2; nad; 0.5; in nad 1.1.
Rezultati so podpirali prejšnje ugotovitve in odgovorili na naše zastavljeno vprašanje, da se večina nesreč pod vplivom alkohola ne zgodi pod omejitvami ampak nad. Med trenutno mejo in mejo, ki jo je priporočila Agencija za varstvo prometa je le 11.66% nesreč, kjer je voznik vinjen.
 
![alt text](/images/razporeditev_alkohola.jpg)
 
Na vprašanje, kateri tip nesreče je najbolj pogost, smo odgovorili tako, da za vsako nesrečo preverimo najprej vrednost strokovnega pregleda nesreče, če se ta ne razlikuje od nič, pa vrednost alkotesta. Vrednost alkotesta je potrebno tudi pretvoriti iz vrednosti izdihanega zraka, v vrednost alkohola v krvi. 

Pri tem smo izvedeli, da sta 2 najbolj pogosta tipa nesreče v vinjenem stanju trčenje v objekt, ter bočno trčenje.
 
![alt text](/images/graf_tip_nesrec.jpg)

![alt text](/images/podatki_tip_nesrec.jpg)




Raziskali smo tudi številčno razdeljenost število nesreč po starostih skupinah. Pri tem smo izvedeli, da se je največ nesreč zgodilo pri mlajših in srednjih generacijah.

![alt text](/images/podatki_starost.jpg)

![alt text](/images/graf_starost.jpg)

 
 
 
 
