# Object arrays

We vallen in herhaling: ook arrays van objecten zijn mogelijk, net zoals je arrays van valuetypes al kon maken. Ook hier is de werking grotendeels dezelfde. Maar ook hier moet je er rekening mee houden dat de individuele objecten in je array **reference** values hebben en dus mogelijk ``null`` zijn.

## Array van objecten aanmaken

Een array van objecten gebeurt als volgt:

```csharp
Student[] mijnKlas = new Student[20];
```

**Maar: er staan nog géén objecten in deze array. Alle elementen in deze array zijn nu nog ``null``.**
Je zou kunnen zeggen dat we enkel nog maar de parkeerlijnen hebben aangemaakt.

![](/assets/6_klassen/legearray.png)

Willen we nu elementen in deze array plaatsen dan moeten dit ook expliciet doen:

```csharp
mijnKlas[0]= new Student();
mijnKlas[7]= new Student();
```

Uiteraard kan dit ook in een loop indien relevant voor de opgave.

Probeer je objecten te benaderen die nog niet bestaan dan zal je uiteraard een ``NullReferenceException`` krijgen.

## Individueel object benaderen

Van zodra een object in de array staat kan je deze vanuit de array aanspreken d.m.v. de index :

```csharp
mijnKlas[3].Name= "Vincent Lagasse";
```

### Null check met ?

Ook hier kan je met ``?`` een null check schrijven:

```csharp
mijnKlas?[3]?.Name= "Romeo Montague ";
```
Merk op dat het eerste vraagteken controleer of de array niet ``null``is. Het tweede vraagteken, na de index, is om te controleren of het element op die index niet ``null`` is.

# Arrays als parameters en return

Ook arrays mag je als parameters en returntype gebruiken in methoden. De werking hiervan is identiek aan die van value-types.