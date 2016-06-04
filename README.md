# Uczenie maszynowe języka za pomocą rekurencyjnych sieci neuronowych.

## keywords
rekurencyjne sieci neuronowe, nauczanie języka, torch-rnn, char-rnn, lua, torch, dokeryzacja

## streszczenie projektu
W pracy opisałem działanie oraz wybrane możliwości wykorzystania algorytmu autorstwa Adreja Karpathy'ego o nazwie char-rnn. Moją motywacją do napisania tej pracy była niepochamowana ciekawość dotycząca granic możliwości współczesnej informatyki. Zastanawiało mnie, czy w sztuczny sposób zaimplementowane modele matematyczne są w stanie osiągnąć aż taką wydajność aby mogły one zacząć posługiwać się ludzkim językiem pisanym, który przecież do tej pory był dla nich niedostępny. Algorytm który opisałem w tej pracy realizuje wielopoziomową rekurencyjną sieć neuronową (RNN, LSTM oraz GRU) która potrafi nauczyć się posługiwać językiem z poziomu pojedyńczych liter. Innymi słowy model ten potrzebuje pliku tekstowego na wejściu, następnie Rekurencyjna Sieć Neuronowa uczy się przewidywać kolejne litery w sekwencjach słów. Rekurencyjna Sieć Neuronowa może zostać użyta do wygenerowania tekstu litera po literze który będzie przypominał oryginalne treningowe dane. W pracy podjąłem próbę odpowiedzi na następujące pytania: Czy ten algorytm może zostać wykorzystany do generowania tekstów, które będą przypominać teksty napisane przez człowieka? Czy da się w ten sposób "nauczyć" sieć neuronową posługiwania się językiem polskim? Oraz wreszczie: Czy sieć neuronowa jest w stanie tworzyć poezję albo w bardziej pesymistycznym scenariuszu: imitację poezji. Pomniejszym problemem prószonym w pracy jest omówienie implementacji tego algorytmu w języku Lua z użyciem frameworku Torch. 

## plan pracy
1. Wprowadzenie.
2. Streszczenie pracy.
3. Czym są rekurencyjne sieci neuronowe?
4. Zasada działania algorytmu torch-rnn.
5. Wybrane możliwości wykorzystania tego fenomenu:
..1. Dramat szekspirowski.
..2. Nauka języka polskiego.
..3. Cyfrowy podmiot liryczny, czyli sieci neuronowe piszą poezję.
6. Omówienie implementacji algorytmu.
7. Wnioski.


## linki
referat: http://slides.com/michaljakobowski/c

torch-rnn na GitHub: https://github.com/jcjohnson/torch-rnn

char-rnn na GiTHub: https://github.com/karpathy/char-rnn

http://www.itreseller.pl/technologie/257-docker-kontenery

http://www.ai.c-labtech.net/sn/sneuro.html
