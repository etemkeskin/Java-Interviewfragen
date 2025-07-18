# Java-Interviewfragen
Java-Interviewfragen

<details>

<summary>Fragen, die du stellen solltest ?</summary>

1. Was ist das Hauptziel und der Umfang des Projects?
2. Welche Technologien werden im Project verwendet?
3. Wann hat das Project begonnen und wann soll es abgeschlossen sein?
4. Wie groß ist das Projectteam und welche Rollen sind darin enthalten?
5. Welche Java-Version wird aktuell verwendet?
6. Welche Version von Spring-Boot wird im Project eingesetzt?
7. Wervendet ihr JPA oder jdbc (oder beides)?
8. Welche Versionverwaltung nutzt ihr - Github, gitlab etwas anderes?

</details>

# Java und OOP

<details>
    <summary>Was sind die Unterschiede zwischen JDK und JRE?  </summary>
JRE(Java Runtime Enviroment) ist die Lauftzeitumgebung, die notwendig ist, um eine Java Anwendung auszuführen.
    Sie enthält die Java-Bibliotheken, die JVM(Java Virtual Machine)  sowie weitere Komponenten, die zur Ausführung von Java-Programmen
    erforderlich sind.

JDK(Java Development Kit) ist das Softwarepaket, das benötigt wird, um Java-Anwendungen zu entwickeln.
    Es enthält Werkzeuge wie den Compiler(javac), mit dem .java-Dateien .class-Dateien kompiliert werden können.
    Das JDK beinhaltet die JVM, JRE und zusätzliche Entwickler-Tools.  
</details>
<details> <summary>Was bedeuten die Konzepte 'super' und 'this' in Java?
</summary>

1. **super**: wird in einer Unterklasse verwendet, um auf Methoden oder Variablen der Oberklasse    zuzugreifen. Mit super
    kann man innerhalb der Unterklassse explizit die Implementierungen der Oberklasse ansprechen, z.B. beim Überschreiben von Methoden.
2. **this**: wird verwendet, um auf das aktuelle Objekt der Klasse zuzugreifen. Besonders nützlich ist this, wenn lokale Parameter den gleichen Namen 
    wie Instanzvariablen haben - this hilft dabei,zwischen ihnen zu unterscheiden.

</details>

<details> <summary>Was ist der Unterschied zwischen **equals** und **==** in Java?
</summary>

-  **equals**: ist eine Methode, die den Inhalt bzw. den Wert zweier Objekte vergleicht. 
Zum Beispiel: Zwei verschiedene String-Objekte mit dem gleichen Text liefern bei **equals()**
den Wert **true**.
- **==**: ist ein **Operator**, der überprüft, ob zwei Referenzen auf dasselbe Objekt im Speicher zeigen.Das bedeutet: Auch wenn zwei Objekte den gleichen Inhalt haben, liefert **==** nur dann
**true**, wenn sie dieselbe Speicheradresse haben.

</details>

<details> <summary>Was sind die Unterschiede zwischen Abstrakte Klassen und Interfaces in Java?
</summary>

-  **Abstrakte Klasse**: wird verwndet, wenn Klassen gemeinsame Funktionalität (Code) teilen sollen. Sie kann sowohl abstrakte als auch konkrete Methoden enthalten. 

- **Interface**: dient der reinen Schnittstellendefinition. Beschreibt nur, was eine Klasse tun soll, nicht wie. Seit Java 8 können Interfaces auch deafult und static Methoden enthalten. Eine Klasse kann mehrere Interfaces implementieren. 
</details>

<details> <summary>Public, Private, Default und Protected - Zugriffsmodifizierer in Java?
</summary>

-  **public**: die Variable oder Methode ist für alle Klassen, auch aus anderen Paketen, ist sichtbar. 

- **private**: kein Zugriff von außen oder von Unterklassen - nur innerhalb der gleichen Klasse.
- **default**:wir kein Modifizierer angegeben, gilt dieser Standartzugriff. Andere paketehaben keinen Zugriff.
- **protected**: Zugänglich für Unterklassen und Klassen imselben Paket   
</details>

<details> <summary>Was sind die Prinzipien der objektorientierten Architektur?
</summary>

- **Encapsulation(Datenkapselung)**: Dia Kapselung bedeutet, dass Daten(Attribute) und Funktionen(Methoden) , die zu einem Objekt gehören,
zusammengefasst und vor dem direkten Zugriff von außen geschützt werden. So wird sichergestellt, dass Daten nur über definierte Schnittstellen werden können. Dies erhöht die Sicherheit und Wartbarkeit des Codes.
- **Inheritance(Vererbung)**: Die Vererbung erlaubt es, dass eine Klasse Eigenschaften und Methoden einer anderen Klasse erbt. Dadurch wird Code-Wiederverwendung möglich und es entstehen Beziehungen zwischen Klassen. Die untergeordnete Klasse(Subklasse) kann die Eihenschaften der übergeordneten Klasse(Superklasse) verwenden und bei Bedarf erweitern.
- **Polymorphism(Polymorphie/Vielgestaltigkeit)**: Polymorphie bedeutet, dass eine Methode in verschidenen Klasse unterschiedlich implementiert werden kann, obwohl sie denselben Namen hat. So kann ein Objekt je nach Typ unterschiedliches Verhalten zeigen.
- **Abstraction(Abstraktion)**: Die Abstraktion, dass komplexe Details verborgen und nur die wesentlichen Informationen offengelegt werden.Dadurch wird die Abhängigkeit zwischen den Komponenten reduziert und der Code übersichtlicher.
</details>

