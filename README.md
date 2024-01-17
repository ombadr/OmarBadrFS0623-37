# Typescript

## Spiegazione generica (Cos'è, a cosa serve, che problema risolve, differenze con JS semplice)

E' un linguaggio di programmazione open-source sviluppato da Microsoft. E' un superset di Javascript, il che significa che qualsiasi codice Javascript è anche codice Typescript valido.

La sua principale caratteristica è il suo sistema di tipizzazione statica. Permette al programmatore di specificare i tipi di variabili direttamente nel codice sorgente.

Questo controllo di tipizzazione offre i seguenti vantaggi:

- Miglioramento della qualità del codice: Aiuta ad individuare errori come assegnazioni di tipi incompatibili o chiamate di metodi non esistenti durante la fase di sviluppo, invece che in fase di esecuzione.
- Maggiore leggibilità e manutenibilità: Il codice con tipi espliciti è più facile da leggere e comprendere, soprattutto in grandi progetti.

Rispetto a Javascript, Typescript richiede una fase di compilazione in cui il codice TypeScript viene "trascompilato" in Javascript puro.

## Il compilatore TS (perché è necessario? e come si usa?)

Il compilatore Typescript è necessario per convertire il codice Typescript, che include tipizzazione statica e altre funzionalità non standard, in Javascript puro che può essere eseguito nei browser o in ambienti come Node.js

Si usa tipicamente tramite linea di comando. Dopo aver installato Typescript tramite NPM, puoi usare il comando `tsc` seguito dal nome del file (es: `tsc myfile.ts`). Questo processo compila il file Typescript (`miofile.ts`) in un file Javascript (`miofile.js`), traducendo tutte le funzionalità specifiche di Typescript in codice Javascript standard.

## La Type Inference

E' un meccanismo per cui il compilatore deduce automaticamente il tipo di una variabile o di un'espressione basandosi sul suo valore o contesto di utilizzo. Per esempio, se assegni `let numero = 5`, Typescript capisce che `numero` è di tipo `number`. 

## Il tipo "any"

Il tipo "any" è utilizzato per indicare che una variabile può contenere un valore di qualsiasi tipo, evitando così il controllo di tipizzazione del compilatore. L'uso eccessivo di `any` può ridurre i vantaggi della tipizzazione statica di Typescript, poichè annulla i controlli di tipo che il linguaggio fornisce.

## Il tipo Union

Il tipo "Union", indicato il simbolo `|`, permette di definire una variabile che può contenere valori di due o più tipi diversi. Ad esempio, `let valore: number | string` significa che la variabile `valore` può essere sia un numero (`number`) sia una stringa (`string`).

## Il tipo Tuple

Il tipo "Tuple" permette di definire un array con un numero fisso di elementi di cui i tipi sono noti, ma non necessariamente uguali. Ad esempio, `[string, number]` rappresenta un arrat con esattamente due elementi: il primo di tipo `string` e il secondo di tipo `number`.

## Le Interfaces in TS

Le "Interfaces" sono strutture che definiscono la forma di un oggetto, specificando i nomi e i tipi delle sue proprietà, metodi ed eventuale ereditarietà. Sono usate per imporre una certa struttura su classi o oggetti. Non esistonon nel codice Javascript finale, poichè sono usate solo in fase di sviluppo per la verifica dei tipi.

## Types vs Interfaces

"Types" e "Interfaces" sono entrambi strumenti per definire la struttura degli oggetti, ma con alcune differenze:

- Interfaces: Sono estendbili e possono essere usate per dichiarare la forma di oggetti, inclusi metodi e proprietà. Le interfaces supportano l'ereditarietà, permettendo di estendere o implementare le interfaces.
- Types: Sono più versatili e possono rappresentare non solo la forma degli oggetti, ma anche unioni di tipi, tuple e altro. Non sono estendibili nello stesso modo delle interfaces.

## I "Generics"

I "Generics" in Typescript sono uno strumento che permette di creare componenti che possono lavorare su più tipi piuttosto che su un singolo tipo. Ciò è utile quando si vuole che una funzione, interfaccia o classe sia capace di gestire diversi tipi mantenendo la sicurezza dei tipi. Ad esempio, un Array generico `Array<T>` può essere un Array di numeri, stringhe, ecc., a seconda del tipo `T` specificato. L'uso dei Generics aumenta la riutilizzabilità e la flessibilità del codice mantenendo la sicurezza di tipizzazione.
