# Ja, ich bin ein Java Programmierer



Ich habe versucht, die Fragen so effizient wie möglich zu gestalten. Auch die Reihenfolge der Fragen ist nicht zufällig ausgewählt. Verwandte Themen sind direkt nebeneinander gelistet. Viele dieser Überschriften aus diesem Schreiben sind in irgendeiner Art und Weise miteinander verknüpft. Alles optimal darzustellen, ist für mich fast unmöglich. Trotzdem sollten die Überschriften/Konzepte/Werkzeuge in ihrer einfachsten Anwendung und in dieser Auflistung sinnvoll sein. So gut wie jeden Punkt hier könnte man noch endlos erweitern. Dies muss dann aber auf eigene Initiative passieren. Vielleicht dient euch diese Zusammenfassung ja als eine Art CheatSheet.


Have Fun!

---

# Inhalt

## Coding Vokabeln
- "Methodensignatur"
- "iterieren"
- "Inkrementieren"
- "Endpoints"
- "CLI"
- "Rekursion"

## Basics
- "Signalfluss" Java
- compile-/runtime
- primitive Datentypen
- statisch VS dynamischer Datentyp
- operatoren
- main
- void
- equals
- final
- scanner
- parsen
- casten (Typenumwandlung)

## Exceptions
- try/catch
- throw/throws

## OOP
- konstruktor
- this
- super
- @override
- private, public
- static
- abstract
- implements
- extends
- getter/setter
- implement/interface

## Datenstrukturen
- Array
- Lists
- LinkedList
- Stack
- Queue
- Hashmap
- Graph
- Tree


## Zusatz
- final VS static



## Noch in arbeit:

- Streams
- generics
- interator
- casten
- toString
- schleifen: for, for-each, while. do, do-while
- parsen
- uvm.



<br>

<br>

<br>

---

# Coding Vokabeln

<br>

## Was ist die "Methodensignatur"?
Die "Methodensignatur" in Java bezieht sich auf die Deklaration einer Methode, einschließlich ihres Namens, der Parameterliste und des Rückgabetyps. 
Sie definiert, wie eine Methode aufgerufen wird und welche Art von Argumenten sie erwartet und zurückgibt, aber nicht ihren tatsächlichen Code.

```java
public int add(int a, int b)
```

In diesem Beispiel ist die Methodensignatur:

- Name der Methode: add
- Parameterliste: (int a, int b)
- Rückgabetyp: int

Die Methode add erwartet zwei Integer-Parameter (a und b) und gibt einen Integer-Wert zurück. Die eigentliche Implementierung der Methode ist hier nicht enthalten und gehört nicht zur Methodensignatur.

<br>

## Was ist  "iterieren"?
"Iterieren" bedeutet, eine Schleife oder eine Wiederholung zu verwenden, um durch eine Sammlung von Elementen oder eine Sequenz von Daten zu gehen. Bei der Iteration werden die Elemente nacheinander verarbeitet oder durchlaufen, normalerweise von Anfang bis Ende.

<br>

## Was bedeutet "inkrementieren"?
Das "Inkrementieren" ist ein Begriff in der Programmierung und Mathematik, der bedeutet, einen Wert um einen bestimmten Betrag zu erhöhen. In der Regel handelt es sich um eine Erhöhung um den Wert "1". Das Gegenteil, das Verringern eines Werts um einen bestimmten Betrag, wird als "Dekrementieren" bezeichnet. Beim Inkrementieren wird der Wert erhöht, z.B. von 1 auf 2 oder von einer anderen Zahl auf die nächstgrößere Zahl.

<br>

## Was bedeutet "Endpoints"?

<br>

## Was bedeutet "CIL"?
Comand Line Interface (Eigene Konsolenbefehle von: Frameworks, APIs, etc)

<br>

## Was ist "Rekursion"
Rekursion ist ein Konzept in der Informatik und Mathematik, bei dem eine Funktion oder ein Algorithmus sich selbst aufruft, um ein Problem in kleinere Teilprobleme aufzuteilen und diese Teilprobleme zu lösen.

Rekursion kann in vielen Programmiersprachen wie Java verwendet werden, um komplexe Probleme elegant und effizient zu lösen. 

<br>

---

# Thema: Basics

<br>


### **For-Schleife:** 
Die For-Schleife nimmt man immer dann, wenn man die Anzahl der benötigten Schleifen-Durchläufe schon im Voraus kennt. Für die Vorschleife werden die folgenden drei 

Parameter benötigt:
- Initialisierung
- Zielwert
- Schrittweite
Mit der Initialisierung legt man fest, ab welchen Wert man mit der Schleife startet. 

Die Schleife wird dann so lange durchgeführt, bis der Zielwert erreicht oder überschritten wird. Wie schnell das geht, das legt man mit der Schrittweite fest. Anbei die allgemeine Syntax der For-Schleife:


```java
// BSP1
for (int i = 0; i <= 10; i++) {
    // Hier wird eine "for"-Schleife initialisiert.
    // Der Zähler "i" wird auf 0 gesetzt, und die Schleife wird so lange ausgeführt, wie "i" kleiner oder gleich 10 ist.
    // Bei jedem Schleifendurchlauf wird "i" inkrementiert (um 1 erhöht).
}

//BSP2
for (int i = 0; i < array.length; i++) {
    // Hier wird die Schleife initialisiert und startet mit i = 0.
    // Die Schleife wird so lange ausgeführt, wie i kleiner als die Länge des Arrays (array.length) ist.
    // In jedem Schleifendurchlauf wird i um 1 erhöht.
}
```

<br>

### **While-Schleife**

Die While-Schleife wird so lange durchlaufen, bis die Bedingung ein False ergibt. Dabei steht die Bedingung am Anfang, ist sie also schon davor „falsch“, dann wird die Schleife kein einziges Mal ausgeführt, sondern übersprungen.

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int count = 1; // Initialisierung einer Zählvariable

        // Die while-Schleife läuft, solange die Bedingung (count <= 5) wahr ist
        while (count <= 5) {
            System.out.println("Schleifendurchlauf " + count);
            count++; // Inkrementieren der Zählvariable
        }

        System.out.println("Schleife beendet");
    }
}

