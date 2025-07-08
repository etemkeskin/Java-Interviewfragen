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