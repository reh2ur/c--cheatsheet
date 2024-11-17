# C# Anfänger Spickzettel

---

## 1. Variablen und Datentypen
- **Definition**: Variablen speichern Daten. Jede Variable in C# hat einen Datentyp.
- **Wichtige Datentypen**:
  - **`string`**: Speichert Text. Beispiel: `"Hallo"`
  - **`int`**: Speichert ganze Zahlen. Beispiel: `42`
  - **`bool`**: Speichert wahr/falsch. Beispiel: `true`
  - **`double`**: Speichert Dezimalzahlen. Beispiel: `3.14`

**Syntax**:
```csharp
string name = "Alice";
int alter = 25;
bool istStudent = true;
double groesse = 1.75;
```

## 2. If-Bedingungen (If Conditions)
- **Definition**: Führt Code aus, wenn eine Bedingung wahr ist.

**Syntax**:
```csharp
if (bedingung)
{
    // Code, wenn die Bedingung wahr ist
}
else if (andereBedingung)
{
    // Code, wenn die andere Bedingung wahr ist
}
else
{
    // Code, wenn keine der Bedingungen wahr ist
}
```

**Beispiel**:
```csharp
int zahl = 10;
if (zahl > 5)
{
    Console.WriteLine("Die Zahl ist größer als 5");
}
else
{
    Console.WriteLine("Die Zahl ist 5 oder kleiner");
}
```

## 3. Switch-Case
- **Definition**: Nutzt mehrere mögliche Werte, um Code auszuführen.

**Syntax**:
```csharp
switch (variable)
{
    case wert1:
        // Code für wert1
        break;
    case wert2:
        // Code für wert2
        break;
    default:
        // Code, wenn kein Fall zutrifft
        break;
}
```

**Beispiel**:
```csharp
int tag = 3;

switch (tag)
{
    case 1:
        Console.WriteLine("Montag");
        break;
    case 2:
        Console.WriteLine("Dienstag");
        break;
    case 3:
        Console.WriteLine("Mittwoch");
        break;
    default:
        Console.WriteLine("Kein gültiger Tag");
        break;
}
```

## 4. While-Schleifen (While Loops)
- **Definition**: Führt Code so lange aus, wie die Bedingung wahr ist.

**Syntax**:
```csharp
while (bedingung)
{
    // Code, der wiederholt ausgeführt wird
}
```

**Beispiel**:
```csharp
int i = 0;
while (i < 5)
{
    Console.WriteLine($"i ist {i}");
    i++; // i um 1 erhöhen
}
```

### while (true)
- **Definition**: Eine Endlosschleife, die nur mit break beendet werden kann.

**Syntax**:
```csharp
while (true)
{
    // Endloser Codeblock
    if (bedingung)
    {
        break; // Beendet die Schleife
    }
}
```

**Beispiel**:
```csharp
int zahl = 0;
while (true)
{
    Console.WriteLine("Gib eine Zahl ein (0 beendet die Schleife):");
    zahl = int.Parse(Console.ReadLine());
    if (zahl == 0)
    {
        Console.WriteLine("Schleife beendet.");
        break;
    }
}
```

## 5. For-Schleifen (For Loops)
- **Definition**: Wiederholt Code eine festgelegte Anzahl von Malen.

**Syntax**:
```csharp
for (start; bedingung; schritt)
{
    // Code, der wiederholt wird
}
```

**Beispiel**:
```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine($"i ist {i}");
}
```

## 6. Do-While-Schleifen
- **Definition**: Führt den Code mindestens einmal aus, bevor die Bedingung überprüft wird.

**Syntax**:
```csharp
do
{
    // Code, der ausgeführt wird
}
while (bedingung);
```

**Beispiel**:
```csharp
int i = 0;
do
{
    Console.WriteLine($"i ist {i}");
    i++;
}
while (i < 5);
```


## 7. Zufallszahlen (Random mit Next)
- **Definition**: Erstellt Zufallszahlen.

**Syntax**:
```csharp
Random zufall = new Random();
int zahl = zufall.Next(min, max); // min = inklusive, max = exklusiv
```

**Beispiel**:
```csharp
Random zufall = new Random();
int zahl = zufall.Next(1, 10); // Zufallszahl zwischen 1 und 9
Console.WriteLine($"Zufallszahl: {zahl}");
```


## 8. break-Anweisung
- **Definition**: Beendet Schleifen oder Switch-Case-Blöcke.

**Beispiel in einer Schleife**:
```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
    {
        break; // Schleife wird beendet, wenn i 5 ist
    }
    Console.WriteLine(i);
}
```

**Beispiel in Switch-Case**:
```csharp
switch (tag)
{
    case 1:
        Console.WriteLine("Montag");
        break;
    case 2:
        Console.WriteLine("Dienstag");
        break;
}
```
