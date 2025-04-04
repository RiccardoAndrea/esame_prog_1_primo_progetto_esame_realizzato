# Rubrica Telefonica con Criptografia

Questo progetto implementa un sistema di gestione di una rubrica telefonica in C su Linux, con funzionalità di crittografia dei dati sensibili. La rubrica permette di memorizzare, cercare, modificare e cancellare contatti telefonici. I contatti sono protetti da una crittografia a più livelli, e le chiavi di crittografia vengono gestite separatamente per garantire la sicurezza dei dati.

## Funzionalità

1. **Aggiunta di contatti**: Inserimento di nuovi contatti nella rubrica. I contatti vengono ordinati automaticamente in ordine alfabetico.
2. **Ricerca contatti**: Utilizzo della ricerca binaria per cercare un contatto in base al nome e cognome.
3. **Visualizzazione delle chiamate**: Ogni contatto ha un contatore che tiene traccia del numero di chiamate effettuate da o verso quel contatto.
4. **Effettuare chiamate**: Incremento del contatore delle chiamate per ogni chiamata effettuata a un contatto.
5. **Cancellazione di contatti**: Rimozione di un contatto dalla rubrica.
6. **Criptografia dei dati**: Tutti i dati sensibili (nome, cognome, numero di telefono) sono criptati con una chiave generata e gestita separatamente.

## Come funziona

### Archiviazione dei dati

I contatti vengono memorizzati in file separati:

- **contatti.txt**: Contiene i dati dei contatti, come nome, cognome e numero di telefono, criptati.
- **chiavi_contatti_criptate.txt**: Contiene le chiavi per la crittografia dei contatti.
- **chiavi_delle_chiavi.txt**: Contiene le chiavi per la crittografia delle chiavi.

### Crittografia

La crittografia viene realizzata tramite una semplice cifra basata sul codice ASCII dei caratteri. I contatti e le chiavi sono criptati in modo circolare per impedire la visualizzazione diretta dei dati.

### Funzioni principali

1. **inserisci_elemento()**: Inserisce un nuovo contatto, ordinato alfabeticamente.
2. **ric_bin_ric()**: Funzione ricorsiva di ricerca binaria per trovare un contatto in base al nome e cognome.
3. **trova_numero()**: Trova il numero telefonico di un contatto dato il nome e cognome.
4. **trova_chiamate()**: Restituisce il numero di chiamate effettuate verso o da un numero.
5. **chiamata()**: Incrementa il contatore delle chiamate per un contatto specificato.
6. **cancella_numero()**: Rimuove un contatto dalla rubrica.

## Compilazione e Esecuzione

### Prerequisiti

- Un sistema Linux
- Compilatore C (gcc)
- Librerie standard C

### Istruzioni per la compilazione

1. Clona il repository:
    ```bash
    git clone https://github.com/tuo-utente/rubrica-telefonica.git
    ```

2. Entra nella cartella del progetto:
    ```bash
    cd rubrica-telefonica
    ```

3. Compila il progetto:
    ```bash
    gcc -o rubrica main.c
    ```

4. Esegui il programma:
    ```bash
    ./rubrica
    ```

## Tecnologie Utilizzate
- C
- GTK per interfaccia

