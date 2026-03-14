# Aufgabe 1

Der Datensatz enthält den Verlauf des Aktienkurses einer Aktie aller Handelstage von 2010 bis 2018. Der Datensatz hat sieben Spalten:

•	Date: Datum

•	Open: Eröffnungskurs

•	High: Höchster Kurs an dem Tag

•	Low: Niedrigster Kurs an dem Tag

•	Close: Finaler Kurs an dem Tag (Schlusskurs)

•	Adj Close: Angepasster Schlusskurs (Weitere Infos: https://www.investopedia.com/terms/a/adjusted_closing_price.asp)

•	Volume: Handelsvolumen

Für die Vorhersage nehmen Sie nun 3 bis 8 Schlusskurse (Spalte Close), um daraus den Kurs am 9ten Tag (bzw. Folgetag) vorherzusagen. Beispiel: 

Nehmen Sie die Schlusskurse (Close) drei vorheriger Tage als unabhängige Variablen und den Schlusskurs des vierten Tages als abhängige Variable:

•	Unabhängige Variable: 2010-01-04: 133.899994

•	Unabhängige Variable: 2010-01-05: 134.690002

•	Unabhängige Variable: 2010-01-06: 132.250000

•	Abhängige Variable: 2010-01-07: 130.000000

Teilaufgabe a)

Erstellen Sie nun aus dem Rohdatensatz mit 2261 Zeilen einen neuen Datensatz mit 3-8 unabhängigen Variablen/Spalten (probieren Sie verschiedene Varianten aus, funktioniert es besser wenn Sie drei Tage nehmen oder 5 oder 8 Tage?) und einer abhängigen Variable. Der neue Datensatz sollte je nach Anzahl der unabhängigen Variablen zwischen 2253 bis 2258 Zeilen haben. 




Teilaufgabe b)

Nutzen Sie nun die sklearn (Scikit-learn) Funktion „train_test_split“, um ein Trainingsdatenset und Testdatensetz zu erstellen. Erstellen Sie ein neuronales Netz mit 3-8 Eingabe Neuronen und einem Ausgabeneuronen für eine Regression. Der Ausgabelayer hat eine lineare Aktivierungsfunktion. Die „loss“ Funktion für den Optimierer ist „mean_squared_error“. Versuchen Sie den mittleren quadratischen Fehler unter 260 zu bringen.

Teilaufgabe c)

Erstellen Sie nun eine normale Regression mit Hilfe der Funktion „LinearRegression“ aus sklearn (Scikit-learn) für die Aktienvorhersage welches Sie schon mit dem neuronalen Netz gelöst haben. Was sehen Sie für Unterschiede und was schließen Sie daraus? Macht es Sinn eine Ridge oder Lasso Regression anzuwenden: https://scikit-learn.org/stable/modules/linear_model.html#ordinary-least-squares
Warum? Warum nicht? Diskutieren Sie mögliche Vorteile und Nachteile. 

# Aufgabe 2

In dieser Aufgabenstellung arbeiten Sie mit dem „Cardiotocography Data Set“ (https://archive.ics.uci.edu/ml/datasets/Cardiotocography). Sie können den Datensatz entweder direkt von der Website runterladen oder aus dem Akad Online Bereich zu diesem Modul die Datei „CTG.xls“ nutzen. 

Öffnen Sie die Datei zuerst mit Excel und machen sich mit dem Aufbau des Datensatzes vertraut. Eine Erklärung finden Sie in dem Datenblatt „Description“ der Exceldatei. Ziel ist es nun mit einer 92% Genauigkeit auf einem Testdaten Set die Klassifikation NSP zu lernen (Datenblatt „Raw data“, Spalte „AN“). Dabei entscheiden Sie welcher Algorithmus am besten geeignet ist. Der Algorithmus muss nicht erklären, wie die Klassifikation zustande gekommen sie. Sie können also eine normale Regression nehmen, eine SVC, einen Entscheidungsbaum oder ein neuronales Netz, oder einen anderen Klassifizierungsalgorithmus. 

Wichtig ist nur, dass Sie folgende Schritte implementieren und zeigen:

•	Das Laden der Daten mit „pandas“

•	Prüfen ob es fehlende Daten gibt

•	Erklären Sie die Auswahl ihrer unabhängigen Merkmale (Features)

•	Erläutern Sie, warum Sie sich für den von Ihnen ausgesuchten Algorithmus entschieden haben.

•	Nutzen Sie die Funktion GridSearchCV aus sklearn (Scikit-Learn): https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html, um mindestens einen Parameter ihres Models automatisch optimieren zu lassen. 

•	Führen Sie das Training durch und zeigen Sie eine Klassifikationsgenauigkeit mindestens 92%