```

<br>

### **Do-While-Schleife**
Wenn man weiß, dass die Schleife auf jeden Fall mindestens einmal ausgeführt werden soll, dann kann man statt einer While-Schleife auch eine Do-While-Schleife einsetzen. Eine Do-While-Schleife ist im Grunde genommen nichts Anderes, als eine While-Schleife bei der die Schleifen-Bedingung am Ende der Schleife und nicht am Anfang steht.

<br>

### **Iterator:** 
In Java ist ein "Iterator" ein Objekt, das zur Durchführung von Iterationen über eine Sammlung (wie z.B. eine Liste oder ein Set) verwendet wird. Der Iterator ermöglicht es, die Elemente der Sammlung nacheinander zu durchlaufen, ohne die zugrunde liegende Datenstruktur zu ändern.

Der Iterator bietet normalerweise folgende Methoden:

- hasNext(): Überprüft, ob es noch weitere Elemente in der Sammlung gibt, die durchlaufen werden können.

- next(): Gibt das nächste Element in der Sammlung zurück und bewegt den Iterator zum nächsten Element.

- remove(): Entfernt das zuletzt zurückgegebene Element aus der Sammlung (nicht immer unterstützt).

Der Iterator ermöglicht eine einfache und sichere Möglichkeit, über Elemente in einer Sammlung zu iterieren, ohne sich um die Details der internen Implementierung der Sammlung kümmern zu müssen. Dies erleichtert die Schleifen- und Iterationslogik in Java-Programmen.

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class IteratorExample {
    public static void main(String[] args) {
        // Erstellen einer Liste von Integer-Werten
        List<Integer> numbers = new ArrayList<>();
        numbers.add(1);
        numbers.add(2);
        numbers.add(3);
        numbers.add(4);
        numbers.add(5);

        // Erzeugen eines Iterators für die Liste
        Iterator<Integer> iterator = numbers.iterator();

        // Iteration über die Liste und Ausgabe der Elemente
        while (iterator.hasNext()) {
            Integer number = iterator.next();
            System.out.println(number);
        }
    }
}
```

<br>

### "Signalfluss"
Java Code -> via Compiler into -> Bytecode -> via Interpreter (JVM) into -> Maschienencode


## Was ist die Compiletime? (Java)
In Java bezieht sich die Compile-Time auf den Zeitpunkt, zu dem der Java-Quellcode (.java-Dateien) vom Java-Compiler (javac) in Bytecode (.class-Dateien) umgewandelt wird. Während der Compile-Time:

1. **Syntaxprüfung**: Der Compiler prüft den Code auf korrekte Syntax gemäß den Java-Sprachspezifikationen.
2. **Typüberprüfung**: Der Compiler überprüft Typen und wirft Fehler oder Warnungen bei Typinkompatibilitäten.
3. **Übersetzung**: Quellcode wird in plattformunabhängigen Java-Bytecode übersetzt, der auf jeder Maschine mit einer JVM ausgeführt werden kann.
4. **Annotation Processing**: Annotationen im Code können verarbeitet und entsprechende Aktionen ausgeführt werden.
5. **Generics**: Typ-Erasure-Prozess findet statt, wobei generische Typen in rohe Typen umgewandelt werden.

Compile-Time-Fehler müssen behoben werden, bevor der Code erfolgreich in Bytecode übersetzt und ausgeführt werden kann.

<br>

## Was ist die Runtime?
Die Runtime in Java bezieht sich auf den Zeitraum, in dem das Java-Programm ausgeführt wird. Dies beginnt, wenn die Java Virtual Machine (JVM) den kompilierten Bytecode lädt und endet, wenn das Programm beendet wird. Während der Runtime:

1. **Ausführung**: Die JVM führt den Bytecode aus, der während der Compile-Time generiert wurde.
2. **Speicherverwaltung**: Die JVM verwaltet den Speicher, insbesondere die Zuweisung und Freigabe von Speicher im Heap für Objekte.
3. **Garbage Collection**: Die JVM führt Garbage Collection aus, um nicht mehr verwendete Objekte zu entfernen und Speicher freizugeben.
4. **Exception Handling**: Laufzeitfehler (Exceptions) werden erkannt und können abgefangen werden, um eine angemessene Fehlerbehandlung zu ermöglichen.
5. **Dynamische Bindung**: Methodenaufrufe werden zur Laufzeit aufgelöst (Late Binding), was Polymorphismus ermöglicht.
6. **Just-In-Time (JIT) Kompilierung**: Ein JIT-Compiler kann Bytecode in Maschinencode übersetzen, während das Programm läuft, um die Ausführungsgeschwindigkeit zu verbessern.

Die Runtime-Phase ist kritisch für die Leistung und das Verhalten des Java-Programms.

<br>

## primitive Datentypen

| Datentyp  | Größe (in Bits) | Wertebereich                 | Beispiel          |
|-----------|-----------------|------------------------------|--------------------|
| `byte`    | 8               | -128 bis 127                 | `byte b = 10;`     |
| `short`   | 16              | -32,768 bis 32,767           | `short s = 100;`   |
| `int`     | 32              | -2,147,483,648 bis 2,147,483,647 | `int i = 1000;`   |
| `long`    | 64              | sehr große Ganzzahlen        | `long l = 100000L;`|
| `float`   | 32              | Fließkommazahlen mit einfacher Genauigkeit | `float f = 3.14f;` |
| `double`  | 64              | Fließkommazahlen mit doppelter Genauigkeit | `double d = 3.14159;` |
| `char`    | 16              | Unicode-Zeichen               | `char c = 'A';`    |
| `boolean` | -               | `true` oder `false`           | `boolean flag = true;` |

<br>

## statischer VS dynamischer Datentyp

"Statischer Datentyp" und "dynamischer Datentyp" sind Begriffe, die sich auf die Art und Weise beziehen, wie Datentypen in der Programmierung behandelt werden. Da Java eine typisierte Sprache ist, werden die "Vorteile" von dynamischen Datentypen erst mithilfe von Generics einsetzbar. 

Hier ist eine Erklärung für beide Begriffe:

### Statischer Datentyp:

- Ein statischer Datentyp ist ein Datentyp, der zur Compile-Zeit festgelegt wird und während der Laufzeit unverändert bleibt.

- In statisch typisierten Programmiersprachen wie Java, C++ und C# werden Datentypen in der Regel explizit deklariert und zur Compile-Zeit überprüft. Der Compiler erkennt und überprüft, ob die Variablen und Ausdrücke den erwarteten statischen Datentypen entsprechen.

- Statische Datentypen bieten Sicherheit und Fehlererkennung zur Compile-Zeit, da sie sicherstellen, dass bestimmte Operationen nur auf kompatiblen Datentypen durchgeführt werden können.

