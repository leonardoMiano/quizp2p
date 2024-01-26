\documentclass[a4paper, 12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{listings}
\usepackage{color}
\usepackage{xcolor}
\usepackage{geometry}
\usepackage{hyperref}

\geometry{a4paper, margin=1in}

\definecolor{codegreen}{rgb}{0,0.6,0}
\definecolor{codegray}{rgb}{0.5,0.5,0.5}
\definecolor{codepurple}{rgb}{0.58,0,0.82}
\definecolor{backcolour}{rgb}{0.95,0.95,0.92}

\lstdefinestyle{mystyle}{
    backgroundcolor=\color{backcolour},
    commentstyle=\color{codegreen},
    keywordstyle=\color{magenta},
    numberstyle=\tiny\color{codegray},
    stringstyle=\color{codepurple},
    basicstyle=\ttfamily\footnotesize,
    breakatwhitespace=false,
    breaklines=true,
    captionpos=b,
    keepspaces=true,
    numbers=left,
    numbersep=5pt,
    showspaces=false,
    showstringspaces=false,
    showtabs=false,
    tabsize=2
}

\lstset{style=mystyle}

\title{Documentazione del Progetto \\ \large Quiz Multiplayer con Server e Client}
\author{Tuo Nome}
\date{\today}

\begin{document}

\maketitle

\tableofcontents
\newpage

\section{Descrizione del Progetto}
In questo progetto, abbiamo sviluppato un'applicazione di quiz multiplayer che consente a giocatori di connettersi a un server, rispondere a domande e competere tra loro.

\section{Descrizione e Schema dell'Architettura}
L'architettura dell'applicazione è composta da un server centrale e client multipli. Il server gestisce le connessioni, invia domande e raccoglie le risposte dai client. Ogni giocatore è gestito in un thread separato per garantire un'esperienza di gioco sincronizzata.

\subsection{Schema dell'Architettura}
In Figura~\ref{fig:architecture}, è rappresentato lo schema generale dell'architettura del progetto.

\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{architecture_diagram.png}
    \caption{Schema dell'Architettura}
    \label{fig:architecture}
\end{figure}

\section{Dettagli Implementativi dei Client/Server}
Questa sezione discute i dettagli implementativi chiave dei componenti client e server.

\subsection{Server}
Il server utilizza il linguaggio di programmazione C++ e sfrutta la libreria di socket per la comunicazione TCP/IP. Ogni giocatore è gestito in un thread separato, condividendo le risorse in modo sincronizzato.

\lstinputlisting[language=C++, caption=Esempio di codice del server]{quiz_server.cpp}

\subsection{Client}
Il client, anch'esso implementato in C++, si connette al server, esegue il login con un nome utente e partecipa al gioco rispondendo alle domande del quiz.

\lstinputlisting[language=C++, caption=Esempio di codice del client]{quiz_client.cpp}

\section{Parti Rilevanti del Codice Sviluppato}
La parte rilevante del codice è stata inclusa nelle sezioni precedenti. Per una visione completa, fare riferimento ai file sorgente completi.

\section{Manuale Utente}
Questa sezione fornisce istruzioni su come compilare ed eseguire il progetto.

\subsection{Compilazione}
Per compilare il server:
\begin{lstlisting}[language=bash]
g++ -pthread quiz_server.cpp -o quiz_server
\end{lstlisting}

Per compilare il client:
\begin{lstlisting}[language=bash]
g++ -pthread quiz_client.cpp -o quiz_client
\end{lstlisting}

\subsection{Esecuzione}
Per eseguire il server:
\begin{lstlisting}[language=bash]
./quiz_server
\end{lstlisting}

Per eseguire il client:
\begin{lstlisting}[language=bash]
./quiz_client
\end{lstlisting}

\section{Conclusioni}
Questa documentazione fornisce una panoramica completa del progetto, compresi dettagli architetturali, parti rilevanti del codice e istruzioni per l'utente. L'applicazione di quiz multiplayer offre un'esperienza coinvolgente per i giocatori.

\end{document}
