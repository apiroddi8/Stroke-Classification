Tale progetto è stato sviluppato nell’ambito del laboratorio di Big Data ed è incentrato sulla classificazione dell’insorgenza di ictus nei pazienti utilizzando diversi modelli di Machine Learning. L’analisi è stata condotta sullo Stroke Prediction Dataset, disponibile su [Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).
, e ha previsto un’ampia fase di pulizia e pre-elaborazione dei dati, oltre all’applicazione di tecniche avanzate per il bilanciamento delle classi e l’ottimizzazione dei modelli predittivi.

È possibile visionare il progetto ed il report anche su Google Drive al seguente [link](https://drive.google.com/drive/folders/1J0MxpK_KzfL4haCVDAzY55ibbiZvDK6t?usp=sharing)

Docente: Giuliano Armano

Autore: Alessandro Piroddi

L’obiettivo principale del lavoro è stato quello di identificare i fattori che possono influenzare il rischio di ictus e costruire modelli di classificazione capaci di prevedere l’evento con un buon livello di affidabilità. Per raggiungere questo scopo, i dati sono stati inizialmente esplorati attraverso un’analisi visiva, utilizzando strumenti come matplotlib, seaborn e plotly, al fine di comprendere la distribuzione delle variabili e individuare eventuali anomalie o valori mancanti. È emerso fin da subito uno squilibrio significativo tra le classi della variabile target, con una netta prevalenza di pazienti che non hanno mai avuto un ictus rispetto a quelli che lo hanno avuto.

Per migliorare la qualità del dataset, è stata eseguita un’accurata fase di pulizia, che ha incluso la gestione dei dati mancanti e la rilevazione degli outlier utilizzando la regola dell’Interquartile Range. Le variabili categoriche sono state codificate attraverso tecniche di string indexing e One Hot Encoding, mentre le variabili numeriche sono state trasformate utilizzando diversi metodi di scaling, tra cui il MinMax Scaler e il RobustScaler.

Un aspetto fondamentale dell’analisi ha riguardato la gestione dello sbilanciamento della variabile target. Per affrontare questa problematica sono state testate sia tecniche di undersampling che di oversampling, optando infine per la seconda, in modo da preservare il maggior numero di informazioni possibili senza ridurre il dataset.

Per la classificazione sono stati implementati diversi modelli di Machine Learning, tra cui la Regressione Logistica, il Decision Tree, la Random Forest, il Naive Bayes, il Gradient Boosted Trees e le Support Vector Machines. Ciascun modello è stato valutato in base a metriche specifiche come Precision, Recall e F1-score, poiché in un contesto di classi sbilanciate l’accuratezza da sola non è un indicatore affidabile. Nonostante l’adozione di strategie avanzate di bilanciamento, i modelli non hanno raggiunto performance ottimali, evidenziando difficoltà nella classificazione dei casi positivi.

Per migliorare i risultati sono stati sperimentati approcci di Ensemble Learning, come il Bagging e il Boosting, che hanno permesso di ottenere un lieve incremento della Precision, passando da un valore iniziale di 0,13 fino a 0,25 a seconda dei parametri utilizzati nella fase di tuning. Tuttavia, i risultati suggeriscono che per ottenere una classificazione più accurata sarebbe necessario ampliare il dataset, integrandolo con dati aggiuntivi reperibili attraverso il web scraping o altre fonti di open data.

L’intero progetto è stato sviluppato utilizzando PySpark per la gestione dei dati e l’implementazione degli algoritmi di classificazione. Per chiunque voglia riprodurre l’analisi o approfondire i dettagli metodologici, il codice è disponibile nel repository. È sufficiente clonare il progetto e installare le dipendenze necessarie per poter eseguire gli script.

Questo studio rappresenta un primo tentativo di applicare il Machine Learning al problema della previsione dell’ictus, ma i risultati ottenuti dimostrano quanto sia complesso affrontare un problema di classificazione con una forte sproporzione tra le classi. Ulteriori miglioramenti potrebbero essere ottenuti esplorando nuove architetture di modelli o utilizzando tecniche avanzate di Feature Selection per ridurre la dimensionalità del problema.