```java
int x = 5; // Die Variable 'x' hat den statischen Datentyp 'int' (ganze Zahl).
```

### Dynamischer Datentyp: ((Generics))
- Ein dynamischer Datentyp ist ein Datentyp, der zur Laufzeit festgelegt wird und sich während der Ausführung eines Programms ändern kann.

- Wenn man die Vorteile von dynamischen Datentypen in Java nutzen möchten, können Sie generische Datentypen (Generics) verwenden, um flexiblere Datenstrukturen zu erstellen. Generics erlauben es, parametrisierte Klassen und Methoden zu definieren, die mit verschiedenen Datentypen arbeiten können. Hier ist ein einfaches 

Beispiel:

```java
public class Container<T> {
    private T value;

    public Container(T value) {
        this.value = value;
    }

    public T getValue() {
        return value;
    }
}

public class Main {
    public static void main(String[] args) {
        Container<Integer> integerContainer = new Container<>(42);
        Container<String> stringContainer = new Container<>("Hallo, Welt!");

        int intValue = integerContainer.getValue();
        String stringValue = stringContainer.getValue();

        System.out.println(intValue);
        System.out.println(stringValue);
    }
}
```

<br>

## Was sind Operatoren?
Operatoren sind eine Art Bindeglied beim Programmieren. Sie dienen dazu, bestimmte Code-Elemente (Variablen, Methoden, Objekte, etc) auf die gewüschte Art und Weise zu verbinden.

| Kategorie              | Operatoren                                  | Beschreibung                                      |
|------------------------|---------------------------------------------|---------------------------------------------------|
| Arithmetische Operatoren | `+`, `-`, `*`, `/`, `%`, `++`, `--`           | Für mathematische Berechnungen.                   |
| Vergleichsoperatoren    | `==`, `!=`, `>`, `<`, `>=`, `<=`             | Zum Vergleichen von zwei Werten.                  |
| Logische Operatoren     | `&&`, `\|\|`, `!`                            | Für boolesche Logik.                              |
| Bitweise Operatoren     | `&`, `\|`, `^`, `<<`, `>>`, `>>>`            | Operieren auf den Bits von Ganzzahlen.            |
| Zuweisungsoperatoren    | `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `^=`, `<<=`, `>>=`, `>>>=` | Weisen Werte zu Variablen zu.                     |
| Sonstige Operatoren     | `? :`, `instanceof`, `->`                    | Bedingter Operator, Typvergleich, Lambda-Ausdrücke. |

<br>

## Was bedeutet `main`

In Java ist "main" eine spezielle Methode, die als Einstiegspunkt für die Ausführung eines Java-Programms dient. Die Signatur der `main`-Methode sieht normalerweise wie folgt aus:

```java
public static void main(String[] args)
```
Die main-Methode wird beim Starten eines Java-Programms aufgerufen und ist der erste Code, der ausgeführt wird. Sie enthält die Anweisungen, die das Programm ausführen soll. Java-Anwendungen beginnen ihre Ausführung in der main-Methode und von dort aus können weitere Methoden aufgerufen werden, um den Programmfluss zu steuern und Aufgaben auszuführen.

In der `main`-Methode in Java steht `(String[] args)` für die Parameterliste der Methode. Diese Parameter dienen dazu, Informationen an das Java-Programm zu übergeben, wenn es gestartet wird.

- `String[]`: Dieser Teil definiert ein Array von Zeichenketten (Strings), in dem die übergebenen Argumente gespeichert werden. Diese Argumente können beim Programmstart aus der Kommandozeile eingegeben werden.

- `args`: Dies ist der Name des Parameters. Sie können einen anderen Namen verwenden, aber `args` ist eine gängige Konvention.

Wenn Sie beispielsweise Ihr Java-Programm von der Kommandozeile aus mit `java MeinProgramm arg1 arg2` aufrufen, werden `arg1` und `arg2` in das String-Array `args` übergeben, und Sie können auf diese Werte innerhalb Ihrer `main`-Methode zugreifen, um Ihr Programm entsprechend zu steuern.


<br>


## Was bedeutet `void`
In Java steht "void" für einen Rückgabetyp, der in Methoden verwendet wird. Wenn eine Methode den Rückgabetyp "void" hat, bedeutet dies, dass die Methode keinen Wert zurückgibt. Sie führt bestimmte Anweisungen aus, kann aber keine Daten als Ergebnis zurückgeben. In anderen Worten, sie hat keine Rückgabeanweisung wie `return Wert;`. Void-Methoden werden oft für Aufgaben verwendet, die keine Rückgabe erfordern, wie das Drucken von Informationen auf der Konsole oder das Ändern des Zustands eines Objekts.



<br>

## Was bedeutet `equals`
`equals` ist eine Methode in Java, die in der Object-Klasse definiert ist und von abgeleiteten Klassen überschrieben werden kann. Sie wird verwendet, um den inhaltlichen Vergleich von Objekten auf Gleichheit basierend auf ihren Attributen oder Inhalten durchzuführen. Der Standardvergleich in Java (ohne Überschreibung) entspricht einem Vergleich der Referenzen auf Objekte, nicht ihrem Inhalt.

<br>

## Was bedeutet das Keyword: `final`

1. **Variablen**: Eine `final` Variable kann nach der Initialisierung nicht neu zugewiesen werden. Sie wird effektiv zu einer Konstante.
2. **Methoden**: Eine `final` Methode kann in keiner Unterklasse überschrieben werden.
3. **Klassen**: Eine `final` Klasse kann nicht erweitert werden, d.h., man kann keine Unterklasse davon erstellen.

<br>

## Scanner
Wir dazu verwendet, um Benutzereingaben von der Konsole oder anderen Eingabequellen zu lesen. Der Scanner erleichtert das Einlesen von Daten, die vom Benutzer eingegeben werden, und deren Verarbeitung in Java-Programmen.

- **Einlesen von Benutzereingaben:** Mit dem Scanner können Sie Benutzereingaben von der Konsole lesen. Zum Beispiel können Sie Zahlen, Zeichenketten oder andere Datentypen eingeben.

- **Parsen von Eingaben:** Der Scanner bietet Methoden zum Parsen von Eingaben in verschiedene Datentypen, z.B. nextInt() zum Lesen einer Ganzzahl, nextDouble() zum Lesen einer Gleitkommazahl und so weiter.

- **Trennzeichen:** Sie können den Scanner so konfigurieren, dass er Eingaben anhand von Trennzeichen, wie Leerzeichen oder Zeilenumbrüchen, in Teile aufteilt.

- **Fehlerbehandlung:** Der Scanner bietet Mechanismen zur Fehlerbehandlung, z.B. können Sie auf falsch formatierte Eingaben reagieren und den Benutzer erneut zur Eingabe auffordern.


BSP - Benutzereingaben lesen:
```java
import java.util.Scanner;

