# Mitta

Luo uusi projekti tai käytä annettua projektia.

1. Luo projektiin luokka Mittari. Mittarilla on oliomuuttuja private int _mitta, parametriton konstruktori (asettaa muuttujan mitta alkuarvoksi 0), sekä seuraavat neljä metodia:  
	a. Metodi public void Lisaa() kasvattaa oliomuuttujan _mitta arvoa yhdellä. Ei kasvata arvoa yli viiden.  
	b. Metodi public void Vahenna() vähentää oliomuuttujan _mitta arvoa yhdellä. Ei vähennä arvoa negatiiviseksi.  
	c. Metodi public int Mitta() palauttaa oliomuuttujan _mitta arvon.  
	d. Metodi public boolean Taynna() palauttaa true mikäli oliomuuttujan _mitta on viisi, palauttaa muulloin false.  

Esimerkki luokan käytöstä.
```c#
Mittari m = new Mittari();

while(!m.Taynna()) { 
	Console.WriteLine("Ei täynnä! Mitta: " + m.Mitta());
	m.Lisaa();
} 

Console.WriteLine("Täynnä! Mitta: " + m.Mitta());
m.Vahenna();
Console.WriteLine("Ei täynnä! Mitta: " + m.Mitta());
```

Esimerkkitulostus

Ei täynnä! Mitta: 0\
Ei täynnä! Mitta: 1\
Ei täynnä! Mitta: 2\
Ei täynnä! Mitta: 3\
Ei täynnä! Mitta: 4\
Täynnä! Mitta: 5\
Ei täynnä! Mitta: 4
