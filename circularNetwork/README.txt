1. Cały projekt można uruchomić poleceniem nrngui circularInit.hoc
2. Opis modelu: Model jest skonstruowany ze 125 neuronów (zgodnie ze specyfikacją projektu 3.) losowo rozmieszczonych w kuli o promieniu 1
3. Istnieją różne pliki z zestawami stałych: 
    constants.hoc               - 
    noise.hoc                   - 
    period_constants.hoc        -
    prolonged_short_input.hoc   -
Żeby wywołać model z innym zestawem stałych należy wykomentować odpowiednią linijkę z xopen("...") w pliku circularInit.hoc i odkomentować z odpowiednim zestawem stałych.
4. Opisy pozostałych plików:
    neuronIAF.hoc           - szablon neuronu
    createNetworkCells.hoc  - plik, w którym zostały stworzone neurony z podziałem na hamujące i pobudzające
    createConnections.hoc   - tworzy połączenia pomiędzy neuronami
    networkRasterGraph.hoc  - tworzenie rasterplotu
    counter.hoc             - dodanie do rasterplotu czerwonej linii, która ma zwizualizować liczbę pobudzeń w danej jednostce czasu 
                              (przedział czasowy zdefiniowany przez stałą STEPS_FORWARD)
    addGraphs.hoc           - taki sam jak na zajęciach