public class ScannerExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Erstellen eines Scanner-Objekts zur Eingabe von der Konsole
        System.out.print("Geben Sie eine Ganzzahl ein: ");
        int number = scanner.nextInt(); // Einlesen einer Ganzzahl
        System.out.println("Sie haben die Zahl " + number + " eingegeben.");
        scanner.close(); // Schließen des Scanner-Objekts, um Ressourcen freizugeben
    }
}
```

<br>

## Parsen

"Parsen" in Java bezieht sich auf den Prozess des Konvertierens einer Zeichenkette (String) oder anderer Eingabe in einen anderen Datentyp oder ein anderes Datenformat. Das Parsen ermöglicht es, Rohdaten aus einer Zeichenkette zu extrahieren und in ein geeignetes Datenformat zu überführen, damit sie in einem Programm verwendet werden können.

Beispiele für das Parsen in Java sind:

- **String in Ganzzahl konvertieren:**
```java
String zahlAlsText = "42";
int zahl = Integer.parseInt(zahlAlsText); // Parsen der Zeichenkette zu einer Ganzzahl
```
- **Zeichenkette in Gleitkommazahl konvertieren:**
```java
String zahlAlsText = "3.14";
double zahl = Double.parseDouble(zahlAlsText); // Parsen der Zeichenkette zu einer Gleitkommazahl
```
- **Datum und Uhrzeit aus Zeichenkette extrahieren:**
```java
String datumAlsText = "2023-11-09 14:30:00";
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
Date date = dateFormat.parse(datumAlsText); // Parsen der Zeichenkette zu einem Datum und einer Uhrzeit
```
- **JSON- oder XML-Daten analysieren:**
Das Parsen wird häufig verwendet, um Daten aus JSON- oder XML-Dateien zu extrahieren und in Datenstrukturen oder Objekte zu überführen, die in Java verwendet werden können.

Das Parsen ist wichtig, um Eingaben von Benutzern oder externe Daten in einem Programm zu verarbeiten, da sie häufig als Zeichenketten vorliegen und in die erforderlichen Datentypen oder Datenstrukturen umgewandelt werden müssen, um sinnvoll damit arbeiten zu können. Es ist jedoch wichtig, beim Parsen auf die richtige Formatierung und Fehlerbehandlung zu achten, um unerwartete Probleme zu vermeiden.

<br>


## Was bedeutet: Casten (Typenumwandlung)

In Java bezieht sich "Casten" auf den Vorgang, eine Variable oder einen Ausdruck von einem Datentyp zu einem anderen zu konvertieren. Dies wird auch als "Typumwandlung" bezeichnet. Das Casting ermöglicht es, den Datentyp einer Variable oder eines Ausdrucks gezielt zu ändern, um bestimmte Operationen durchzuführen oder Kompatibilität zwischen Datentypen sicherzustellen.

Es gibt zwei Arten des Castings in Java:

1. **Implizites Casting (Automatisches Casting):** Hierbei wird ein kleinerer Datentyp in einen größeren umgewandelt, ohne dass zusätzlicher Code erforderlich ist. Dies geschieht, wenn der Zieltyp den Quelltyp umfassen kann, ohne Datenverlust oder Genauigkeitsverlust zu verursachen.

```java
int zahl1 = 42;
double zahl2 = zahl1; // Implizites Casting von int zu double
```
<br>

2. **Explizites Casting (Manuelles Casting):** Hierbei wird ein Datentyp manuell in einen anderen umgewandelt, wenn ein größerer Datentyp in einen kleineren oder ein komplexerer Datentyp in einen einfacheren umgewandelt werden soll. Dies erfordert die Verwendung eines Casting-Operators und kann zu Datenverlust oder Genauigkeitsverlust führen.

```java
double zahl1 = 3.14;
int zahl2 = (int) zahl1; // Explizites Casting von double zu int (Genauigkeitsverlust)
```

Das Explizite Casting erfordert die Verwendung von Klammern und dem gewünschten Datentyp in Klammern, gefolgt von der Variable oder dem Ausdruck, der umgewandelt werden soll.

Es ist wichtig zu beachten, dass beim Expliziten Casting Datenverlust oder Rundungsfehler auftreten können, wenn die Genauigkeit des Zieltyps nicht ausreicht, um die gesamte Information des Quelltyps zu speichern. Daher sollte Casting vorsichtig und mit Bedacht eingesetzt werden, insbesondere wenn es zu Datenverlusten kommen kann.


---

# Thema: Exceptions

<br>

Exceptions in Java sind Ereignisse, die während der Ausführung eines Programms auftreten und den normalen Fluss der Anweisungen stören. Sie sind Objekte, die ein Problem signalisieren, wie z.B. ein Versuch, eine Datei zu öffnen, die nicht existiert, oder eine Division durch Null. Exceptions bieten eine strukturierte Möglichkeit, Fehler zu erkennen und zu behandeln, indem sie den Fehler an einen Teil des Programms weiterleiten, der dafür ausgelegt ist, damit umzugehen.

### Hauptarten von Exceptions:


1. **Checked Exceptions**: Diese sind Exceptions, die zur Compile-Time überprüft werden. Sie müssen entweder mit einem `try-catch`-Block behandelt oder mit `throws` in der Methodensignatur deklariert werden. Beispiele sind `IOException`, `SQLException`.

2. **Unchecked Exceptions**: Diese sind Exceptions, die zur Runtime auftreten und von der Klasse `RuntimeException` abgeleitet sind. Sie müssen nicht explizit in einem `try-catch`-Block gefangen oder deklariert werden. Beispiele sind `NullPointerException`, `ArrayIndexOutOfBoundsException`.

<br>

Zusätzlich gibt es noch `Errors`, die von der Klasse `Error` abgeleitet sind und normalerweise außerhalb des Kontrollbereichs des Programms liegen (z.B. `OutOfMemoryError`, `StackOverflowError`). Sie werden in der Regel nicht vom Programm behandelt, da sie auf schwerwiegende Probleme in der Java-Laufzeitumgebung hinweisen.


**Exceptions/Probleme lassen sich oft nicht vermeiden. Beim Programmieren muss man sich bewusst entscheiden, wie man mit ihnen umgehen will. Das bewusste Umgehen mit Exceptions wird "Exception Handling" genannt.**



### Exception Handling: `try` und `catch`

- **try-Block**: Hier platziert man den Code, von dem man erwartet, dass er eine Exception auslösen könnte. Wenn innerhalb des `try`-Blocks eine Exception auftritt, wird die Ausführung dieses Blocks beendet, und die Kontrolle wird an den entsprechenden `catch`-Block übergeben.

- **catch-Block**: Dieser Block wird verwendet, um die Exception zu fangen und zu behandeln, die im `try`-Block aufgetreten sein könnte. Man kann mehrere `catch`-Blöcke haben, um verschiedene Arten von Exceptions zu fangen. Jeder `catch`-Block kann eine spezifische Aktion durchführen, basierend auf der Art der gefangenen Exception.

```java
try {
    // Code, der eine Exception auslösen könnte
    int division = 10 / 0;
} catch (ArithmeticException e) {
    // Code zur Behandlung der ArithmeticException
    System.out.println("Es gab einen Fehler beim Teilen durch Null.");
}
```

### 11 Häugie Exceptions

| Exception-Klasse                | Beschreibung                                                                 |
|---------------------------------|------------------------------------------------------------------------------|
| NullPointerException            | Zugriff auf ein Objekt mit dem Wert `null`.                                  |
| ArrayIndexOutOfBoundsException  | Zugriff auf einen Array-Index außerhalb der Grenzen des Arrays.              |
| ClassCastException              | Versuch, ein Objekt in einen inkompatiblen Typ umzuwandeln.                  |
| IllegalArgumentException        | Eine Methode erhält einen unangemessenen oder unzulässigen Argumentwert.     |
| ArithmeticException             | Arithmetische Ausnahmesituation, z.B. Division durch Null.                   |
| IOException                     | E/A-Fehler, z.B. beim Lesen oder Schreiben von Dateien.                      |
| FileNotFoundException           | Eine Datei, die gelesen oder geschrieben werden soll, wurde nicht gefunden.  |
| NumberFormatException           | String kann nicht in einen numerischen Typ umgewandelt werden.               |
| InterruptedException            | Ein schlafender oder blockierter Thread wird unterbrochen.                   |
| NoSuchMethodException           | Eine reflektierte Methode wurde nicht gefunden.                              |
| NoSuchFieldException            | Ein reflektiertes Feld wurde nicht gefunden.                                 |

<br>

## Was bedeutet das Keyword: `throw`
Das Schlüsselwort `throw` in Java wird benutzt, um eine Exception manuell auszulösen. Man verwendet es, um ein `Exception`-Objekt zu erzeugen und dann das Programm zu zwingen, den normalen Ablauf zu unterbrechen und zum nächsten passenden `catch`-Block zu springen, der diese Art von Exception behandeln kann. Wenn kein solcher `catch`-Block existiert, wird das Programm beendet und die Exception wird auf der Konsole ausgegeben.

```java
public void checkAge(int age) {
    if (age < 18) {
        throw new IllegalArgumentException("Zugriff verweigert - Du musst mindestens 18 Jahre alt sein.");
    }
}
```

### Verwechslungsgefahr (`throw` VS `throws`)
- `throw` wird verwendet, um eine einzelne Exception explizit zu werfen.
- `throws` wird in einer Methodensignatur deklariert, um anzugeben, dass eine Methode möglicherweise eine oder mehrere Exceptions werfen kann.

<br>

---

# Thema: Objekt Orientiertes Programmieren - OOP

<br>

## Was sind die vier Säulen der OOP?

Die vier Säulen der Objektorientierten Programmierung (OOP) sind:

1. **Abstraktion**: https://www.w3schools.com/java/java_abstract.asp
2. **Kapselung/Encapsulation**: https://www.w3schools.com/java/java_encapsulation.asp
3. **Vererbung**: https://www.w3schools.com/java/java_inheritance.asp
4. **Polymorphismus**: https://www.w3schools.com/java/java_polymorphism.asp

## Hier zwei Aufzählungen, um eigene Schlüsse zu ziehen:

1. **Abstraktion**: Klassen, Interfaces, Abstrakte Methoden.
2. **Kapselung**: Zugriffsmodifikatoren (private, protected), Getter/Setters, Datenversteckung.
3. **Vererbung**: Superklasse, Subklasse, `extends`-Schlüsselwort, Methodenüberschreibung.
4. **Polymorphismus**: Methodenüberladung, Methodenüberschreibung, dynamische Bindung, Interface.

---

1. **Abstraktion**: Datenmodelle, Vereinfachung, Designebene.
2. **Kapselung**: Klassenstruktur, Information Hiding, Verantwortungstrennung.
3. **Vererbung**: `super`, Hierarchie, Basisklasse, abgeleitete Klasse.
4. **Polymorphismus**: Schnittstellen, abstrakte Klassen, Typumwandlung, späte Bindung.

Aber für die meisten Diskussionen, insbesondere in einem Bewerbungsgespräch, sollten die zuerst genannten Schlüsselwörter ausreichen, um ein grundlegendes Verständnis der OOP-Prinzipien zu demonstrieren.

<br>

## Zugrifsmodifikatoren: Keywords: `public`, `private` und `protected`

### `private` (OOP)
`private` in Java ist ein Zugriffsmodifikator, der verwendet wird, um den Zugriff auf Methoden, Variablen und Konstruktoren auf die Klasse zu beschränken, in der sie deklariert sind. In der OOP sollte so viel Code als nur möglich `private` sein (siehe: Kapselung)

<br>

### `public` (OOP)
`public` in Java ist ein Zugriffsmodifikator, der die höchste Ebene des Zugriffs bietet. Wenn eine Klasse, Methode, Konstruktor oder Variable als `public` deklariert wird, bedeutet das:

1. **Zugänglichkeit**: Diese Elemente sind von jeder anderen Klasse aus zugänglich, unabhängig davon, in welchem Paket sie sich befinden.
2. **Schnittstelle**: `public` wird oft verwendet, um eine API oder eine Service-Schnittstelle zu definieren, die für andere Klassen zugänglich sein soll.
3. **Nutzung**: Für Klassen und Interfaces, die weit verbreitet verwendet werden sollen, ist `public` die typische Wahl.

<br>

### `protected` (OOP)
`protected` in Java ist ein Zugriffsmodifikator, der eine mittlere Ebene des Zugriffs zwischen `public` und `private` bietet:

1. **Zugriff innerhalb der Klasse**: Mitglieder, die als `protected` deklariert sind, können innerhalb ihrer eigenen Klasse aufgerufen werden.
2. **Zugriff in Subklassen**: `protected` Mitglieder können von jeder Subklasse aus aufgerufen werden, auch wenn sich die Subklasse in einem anderen Paket befindet.
3. **Paketzugriff**: `protected` ermöglicht auch den Zugriff von anderen Klassen im selben Paket, ähnlich wie der Standardzugriffsmodifikator (kein Modifikator).


<br>

## Getter und Setter 

...werden in Java verwendet, um die Prinzipien der Kapselung umzusetzen, indem sie kontrollierten Zugriff auf die Eigenschaften eines Objekts bieten.


## get()
Eine "Getter"-Methode in Java, oft auch als Zugriffsmethode bezeichnet, ist eine öffentliche Methode, die den Wert einer privaten Variablen zurückgibt. Sie ermöglicht kontrollierten Zugriff auf die Werte der Eigenschaften eines Objekts.


## set()
Eine "Setter"-Methode in Java ist eine öffentliche Methode, die es ermöglicht, den Wert einer privaten Variablen zu setzen oder zu ändern. Sie dient dazu, den Wert einer Eigenschaft unter Einhaltung von Geschäftsregeln oder Validierungslogik zu aktualisieren.

### Superklasse

```java
public class Person {
    private String name; // Private Variable

