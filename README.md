# Praca Magisterska (algorytm char-rnn)
W pracy chciałbym opisać algorytm autorstwa Adreja Karpathy'ego o nazwie char-rnn. Algorytm ten realizuje wielopoziomową rekurencyjną sieć neuronową (RNN, LSTM oraz GRU) która potrafi nauczyć się posługiwać językiem z poziomu pojedyńczych liter. Innymi słowy model ten potrzebuje pliku tekstowego na wejściu, następnie Rekurencyjna Sieć Neuronowa uczy się przewidywać kolejne litery w sekwencjach słów.

Rekurencyjna Sieć Neuronowa może zostać użyta do wygenerowania tekstu litera po literze który będzie przypominał oryginalne treningowe dane.

Głównym problemem pracy będzie próba odpowiedzi na pytanie: Czy ten algorytm może zostać wykorzystany do generowania tekstów, które będą przypominać teksty napisane przez człowieka?Pomniejszymi problemami poruszanymi w pracy będzie omówienie programowanie w języku Lua z użyciem frameworku Torch oraz omówienie sposobu działania danego algorytmu, jego czasu działania oraz wyników wyjściowych. 