<details> <summary>Was ist Methodenüberladung und Methodenüberschreibung in Java?
</summary>

-  **Method Overloading(Methodüberladung)**: die Methodeüberladung bedeutet, dass innerhalb einer Klasse mehrere Methodenmit dem gleichen
Namen, aber unterschiedlicher Parameterliste(Anzahl oder Typ der Parameter)  definiert werden.
```java
public class Rechner {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

- **Method Overriding(Methodüberschreiben)**: Die Methodüberschreibung, dass eine Unterklasse eine Methodeder Oberklasse mit dem gleichen Methodnamen, Parametern und Rückgabewert neu definiert, um das Verhalten anzupassen.
```java
class Tier {
    void macheGeräusch() {
        System.out.println("Ein Tier macht ein Geräusch");
    }
}

class Hund extends Tier {
    @Override
    void macheGeräusch() {
        System.out.println("Der Hund bellt");
    }
}

```
</details>

<details> <summary>Was sind static und final in Java und wo werden sie verwendet?
</summary>

**static**: Das **static**- Schlüsselwort wird verwendet, um anzugeben, dass eine Variable oder Methode zur Klasse gehört und nicht zu einer bestimmten Instanz(Object) der Klasse.
- **Static-Variablen**: gehören zur Klasse und werden von allen Objekten gemeinsam genutzt. Es gibt nur Kopie der Variable - unabhängigvon der Anzahl der Objekte.
-  **Static-Methoden**: Können ohne Objeckt direkt über den Klassennamen aufgerufen werden. Sie dürfen nich auf nicht-statische(instanzbezogene) Variablen oder Methoden zugreifen, da sie nicht wissen, welches Objekt gemeint ist. 
```java
public class Auto {
    static int anzahlAutos = 0;  // Klassenvariable

    public Auto() {
        anzahlAutos++;
    }

    static void zeigeAnzahl() { // Klassenmethode
        System.out.println("Anzahl Autos: " + anzahlAutos);
    }
}

public class Main {
    public static void main(String[] args) {
        Auto auto1 = new Auto();
        Auto auto2 = new Auto();
        Auto.zeigeAnzahl(); // Ausgabe: Anzahl Autos: 2
    }
}
```


**final**: Das **final**-Schlüsselort wird verwendet, um anzugeben, dass etwas nicht verändert werden darf, nachdem es einmal gesetzt oder deklariert wurde.(Klass, Method oder Variable)
- **final** Klassen können keine Unterklassen haben.
- **final** Methoden können nicht von Unterklassen überschrieben werden.
```java
public class Kreis {
    final double PI = 3.14159;  // Konstante

    double berechneUmfang(double radius) {
        return 2 * PI * radius;
    }
}

 final class FinalClass {
       // ...
   }

```
</details>

<details> <summary>Unterschied zwischen Set, Map und Arraylist in Java?
</summary>

- **Datenreihenfolge**: Eine **ArrayList** speichert die Elemente, in der sie hinzugefügt wurden, und erlaubt doppelte Elemente. Ein **Set** speichert die Elemente ungeordnet und ohne Duplikate. Eine **Map** speichert Schlüssel-Wert-Paare, wobeijeder Schlüssel nur einmalvorkommen darf.

- **Zugriff auf Elemente**: In einer **ArrayList** erfolgt der Zugriff über Indexnummern(z.B. list.get(0)). Bei **Set** und **Map** erfolgt der Zugriff über den Schlüssel bzw. über die enthaltenen Objekte selbst.De jeder Schlüssel in einer **Map** eindeutig ist, ist der Zugriff in der Regel sehr schnell.  
- **Doppelte Einträge**: **ArrayList** erlaubt mehrfache Vorkommen desselben Elements. **Set** und **Map** hingegen verhindern doppelte Einträge - ein Element bzw. ein Schlüssel kann nur einmal vorhanden sein.
- **Leistung(Performance)**: Beim Hinzufügen und Entfernen von Elementen ist **ArrayList** oft schneller,da keine Prüfung auf Duplikate oder Schlüssel erfolgen muss. Beim Zugriff auf Elemente sind **Set** und besonders **Map oft schneller**, da sie Schlüssel-basierte Datenstrukturen nutzen und so den direkten Zugriff ermöglichen.
</details>

<details> <summary>Was ist der Unterschied zwischen einer ArrayList und einer LinkedList in Java?
</summary>

**`ArrayList`** ist eignet sich besser für Indexbasierten Zugriff und sequentielle Datenspeicherung, während **`LinkedList`** besser für dynamische Einfüge- Löschvorgänge geeignet ist. 

</details>