    // Getter-Methode für 'name'
    public String getName() {
        return name;
    }

    // Setter-Methode für 'name'
    public void setName(String newName) {
        this.name = newName;
    }
}
```
### Subclass

```java
public class TestPerson {
    public static void main(String[] args) {
        Person person = new Person();
        
        // Setzt den Namen der Person mit der Setter-Methode
        person.setName("Alice");
        
        // Ruft den Namen der Person mit der Getter-Methode ab
        String personName = person.getName();
        
        System.out.println(personName); // Gibt "Alice" aus
    }
}
```

<br>

## Was bedeutet das Keyword: `static` (OOP)
`static` in Java bedeutet, dass das betreffende Mitglied (Variable, Methode, Block oder verschachtelte Klasse) zur Klasse gehört und nicht zu einer Instanz der Klasse. Wesentliche Punkte dazu:

1. **Klassenlevel**: `static` Mitglieder werden auf Klassenebene gespeichert, es gibt nur eine Kopie davon, unabhängig davon, wie viele Objekte erstellt werden.
2. **Zugriff**: `static` Mitglieder können ohne Erstellung eines Objekts der Klasse aufgerufen werden.
3. **Speicher**: `static` Variablen werden im Speicherbereich für statische Daten abgelegt und existieren ab dem Zeitpunkt des Klassenladens bis zum Ende des Programms.
4. **Methoden**: `static` Methoden können nur andere `static` Methoden direkt aufrufen und nur auf `static` Daten zugreifen.


<br>

## Was ist ein Konstruktor? (OOP)
Ein Konstruktor ist eine spezielle Methode in einer Klasse, die automatisch aufgerufen wird, wenn ein Objekt dieser Klasse erstellt wird. Er wird verwendet, um die Initialisierung von Objekten durchzuführen.

- **Aufruf anderer Konstruktoren:** Innerhalb eines Konstruktors kann mit this() ein anderer Konstruktor derselben Klasse aufgerufen werden.

- **Aufruf von Elternkonstruktoren:** Mit `super()` kann der Konstruktor der Superklasse aufgerufen werden.

- **Überladung:** Ein überladender Konstruktor ist, wenn eine Klasse mehrere Konstruktoren mit unterschiedlichen Parametern hat.

<br>

## Was bedeutet das Keyword: `this` (OOP)
Das Schlüsselwort `this` in Java ist eine Referenz auf das aktuelle Objekt, innerhalb dessen Methode oder Konstruktor der Code ausgeführt wird. 

Es wird häufig verwendet, um:

- Aktuelle Klassenvariablen von lokalen Variablen zu unterscheiden, wenn sie denselben Namen haben.
- Einen anderen Konstruktor derselben Klasse aufzurufen.
- Eine Methode aufzurufen oder eine Variable des aktuellen Objekts zu referenzieren.
- Das aktuelle Objekt als Rückgabewert zu verwenden.


## Was bedeutet das Keywort: `super` (OOP)
Bezieht sich immer auf die direkte Elternklasse (Methoden, Konstruktoren und Variablen)

- **Zugriff auf Methoden:** Es kann verwendet werden, um Methoden der Elternklasse aufzurufen, die von der aktuellen Klasse überschrieben wurden.
- **Zugriff auf Konstruktoren:** In einem Konstruktor ruft super() den Konstruktor der Elternklasse auf. Wenn verwendet, muss es die erste Anweisung im Konstruktor sein.
- **Zugriff auf Variablen:** Es kann auch verwendet werden, um auf Mitgliedsvariablen der Elternklasse zuzugreifen, die von der aktuellen Klasse verdeckt werden.

<br>

## Was bedeutet das Keyword: `abstract` (OOP)
`abstract` in Java wird verwendet, um eine Klasse oder Methode als abstrakt zu deklarieren:

1. **Abstrakte Klasse**: Eine Klasse, die nicht instanziiert werden kann. Sie dient als Basisklasse für andere Klassen und kann abstrakte sowie konkrete Methoden enthalten.
2. **Abstrakte Methode**: Eine Methode ohne Implementierung. Abstrakte Methoden müssen in den Unterklassen, die die abstrakte Klasse erweitern, überschrieben und implementiert werden.

<br>

# **Interfaces** - Schnittstellen (`implements`, `@Override`)
Ein Interface in Java ist ein Referenztyp, ähnlich einer Klasse, und ist eine Sammlung von abstrakten Methoden (Methoden ohne Körper) und Konstanten. Ab Java 8 können Interfaces auch Default- und statische Methoden enthalten.

Ein Interface definiert eine Art Vertrag oder Spezifikation, die von Klassen implementiert werden kann. Wenn eine Klasse ein Interface implementiert, muss sie alle Methoden des Interfaces implementieren (sofern diese nicht als Default- oder statische Methoden definiert sind).

1. **Methodendeklarationen**: Interfaces können abstrakte Methoden, Standardmethoden (mit Implementierung) und statische Methoden enthalten.
2. **Implementierung**: Eine Klasse, die ein Interface implementiert, muss alle seine abstrakten Methoden implementieren.
3. **Mehrfachvererbung**: Eine Klasse kann mehrere Interfaces implementieren, was eine Form der Mehrfachvererbung ermöglicht.
4. **Verträge**: Interfaces stellen einen Vertrag dar, den implementierende Klassen erfüllen müssen, was die Entkopplung von Komponenten fördert.

### Anwendungsbeispiele

1. **Normale Interfaces**: Enthalten abstrakte Methoden, die von implementierenden Klassen definiert werden müssen.
2. **Funktionale Interfaces**: Enthalten genau eine abstrakte Methode und können mit Lambda-Ausdrücken verwendet werden (z.B. `Runnable`, `Callable`).
3. **Marker-Interfaces**: Enthalten keine Methoden oder Felder und signalisieren dem JVM oder Frameworks bestimmte Verhaltensweisen (z.B. `Serializable`, `Cloneable`).
4. **Erweiterte Interfaces (Subinterfaces)**: Können andere Interfaces erweitern, um neue Methoden hinzuzufügen oder bestehende zu modifizieren.
5. **Nested Interfaces**: Interfaces, die innerhalb einer Klasse oder eines anderen Interfaces definiert sind.
6. **Standardmethoden-Interfaces**: Erlauben die Implementierung von Methoden mit einem Standardverhalten, das von implementierenden Klassen übernommen oder überschrieben werden kann.
7. **Statische Methoden-Interfaces**: Erlauben die Definition von statischen Methoden innerhalb eines Interfaces.

Umgangssprachlich könnte man ein Interface in Java als eine Art Vertragsvorlage beschreiben, die festlegt, welche Methoden eine Klasse implementieren muss, ohne vorzugeben, wie die Details der Implementierung aussehen sollen. Es ist wie eine Liste von "Dingen", die eine Klasse tun können muss, wobei das "Wie" der Klasse überlassen bleibt, die das Interface "unterschreibt" (implementiert).

### **Vorteile/Warum  Interfaces!?**

* **Abstraktion:** Interfaces bieten eine hohe Ebene der Abstraktion. Sie erlauben es Ihnen, eine Methode zu definieren, die in der Klasse, die das Interface implementiert, implementiert werden muss, ohne dass Sie sich um die Einzelheiten der Implementierung kümmern müssen.

* **Mehrfachvererbung:** Im Gegensatz zu Klassen können Interfaces in Java Mehrfachvererbung unterstützen. Eine Klasse kann mehrere Interfaces implementieren, was in Java der einzige Weg ist, Mehrfachvererbung zu erreichen.

* **Lose Kopplung:** Interfaces helfen dabei, Systemkomponenten lose zu koppeln. Wenn Klassen über Interfaces und nicht direkt miteinander kommunizieren, können Änderungen an einer Klasse ohne Auswirkungen auf andere Klassen vorgenommen werden.

* **Polymorphismus:** Interfaces unterstützen Polymorphismus, da ein Objekt in vielen Formen präsentiert werden kann. Wenn eine Klasse ein Interface implementiert, kann sie als das Interface-Typ behandelt werden.

* **Wiederverwendbarkeit** und Austauschbarkeit von Code: Wenn Klassen auf Interface-Typen statt auf konkrete Klassen programmieren, können verschiedene Implementierungen des Interfaces ausgetauscht und wiederverwendet werden, was die Flexibilität und Wartbarkeit des Codes erhöht.

* **Unterstützung für Callbacks:** Mit Hilfe von Interfaces kann Java das Konzept der Rückrufe (Callbacks) implementieren, das in anderen Programmiersprachen durch Funktionen höherer Ordnung oder Funktionszeiger erreicht wird.

* **Unterstützung für Lambda-Ausdrücke:** Ab Java 8 unterstützt das Konzept des funktionalen Interfaces (ein Interface mit genau einer abstrakten Methode) die Verwendung von Lambda-Ausdrücken für eine sauberere und prägnantere Syntax.

<br>

## Was bedeutet das Keyword: `implements`
`implements` in Java wird in einer Klassendefinition verwendet, um anzugeben, dass die Klasse die Methoden eines bestimmten Interfaces implementieren wird. Es signalisiert, dass die Klasse alle abstrakten Methoden des Interfaces definieren und Verhalten gemäß den Spezifikationen des Interfaces bereitstellen muss. Eine Klasse kann auch mehrere Interfaces implementieren.

<br>

## Was bedeutet das Keyword: `extends`
`extends` in Java wird verwendet, um anzugeben, dass eine Klasse (die Unterklasse) die Eigenschaften und Verhaltensweisen einer anderen Klasse (die Superklasse) erbt. Bei Interfaces wird `extends` verwendet, um ein Interface zu erweitern, d.h., ein neues Interface kann ein anderes Interface erweitern und dessen Methoden erben oder zusätzliche Methoden hinzufügen.

<br>

## `@Override` (OOP)

Das `@Override`-Annotation in Java gibt an, dass die markierte Methode eine Methode überschreibt, die in einer Superklasse deklariert ist. Es dient mehreren Zwecken:

1. **Korrekturprüfung**: Es informiert den Compiler, dass die Absicht besteht, eine Methode der Elternklasse zu überschreiben. Wenn die Superklasse keine solche Methode hat, die überschrieben werden kann, erzeugt der Compiler einen Fehler.
2. **Lesbarkeit**: Es verbessert die Lesbarkeit des Codes, indem es anderen Entwicklern klar macht, dass die Methode eine Überschreibung ist.
3. **Wartbarkeit**: Es hilft bei der Wartung des Codes, da es zukünftige Änderungen an der Superklasse, die die überschriebenen Methoden betreffen könnten, leichter erkennbar macht.

<br>

---

# Thema: Datenstrukturen

Datenstrukturen sind verschiedene Arten der Organisation von Daten in einem Computer, um diese effizient zu nutzen. Eines der wichtigsten Themen, die auch in allen anderen Programmiersprachen in ähnlicher Form relevant sind.

<br>

## Array VS ArryList (dynamisches Array)

In Java unterscheidet sich ein "Array" von einem "dynamischen Array" in Bezug auf ihre Größe und Flexibilität:

### Array:
- Ein Array in Java ist eine statische Datenstruktur, bei der die Größe (Anzahl der Elemente) bei der Erstellung festgelegt wird und nicht geändert werden kann.
- Die Größe eines Arrays ist in der Regel fest und kann nicht zur Laufzeit verändert werden.
- Arrays können verwendet werden, um Elemente desselben Datentyps zu speichern, und sie bieten einen effizienten Zugriff auf die Elemente über ihren Index.


Beispiel statischen Arrays:

```java
int[] staticArray = new int[5]; // Array mit einer festen Größe von 5 Elementen
```

### Dynamisches Array (ArrayList):

- Ein dynamisches Array, oft als ArrayList in Java bezeichnet, ist eine flexible Datenstruktur, bei der die Größe zur Laufzeit dynamisch geändert werden kann.
- ArrayList ist Teil des Java Collections Framework und bietet Methoden zum Hinzufügen, Entfernen und Bearbeiten von Elementen.
Im Gegensatz zu statischen Arrays kann ein ArrayList wachsen oder schrumpfen, um neue Elemente aufzunehmen oder Elemente zu entfernen.

Beispiel ArrayList:
```java
import java.util.ArrayList;

