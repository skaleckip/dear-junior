# Po co komu tyle języków programowania?

Dawno, dawno temu, kiedy kokaina uchodziła jeszcze w Kalifornii za miękkie dragi, ludzie rozmawiali z komputerami w ich
naturalnym języku.

Słowem ... pełen odlot.

Jedna z takich rozmów mogła przebiegać następująco:

![alt text][karta_dziurkowana]

- Hipis: Hej, komputer! Masz tu listę rozkazów.
- Komputer: (miga lampkami)
- Hipis: Jak to jak? Jak zwykle. Wsunę Ci kartę perforowaną w ...
- Komputer: (buczy okrutnie).
- Hipis: Weź, mnie nie wkurzaj! Całą noc dziurkowałem te cyferki. Czuję się, jakbym grał w Totolotka. Skup się, nadaję !
- Komputer: (stuka i puka).
- Hipis: No pewnie, że już liczyłeś silnię z 49. Mówiłem Ci, że gram w Totka.

Programowanie naprawdę polegało na podawaniu komputerowi rozkazów jako ciągów liczb. Na przykład
ciąg `10110000 01100001` to rozkaz *Zapamiętaj sobie liczbę 97 w rejestrze AL*.

Pojawiły się klawiatury, a wraz z nimi pierwszy język programowania *wyższego (hic!) poziomu* (niż kod binarny). Nazywał
się Assembler (od angielskiego *Monter*) i pozwalał stosować tzw. mnemoniki, że niby łatwiej zapamiętać. Ten sam rozkaz
wraz z komentarzem wygląda w nim tak:

`MOV AL, 61h ; Bo 97 to szesnastkowo 61`

Prawda, że GIGANTYCZNA różnica? Wiem, zabawne. A ... jednak postęp.

Oto bowiem pojawiła się pierwsza cecha, której twórcy języków programowania szukali odtąd nieustannie. Możliwość
stosowania własnego, ludzkiego, języka. A najlepiej, języka specyficznego dla konkretnej dziedziny wiedzy. Aby ułatwić
życie programistom, tworzone języki będą starały się wyrażać różne konstrukcje w sposób możliwe łatwy do zapamiętania,
zrozumienia i zastosowania.

Ale wróćmy do naszego hipisa.

Postanowił on zyskać wiekopomną sławę wśród geeków. Skonstruował w garażu własną drukarkę igłową i postanowił napisać
dla niej uniwersalny sterownik. Rynek rozwija się jak na drożdżach, komputery są szybsze, ładniejsze, i w ogóle.

Jest jedno *ALE*.

Co komputer to ma inny procesor, z inną listą rozkazów, inną liczbą rejestrów pamięci i innymi możliwościami. Niektóre
potrafią rozmawiać tylko o liczbach 8. bitowych, inne umieją dodawać liczby 16. bitowe. Słychać nawet o POTWORACH
umiejących dodawać liczby 32. bitowe, a do tego obsługiwać pamięci o 32. bitowych adresach!

![alt text][ibm_pc_classic]
![alt text][mac_classic]
![alt text][sun_sparc_workstation]
<Zrobić montaż o równej wysokości i oświetleniu!>

Słowem ... jak ten świat zasuwa.

Każda różnica to jednak dodatkowa robota. No bo albo można dodać liczby 16. bitowe jednym rozkazem, albo trzeba napisać
funkcję dodającą je 8. bitowymi kawałkami. Jak na kartce paperu, 6 + 7 = 13, zatem zapisz 3 i przenieś 1, i tak dalej. A
do tego znakomita okazja do popełnienia głupiego błędu. Bo na przykład jeden procesor zapisze w pamięci liczbę 16.
bitową F192h, zaczynając od młodszego bajtu (*Little Endian*), o tak `F1h 92h`, a inny dokładnie odwrotnie (Big Endian),
czyli tak `92h F1h`. I przesyłając dane do drukarki, trzeba uważać, bo ta akurat oczekuje pierwszego podejścia.
Sterownik musi kumać, na jakim CPU działa i jeśli trzeba, odwracać przesyłane bajty jak mrówka.

<proponuję przyjąć formułę CIEKAWOSTEK, z osobną małą reklamą, w osobnym okienku. Tu np. informację, że są CPU, które
pozwalają wybrać czy zapisują dane w stylu Little, czy Big Endian.>

Nasz hippis słyszał już o nowych językach programowania *wyższego poziomu*. Namnożyło się ich na rynku jak grzybów po
deszczu, ADA, FORTRAN, COBOL, C. Jeden zdobywa wyjątkową popularność, szczególnie wśród autorów sterowników. ZWĄ GO *C*.
Nie, nie widzieli jeszcze *Man In Black*. Można napisać coś raz, *standardowo*, a kompilator tego języka C sam *
wygeneruje* kod binarny odpowiedni dla różnych CPU.

Słowem ... totalny odlot!

<listę *wymarłych* języków podać jako CIEKAWOSTKĘ>.

I tu dochodzimy do kolejnej cechy języków. Chodzi, o PRZENOŚNOŚĆ, czyli ukrywanie różnic między sprzętem, na którym
działają programy.

[karta_dziurkowana]: images/Karta_dziurkowana_1.jpg "Karta dziurkowana"

[ibm_pc_classic]: images/IBM_PC_5150.jpg "IBM PC Classic"

[mac_classic]: images/Macintosh_classic.jpg "Apple Macintosh Classic"

[sun_sparc_workstation]: images/Sun_SPARC_Workstation.jpg "Sun SPARC Workstation"
