# Practica
Algoritmul Rabin-Karp este un algoritm de căutare în șiruri de caractere, creat de Michael Rabin și Richard Karp și care folosește hashingul pentru a găsi un subșir al șirului de căutat. Pentru un text de lungime n și un șablon de lungime m, complexitatea în timp cea mai bună și cea medie este de O(n), dar în cazurile cele mai rele, ea este de O(mn), și de aceea algoritmul nu este folosit pe scară largă. Totuși, el prezintă avantajul că are aceeași complexitate indiferent de numărul de șabloane căutate. O utilizare practică a acestui algoritm este detecția plagiatului. Cu ajutorul algoritmului Rabin-Karp se pot căuta rapid mai multe propoziții din documentul sursă în același timp în documentul suspect. Din cauza numărului mare de șiruri care se caută, algoritmii de căutare care oferă performanțe la căutarea unui singur șir sunt nepractici.



Pseudocod
function RabinKarp(string s[1..n], string sub[1..m])
 2     hsub := hash(sub[1..m])     
 3     for i from 1 to n-m+1
 4         if hs = hsub
 5             if s[i..i+m-1] = sub
 6                 return i
 7         hs := hash(s[i+1..i+m])
 8     return not found