ArrayList<Integer> dynamicArray = new ArrayList<>(); // Ein dynamisches Array ohne feste Größe
dynamicArray.add(1); // Element hinzufügen
dynamicArray.remove(0); // Element entfernen
```

Zusammengefasst: Ein Array in Java hat eine feste Größe, die bei der Erstellung festgelegt wird, während ein dynamisches Array (z.B. ArrayList) eine flexible Größe hat und zur Laufzeit geändert werden kann. Die Wahl zwischen den beiden hängt von den Anforderungen Ihres Programms ab.

<br>

## `List`
`List` in Java ist eine geordnete Sammlung, die es ermöglicht, Elemente zu speichern, auf sie zuzugreifen und sie zu durchlaufen. Elemente können dupliziert werden und der Zugriff erfolgt über einen Index.

- **Dynamische Größe**: Im Gegensatz zu Arrays, deren Größe statisch ist, können Listen ihre Größe dynamisch anpassen, wenn Elemente hinzugefügt oder entfernt werden.
- **Elementzugriff**: Man kann auf jedes Element über einen Index zugreifen (ähnlich wie bei Arrays) und Elemente an einer bestimmten Position in der Liste einfügen oder entfernen.
- **Duplikate erlaubt**: Listen erlauben duplizierte Elemente, d.h., das gleiche Objekt kann mehrmals in der Liste vorkommen.
- **Geordnet**: Die Elemente in einer Liste behalten ihre Einfügereihenfolge bei, was bedeutet, dass man durch die Liste in der Reihenfolge iterieren kann, in der die Elemente eingefügt wurden.

Implementierungen der `List`-Schnittstelle wie `ArrayList` und `LinkedList` bieten konkrete Mechanismen zur Speicherung von Elementen.

## LinkedList
Eine "LinkedList" ist eine Datenstruktur in Java, die aus einer Reihe von Elementen besteht, die miteinander verknüpft sind. Jedes Element (Knoten) enthält eine Verweis auf das nächste Element in der Liste. LinkedLists ermöglichen das Einfügen und Entfernen von Elementen in konstanter Zeit, sind jedoch weniger effizient beim Zugriff auf Elemente anhand eines Index (im Vergleich zu Arrays). LinkedLists sind Teil des Java Collections Frameworks und bieten flexiblere Möglichkeiten für das Hinzufügen und Entfernen von Elementen als Arrays.


## Stack
Ein "Stack" ist eine Datenstruktur in Java und anderen Programmiersprachen, die nach dem Prinzip "Last-In, First-Out" (LIFO) funktioniert. Das bedeutet, dass das zuletzt hinzugefügte Element als erstes entfernt wird. In Java wird der Call Stack verwendet, um Methodenaufrufe und Rückkehradressen zu verfolgen. Es gibt auch die Datenstruktur `Stack`, die in Java genutzt werden kann, um Elemente zu stapeln und zu verarbeiten.


## Queue
Eine "Queue" ist eine Datenstruktur in Java, die eine geordnete Sammlung von Elementen speichert. Sie folgt dem Prinzip "First-In, First-Out" (FIFO), wobei das zuerst eingefügte Element als erstes entfernt wird. In Java wird die Schnittstelle `Queue` in der Java Collections Framework verwendet, und es gibt verschiedene Implementierungen wie `LinkedList` und `PriorityQueue`, die für verschiedene Anwendungsfälle geeignet sind.


## HashMap
Eine `HashMap` ist eine Datenstruktur in Java, die zur Speicherung und Verwaltung von Schlüssel-Wert-Paaren verwendet wird. Sie bietet schnellen Zugriff auf Werte anhand eines eindeutigen Schlüssels und ermöglicht das Speichern von Daten in Form einer Hashtabelle. `HashMap` erlaubt keine doppelten Schlüssel und ist Teil des Java Collections Frameworks.








<br>

# Zusatz

## `final` VS `static`

`final` und `static` sind zwei unterschiedliche Konzepte in Java:

- `final` wird verwendet, um eine Konstante zu deklarieren, eine Methode, die nicht überschrieben werden kann, oder eine Klasse, die nicht erweitert werden kann.
- `static` bezieht sich auf das Klassenniveau. Statische Mitglieder gehören zur Klasse selbst und nicht zu einer spezifischen Instanz.

Hier sind die Hauptunterschiede:

1. **Zuweisung**:
   - `final` Variablen müssen genau einmal initialisiert werden und können danach nicht mehr geändert werden.
   - `static` Variablen können mehrmals zugewiesen werden, aber es gibt nur eine Kopie dieser Variablen, die von allen Instanzen der Klasse geteilt wird.

2. **Zugriff**:
   - `final` Mitglieder werden über Instanzen der Klasse oder direkt über die Klasse zugegriffen, wenn sie auch `static` sind.
   - `static` Mitglieder werden über den Klassennamen zugegriffen, ohne dass eine Instanz der Klasse erstellt werden muss.

3. **Vererbung**:
   - `final` Methoden können nicht überschrieben werden, was bedeutet, dass die Funktionalität in Unterklassen nicht geändert werden kann.
   - `static` Methoden können verdeckt werden, aber nicht im traditionellen Sinne von Polymorphismus überschrieben werden, da sie nicht an eine Instanz gebunden sind.

4. **Designabsicht**:
   - Die Verwendung von `final` zeigt an, dass der Wert oder das Verhalten nicht geändert werden soll.
   - Die Verwendung von `static` zeigt an, dass das Mitglied auf Klassenebene existiert und von allen Instanzen geteilt wird.
