# Po co komu tyle języków programowania?

Dawno, dawno temu, kiedy kokaina uchodziła jeszcze w Kalifornii za miękkie dragi, 
ludzie rozmawiali z komputerami w ich naturalnym języku. 

Słowem ... pełen odlot.

Jedna z takich rozmów mogła przebiegać następująco:

<małe zdjęcie karty perforowanej *ołówkowej*>

- Hipis: Hej, komputer! Masz tu listę rozkazów.
- Komp: (miga lampkami)
- Hipis: Jak to jak? Jak zwykle. Wsunę Ci kartę perforowaną ...
- Komp: (buczy okrutnie).
- Hipis: Weź, mnie nie wkurzaj! Całą noc skreślałem te zakichane cyferki. Czuję się, jakbym cały weekend grał w toto-lotka! Skup się, nadaję ...
- Komp: (stuka i puka).
- Hipis: No pewnie, że już liczyłeś silnię z 49. Mówiłem Ci, że gram w totka. 

Programowanie, naprawdę polegało na podawaniu komputerowi rozkazów w postaci ciągów liczb.
Na przykład ciąg jedynek i zer `10110000 01100001` to rozkaz "Zapamiętaj sobie liczbę 97 w Twoim rejestrze AL". 

Pojawiły się klawiatury, a z nimi pierwszy język programowania *wyższego (hic!) niż kod binarny poziomu*.
Nazywał się assembler (od angielskiego *monter*) i pozwalał stosować tzw. mnemoniki, że niby łatwiej zapamiętać.
Ten sam rozkaz wygląda w nim tak:

`MOV AL, 61h     ; Bo 97 to szesnastkowo 61`

Prawda, że GIGANTYCZNA różnica? Wiem, zabawne. A ... jednak postęp.

Bo oto wyszła na jaw pierwsza cecha, której twórcy języków programowania poszukiwali potem nieustannie. 
Możliwość stosowania własnego, ludzkiego języka, czy nawet języka specyficznego dla konkretnej dziedziny wiedzy. 
Aby ułatwić, życie programistom tworzone języki będą starały się wyrażać różne konstrukcje 
w sposób możliwe łatwy do zapamiętania i zrozumienia. Zanim pokażę jakie, wróćmy do naszego hipisa.

Postanowił on zyskać wiekopomną sławę wśród geeków całego świata. 
Skonstruował w garażu własną drukarkę igłową i postanowił napisać dla niej uniwersalny sterownik.
Rynek się rozwija jak na drożdżach, komputery są szybsze, ładniejsze, i w ogóle.
Jest jedno *ALE*. Co komputer to ma inny procesor, z inną listą rozkazów, inną liczbą rejestrów itd. 
Do tego, niektóre potrafią rozmawiać tylko o liczbach 8. bitowych, inne pozwalają już dodawać liczby 16. bitowe. 
Słychać nawet o POTWORACH umiejących zarówno dodawać liczby 32. bitowe jednym rozkazem, 
jak i obsługiwać pamięci o 32. bitowych adresach!

<zdjęcie pierwszych iMac, IBM PC, i czegoś jeszcze >

Słowem ... jak ten świat zasuwa.

No a każda różnica to nie tylko dodatkowa robota, bo albo coś można dodać jednym rozkazem, 
albo trzeba napisać extra funkcję dodającą liczby po kawałku, ale też okazja do popełnienia głupiego błędu. 
Bo na przykład jeden procesor zapisuje do pamięci liczbę 16. bitową F090h, 
zaczynając od młodszego bajtu (tzw. Little Endian), o tak:

- Pamięć, adres 0000100: F0h
- Pamięć, adres 0000101: 90h

A inny procesor, dokładnie odwrotnie (tzw. Big Endian):

- Pamięć, adres 0000100: 90h
- Pamięć, adres 0000101: F0h

Więc trzeba uważać, przesyłając dane do drukarki, bo ta oczekuje pierwszego podejścia.
I sterownik musi wiedzieć, na jakim CPU działa i gdy trzeba, odwracać przesyłane dane jak mrówka.

<proponuję przyjąć formułę, CIEKAWOSTKA, z osobną małą reklamą, w osobnym okienku.
Tu informację, że są CPU, które pozwalają wybrać, jak zapisują dane.>

Nasz hippis słyszał o nowych językach programowania "wyższego (jak zwykle) poziomu".
Namnożyło się ich na rynku jak grzybów po deszczu <listę *wymarłych* języków podać jako CIEKAWOSTKĘ>.
Jeden zdobywa straszną popularność, również wśród autorów sterowników, nazywają go C.
Można napisać coś raz, *po ludzku*, i taki program zwany kompilatorem sam to dopasuje do różnych CPU.

Słowem ... totalny odlot!
