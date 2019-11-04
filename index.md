---


---

<h1 id="hogyan-lesz-a-lyukból-internet">Hogyan lesz a lyukból internet?</h1>
<blockquote>
<p><strong>Célcsoport</strong>: Nem hálózatüzemeltetéssel foglalkozó, ügyféltámogató kollégák<br>
<strong>Cél</strong>: Az óra végére a résztvevők kapnak egy komplexebb szemléletet,<br>
amely segítségével pontosabban tudnak igényeket megfogalmazni,<br>
hatékonyabban derítenek fel hibákat, és job rálátásuk lesz a  hálózat<br>
nem általuk  kezelt részén végbemenő folyamatokba.</p>
</blockquote>
<p>Az óra szerkezete alkalmas egy rövidebb (max 2 óra) frontális képzésre, opcionálisan rövid szünettel, de jobban működik, ha a jelenlévők akítvan részt vesznek a tudásanyag összeállításában, saját példákkal erősítik meg, amit hallanak. Ezért egy igényfelmérő beszélgetéssel nyitható a képzés, és zárható annak összeszedésével, hogy mi maradt megválaszolatlan.</p>
<p>Érintett témakörök:</p>
<ul>
<li>Networking alapok (IP, MAC, Router vs Switch, DNS, DHCP)</li>
<li>ELTENET felépítése. (vlanok, kábelrendezők és végpont azonosítók, portgazdálkodás)</li>
<li>UTP kábelek szerkezete (NET-TEL vs NET-NET)</li>
<li>Ügykezelő használata (Új - módosítás- hiba)</li>
<li>Hibakeresés lépései</li>
</ul>
<h2 id="ip---mac">IP - MAC</h2>
<ul>
<li>Mifene az az IP cím?</li>
<li>IP-Maszk-Gateway</li>
<li>Privát vs Publikus IP<br>
<em>cél: Tudjuk, milyen címet adunk épp, és Vegyük észre, ha nem kapott az IP.</em><br>
Felmerült problémák: VLAN felismerése, Nyomtató Publikus címen, más L3 alól élő hálózat kérése</li>
</ul>
<h2 id="router-vs-switch">Router vs Switch</h2>
<ul>
<li>Mi a különbség?</li>
<li>Hálózati azonosítók az aktív eszközök mögött. (Milyen IP, MAC…)<br>
Felmerült problémák: “otthoni” kategóriás eszközök, és működésük, anomáliáik.</li>
</ul>
<h2 id="dns-dhcp">DNS, DHCP</h2>
<ul>
<li>Hogy épül fel</li>
<li>Redundancia, mire jó. (pointerek, gyakorlatban)</li>
<li>DHCP:
<ul>
<li>Dinamikus: Nem kell kézzel állítani.  Poolból osztani csak extra opció.</li>
<li>Egyéb hálózati beállítások (network boot…)<br>
Felmerült problémák: subdomainek figyelmen kívül hagyása, saját vlanok nem ismerete.</li>
</ul>
</li>
</ul>
<h2 id="vlanok">Vlanok</h2>
<p><em>//TODO - Szerepük, Használatuk “oka”, komplexitásának részletezése</em><br>
<em>“Ez a hibásan beállított, valójában nem is létező vlan kiadása miért nem ugyanúgy pár perc, mint amikor Misi pár perc alatt megcsinálta itt mellettem a másikat?”</em></p>
<h2 id="kábelrendezők">Kábelrendezők</h2>
<ul>
<li>Mifene az a kábelrendező</li>
<li>Portgazdálkodás: Végpont felélesztése. Miért fontos hogy a raktárrá alakított irodáról a hálózat is tudjon?<br>
Felmerült problémák: User nem érti, miért nincs alapból mindenhol net.</li>
<li>Végpont-azonosítók szerepe. + Rajz.</li>
<li>Telefon és internet, egy helyről.</li>
</ul>
<h2 id="l1-a-falon-túl">L1, a falon túl</h2>
<ul>
<li>UTP kábel felépítése. 8 réz ér, színek…stb</li>
<li>Cross kábelek léteznek. 13-26 (zöld - narancs)</li>
<li>Bontása. “Hány különálló telefon fér el egy kábelben?”</li>
<li>Osztók szerkezete, felismerése. +Ábra.  Sávszélesség limitációi.<br>
Felmerült probléma: Telefon figyelmen kívül hagyása, Osztó használata igénylés nélkül (miért nem megy a másik)</li>
<li>Telefon után kötött számítógép.  &gt; Mac, vlan tudásanyagokra visszautalás</li>
</ul>
<h2 id="ügykezelő-használata">Ügykezelő használata</h2>
<ul>
<li>Ügyek közötti különbség.
<ul>
<li>Végpont igény. (Előzőekre visszautalás, miért fontos minden)</li>
<li>Végpont építés igénye //TODO, Kell ez? ha igen, mit érdemes mondani róla?</li>
<li>Hiba vs Módosítás<br>
Felmerült probléma: Ha nem igényeltél módosítást, az nem hiba.</li>
<li>DNS, DHCP igények, mikor kell, mikor nem.</li>
<li>VPN, Wifi, egyéb nyalánkságok. //TODO, sok ügytípust sosem használunk, mi az amit érdemes lenne várni tőlük?</li>
</ul>
</li>
<li>Hálózati adatbázis.
<ul>
<li>Hálózatfelelősök szerepe. (–Elvek–)</li>
<li>DHCP nélkül, DHCPvel</li>
<li>Melyik az Átjáró? IP tartomány megtekintése, visszautalás az IP-címek témakörre.<br>
Felmerült probléma: Base, Broadcast address-re érkező módosítási igények.</li>
</ul>
</li>
</ul>
<h2 id="hibakeresés-lépései">Hibakeresés lépései</h2>
<p>Egy összefogaló rész, építve az átismételt témákon.</p>
<ul>
<li>Probléma felderítése: Mik a szükséges adatok?
<ul>
<li>Van-e bármilyen hálózat a végponton?</li>
<li>Mikor működött utoljára</li>
<li>Mi a cím, mac, végpontszám (előzőekre utalva, minden fontos)</li>
<li>Mi abszolút irreleváns: A user szívszaggató története, hogy mi történik, ha 3 perccel ezelőttre nem kap internetet.</li>
<li>Mi számít mégis: Mire használná, esetleg változott-e valami, új igény-e valójában.</li>
</ul>
</li>
<li>Gyakorlatias szemlélet: Tesztgép nélkül nehéz kirpbóálni, hogy jó-e…</li>
<li>Kötelező lépések:
<ul>
<li>Kábelcsere: Leginkább mert a hibák fele abból adódik, hogy széttapossák, eltépik a kábelt.</li>
<li><em>Közben esetleg kiderül, hogy nem úgy van bedugva, meg nem oda, meg van egy switch aminek csak 1 lábát használják, de azt hitték fontos… Juss el a falig.</em></li>
<li>Ha nincs tesztgép, vagy gyanús, hogy a hiba nem a hálózattal van, tesztgép bedugása.
<ul>
<li>Ehhez: MAC cím maszkolása</li>
</ul>
</li>
</ul>
</li>
<li>Mit tehet érted a hálózatos? Választ ad a következő kérdésekre:
<ul>
<li>Látszik-e a mac?</li>
<li>Mikor volt utoljára forgalom rajta?</li>
<li>Milyen vlanon van, milyen címet kéne kapnia?</li>
<li>Milyen tűzfalszabályok működnek ott?</li>
</ul>
</li>
</ul>
<h2 id="zárás">Zárás</h2>
<p>Személyes tapasztalatok megosztása, kérdések.</p>
<pre><code>Források a témakörök részletezéséhez:
OP Wiki, CISCO Anyagok, Hálózatos kollégák végtelen lexikális és gyakorlati ismeretanyaga 
</code></pre>

