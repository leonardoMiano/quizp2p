Introduzione
Il progetto consiste in un gioco quiz basato su un'architettura server-client implementata in C++ per una macchina Unix. 
Il gioco consente a più giocatori di connettersi a un server centrale, rispondere alle domande del quiz e ricevere feedback in tempo reale.
La comunicazione tra il server e i client avviene tramite socket.

Struttura del Codice
Il codice del progetto è suddiviso in due componenti principali: il server (quiz.cpp) e il client (giocatori.cpp),
progettati per essere eseguiti su una macchina Unix.

Server (quiz.cpp)
Il server è responsabile della gestione delle connessioni dei giocatori, dell'invio delle domande del quiz e della valutazione delle risposte.
La struttura del codice prevede l'uso di thread per gestire ogni connessione dei giocatori in modo concorrente. La libreria pthread è stata inizialmente utilizzata per la gestione dei thread.

Client (client.cpp)
Il client permette ai giocatori di connettersi al server, inserire un username e rispondere alle domande del quiz. 
La comunicazione tra il server e il client avviene tramite socket. In questo progetto, il client è progettato per essere eseguito in più finestre, simulando così l'esperienza di più giocatori.

Topologia di Rete
Il gioco utilizza una topologia di rete client-server, dove il server funge da punto centrale di gestione del gioco e i clienti si connettono ad esso per partecipare al quiz.
La comunicazione tra il server e i client avviene tramite socket TCP/IP.

Funzionamento di Input/Output
Il server e i client comunicano attraverso i socket, consentendo lo scambio di messaggi tra di loro. 
Il server invia le domande del quiz ai client, riceve le risposte e fornisce feedback in base alle risposte corrette o errate. 
Il client interagisce con l'utente attraverso la console, richiedendo l'inserimento dell'username e visualizzando le domande del quiz e i messaggi del server.

Istruzioni per Giocare

Per giocare, segui i seguenti passaggi:

Compilazione del Codice:

Compila il codice del server (quiz.cpp) e del client (giocatori.cpp) utilizzando i comandi specificati.

Esecuzione del Server:

Esegui l'eseguibile del server sul tuo sistema. Assicurati che il server sia in ascolto su una porta specifica (predefinita: 8080).
Esecuzione del Client:

Esegui l'eseguibile del client su una o più finestre del terminale. Ogni finestra rappresenterà un giocatore simulato.

Inserimento dell'Username:

Inserisci un username quando richiesto dal client.

Rispondere alle Domande:

Rispondi alle domande del quiz inviate dal server. In caso di risposta corretta, il gioco continua con una nuova domanda. 
In caso di risposta errata, potresti essere temporaneamente disconnesso.
Esperienza Multi-Giocatore:

Puoi eseguire il client in più finestre per simulare più giocatori partecipanti al gioco.

Conclusioni

Il progetto offre un esempio di implementazione di un gioco quiz con un'architettura client-server in C++ per una macchina Unix. 
La suddivisione del codice tra server e client, l'uso dei socket per la comunicazione e la gestione dei thread contribuiscono a una struttura organizzata e funzionale. 
L'interazione semplice ma efficace consente una simulazione di gioco coinvolgente.
