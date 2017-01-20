# Uczenie maszynowe języka za pomocą rekurencyjnych sieci neuronowych.

## keywords
rekurencyjne sieci neuronowe, nauczanie języka, torch-rnn, char-rnn, lua, torch, dokeryzacja

## streszczenie pomysłu
W pracy opiszę działanie oraz wybrane możliwości wykorzystania algorytmu autorstwa Adreja Karpathy'ego o nazwie char-rnn. Moją motywacją do napisania tej pracy była niepochamowana ciekawość dotycząca granic możliwości współczesnej informatyki. Zastanawiało mnie, czy w sztuczny sposób zaimplementowane modele matematyczne są w stanie osiągnąć aż taką wydajność aby mogły one zacząć posługiwać się ludzkim językiem pisanym, który przecież do tej pory był dla nich niedostępny. Algorytm który opisałem w tej pracy realizuje wielopoziomową rekurencyjną sieć neuronową (RNN, LSTM oraz GRU) która potrafi nauczyć się posługiwać językiem z poziomu pojedyńczych liter. Innymi słowy model ten potrzebuje pliku tekstowego na wejściu, następnie Rekurencyjna Sieć Neuronowa uczy się przewidywać kolejne litery w sekwencjach słów. Sieci te mogą zostać użyte do wygenerowania tekstu litera po literze który będzie przypominał oryginalne treningowe dane. W pracy podejmę próbę odpowiedzi na następujące pytania: Czy ten algorytm może zostać wykorzystany do generowania tekstów, które będą przypominać teksty napisane przez człowieka? Czy da się w ten sposób "nauczyć" sieć neuronową posługiwania się językiem polskim? Oraz wreszczie: Czy sieci neuronowe mogą zostać wykorzystane do generowania treści (np. z użyciem języka znaczników). Pomniejszym problemem poruszonym w pracy będzie omówienie optymalnej specyfikacji sprzętowej którą można użyć do "trenowania sieci" oraz implementacja tego algorytmu w języku Lua z użyciem frameworku Torch. 

## spis treści
1. Przedmowa.
<br />1.1. Cel i zakres pracy.
<br />1.2. Streszczenie pracy.
2. Sieci neuronowe.
<br />2.1. Rekurencyjne sieci neuronowe (LSTM).
3. Algorytm torch-rnn.
<br />3.1. Opis algorytmu.
<br />3.2. Implementacja.
4. Eksperyment 1: Generowanie treści artykułów na wikipedii.
<br />4.1. Przebieg eksperymentu.
<br />5.2. Porównanie wydajności procesu trenowania w zależności od wyboru architektury procesorów.
<br />&nbsp;&nbsp;&nbsp;&nbsp;5.2.1. Tradycyjne procesory wielordzeniowe.
<br />&nbsp;&nbsp;&nbsp;&nbsp;5.2.1. Architektura nVidia CUDA.
5. Eksperyment 2: ... <i>(TO DO)</i>
6. Podsumowanie wyników pracy oraz wnioski.
<br />6.1. Podsumowanie.
<br />6.1. Przewidywania na temat przyszłości.
7. Zakończenie.

## bibliografia

<br />[1] Ryszard Tadeusiewicz. <i>Sieci neuronowe.</i> Warszawa, 1993.
<br />[2] Nick Bostrom. <i>Superintelligence: Paths, Dangers, Strategies.</i> US, 2014.
<br />[3] Christopher Olah. <i>Understanding LSTM Networks.</i> http://colah.github.io/posts/2015-08-Understanding-LSTMs/
<br />[4] TensorFlow. (<i>kto?</i>) <i>Recurrent Neural Networks.</i> https://www.tensorflow.org/tutorials/recurrent/
<br /><i>to do: wzbogacić bibliografię.</i>


## pozostałe linki
referat: http://slides.com/michaljakobowski/c

torch-rnn na GitHub: https://github.com/jcjohnson/torch-rnn

char-rnn na GiTHub: https://github.com/karpathy/char-rnn

http://www.itreseller.pl/technologie/257-docker-kontenery

http://www.ai.c-labtech.net/sn/sneuro.html
