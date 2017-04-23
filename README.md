# Generowanie treści przy pomocy rekurencyjnych sieci neuronowych

## keywords
rekurencyjne sieci neuronowe, nauczanie języka, torch-rnn, char-rnn, lua, torch, dokeryzacja

## przedmowa
Motywają do napisania pracy magisterskiej jest chęć poznania stosunowo młodego zagadnienia w informatyce jakim są sieci neuronowe. Sztuczna inteligencja już od początku powstania informatyki rozpalała umysły autorów książek science-fiction. Już w latach 50' Alan Turing zaproponował sposób w jaki moglibyśmy powołać do życia sztuczną inteligencję. Chodzi tu o propozycję tak zwanego umysłu dziecka. Turing uważał, że lepiej byłoby stworzyć jeden prosty model działania umysłu dziecka, a dopiero później przy pomocy precesu nauczania uzyskać model zbliżony do działania umysłu osoby dorosłej. Tego typu metodologia działania jest zawarta w idei tworzenia sieci neuronowych. Zastanawiające jest, czy implementacja modeli matematycznych jakimi są sieci neuronowe jest w stanie posługiwać się ludzkim językiem naturalnym w stopniu przypominającym żywą osobę? To pytanie zostało podjęte w tej pracy, aby na nie odpowiedzieć wykorzystano implementacje rekurencyjnych sieci neurownych zaproponowaną przez Andreja Karpathy'ego.

W pracy podejmę próbę odpowiedzi na następujące pytania: Czy ten algorytm może zostać wykorzystany do generowania tekstów, które będą przypominać teksty napisane przez człowieka? Czy da się w ten sposób "nauczyć" sieć neuronową posługiwania się językiem polskim? Oraz wreszczie: Czy sieci neuronowe mogą zostać wykorzystane do generowania treści (np. z użyciem języka znaczników czy języków programowania obiektowego).

## streszczenie pomysłu
W pracy zostało opisane działanie oraz wybrane możliwości wykorzystania modelu rekurencyjnych sieci neuronowych autorstwa Adreja Karpathy'ego, udoskonalonego przez Justina Johnsona. Model ten nosi nazwę Torch-rnn i jego kod źródłowy jest dostępny na platformie github. Jest on realizacją wielopoziomowej rekurencyjnej sieci neuronowej (RNN, LSTM oraz GRU) której działanie sprowadza się do dwóch etapów. Pierwszym jest etap treningowy - zadany zbiór danych (plik w formacie tekstowym) zostaje przetworzony w taki sposób aby Sieć Neuronowa niejako nauczyła się przewidywać kolejne litery w sekwencji słów tak aby w sumie utworzyły one zbiór możliwie jak najbliższy temu który został zadany jako zbiór testowy. Generowanie tych sekwencji odbywa się w drugim etapie, podczas którego z zapisanych w trakcie treningowych iteracji tzw. sampli generowny jest wyjściowy tekst.

Przy pomocy omawianej sieci neuronowej zostaje przeprowadzonych kilka eksperymentów prezentujących wybrane możliwości wykorzystania sieci neurnowych do generowania treści. Pierwszy ekesperyment pokazuje możliwości uproszczonej wersji sieci LSTM (Long short-term memory) z dwoma warstwami oraz 128 ukrytymi jednostkami (hidden units). Zbiorem treningowym dla tego eksperymentu jest zbiór wszystkich dramatów napisanych przez Willama Szekspira. W efekcie uzyskano sieć zdolną do generowania utworów podobnych do dramatu szekspirowskiego. Kolejny eksperyment przeprowadzono już na znacznie bardziej skomplikowanej sieci wykorzystującej 3 warstwy i 512 ukrytych jednostek (hidden units). Jako zbiór treningowy posłużył zbiór wszystkich powieści Henryka Sienkiewicza (oraz kilka jego wybranych opowiadań). W efekcie uzyskano bardziej zadowalające efekty, wygenerowane teksty znacznie bardziej przypominają swój pierwowzór. Trzeci eksperyment pokazuje w jaki sposób sieci neurnowe radzą sobie z generowaniem treści z wykorzystaniem języków znaczników. Zbiorem treningowym był kod źródłówy wybranych artykułów z platformy wikipedia. W efekcie sieć generuje treść przypominającą artykuły popularno-naukowe wraz z wykorzystaniem równań matematycznych. Czwarty eksperyment pokazuje sieć która potrafi generować kod źródłowy w wybranym języku programowania (W jakim?)...

W podsumowaniu przedstawione zostaje porównanie wydajności działania procesu treningowego w zależnośći użytej specyfikacji sprzętowej oraz stopnia skomplikowania użytej sieci. 

## spis treści
1. Przedmowa.
<br />1.1. Przedmowa.
<br />1.2. Streszczenie pracy.
2. Rekurencyjne sieci neuronowe (LSTM).
3. Algorytm torch-rnn.
<br />3.1. Opis algorytmu.
<br />3.2. Proces instalacji sieci Torch-RNN.
<br />3.3. Omówienie implementacji oraz wkładu własnego.
4. Eksperyment 1: Dramat szekspirowski (sieć LSTM, 2-warstwowa, 128 ukrytych jednostek).
<br />4.1. Przebieg eksperymentu.
5. Eksperyment 2: Powieści Henryka Sienkiewicza (sieć LSTM, 3-warstwowa, 512 ukrytych jednostek).
<br />5.1. Przebieg eksperymentu.
6. Eksperyment 3: Generowanie treści artykułów na wikipedii (sieć LSTM, 2-warstwowa, 128 ukrytych jednostek).
<br />6.1. Przebieg eksperymentu.
7. Eksperyment 4: Generowanie kodu źródłowego języka (?!) (sieć LSTM, TO DO ... ).
<br />7.1. Przebieg eksperymentu.
8. Porównanie wydajności procesu trenowania w zależności od wyboru architektury procesorów.
<br />8.1. Tradycyjne procesory wielordzeniowe.
<br />8.2. Architektura nVidia CUDA.
9. Podsumowanie wyników pracy oraz wnioski.
10. Bibliografia.

## bibliografia

<br />[1] Ryszard Tadeusiewicz. <i>Sieci neuronowe.</i> Warszawa, 1993.
<br />[2] Nick Bostrom. <i>Superintelligence: Paths, Dangers, Strategies.</i> US, 2014.
<br />[3] Christopher Olah. <i>Understanding LSTM Networks.</i> http://colah.github.io/posts/2015-08-Understanding-LSTMs/
<br />[4] TensorFlow. (<i>kto!?</i>) <i>Recurrent Neural Networks.</i> https://www.tensorflow.org/tutorials/recurrent/
<br />[5] Christopher Baurez. <i>Element-Research Torch RNN Tutorial for recurrent neural nets</i>. http://christopher5106.github.io/deep/learning/2016/07/14/element-research-torch-rnn-tutorial.html (<i>częściowo może być pomocny?</i>)
<br />[6] Andrej Karpathy. <i>The Unreasonable Effectiveness of Recurrent Neural Networks.</i> http://karpathy.github.io/2015/05/21/rnn-effectiveness/
<br /><i>to do: wzbogacić bibliografię.</i>


## pozostałe linki
referat: http://slides.com/michaljakobowski/c

torch-rnn na GitHub: https://github.com/jcjohnson/torch-rnn

char-rnn na GiTHub: https://github.com/karpathy/char-rnn

http://www.itreseller.pl/technologie/257-docker-kontenery

http://www.ai.c-labtech.net/sn/sneuro.html
