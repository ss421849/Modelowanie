1. Cały projekt można uruchomić poleceniem nrngui circularInit.hoc
2. Opis modelu: Model jest skonstruowany ze 125 neuronów (zgodnie ze specyfikacją projektu 3.) losowo (prawie jednorodnie) rozmieszczonych w kuli
3. Istnieją różne pliki z zestawami stałych: 
    constants.hoc               - Przykładowe stałe pokazujące odpowiedź sieci na losowe wejście tylko po 10 impulsów na każdą komórkę pobudzającą. Można zauważyć silną odpowiedź, która wygasa po dłuższym czasie.

    noise.hoc                   - Przykładowe stałe pokazujące działanie (szum) sieci przy stałym losowym wejściu do każdej komórki pobudzającej. Wejście jest obecne przez cały czas trwania symulacji.

    burst_period.hoc            - Przykładowe stałe pokazujące działanie sieci przy stałym losowym wejściu. Sieć pracuje cyklicznie, tzw. bursty.

    firm_period.hoc             - Przykładowe stałe pokazujące działanie sieci przy stałym losowym wejściu. Sieć pracuje cyklicznie, jednak w sposób bardziej ciągły niż burstowo.

    smooth_period.hoc           - Przykładowe stałe pokazujące działanie sieci przy stałym losowym wejściu. Sieć pracuje rytmicznie, co widać na wykresie chwilowych aktywacji. Praca jest gładka.

    prolonged_short_input.hoc   - Podobne do pliku "constants.hoc" lecz tutaj odpowiedź jest słabsza, mimo to nadal jest dość długa.

Żeby wywołać model z innym zestawem stałych należy wykomentować odpowiednią linijkę z xopen("...") w pliku circularInit.hoc i odkomentować z odpowiednim zestawem stałych.
4. Opisy pozostałych plików:
    neuronIAF.hoc           - szablon neuronu
    createNetworkCells.hoc  - plik, w którym zostały stworzone neurony z podziałem na hamujące i pobudzające
    createConnections.hoc   - tworzy połączenia pomiędzy neuronami
    networkRasterGraph.hoc  - tworzenie rasterplotu
    counter.hoc             - dodanie do rasterplotu czerwonej linii, która ma zwizualizować liczbę pobudzeń w danej jednostce czasu 
                              (przedział czasowy zdefiniowany przez stałą STEPS_FORWARD)
    addGraphs.hoc           - taki sam jak na zajęciach

Uwagi: Sieć jest bardzo niestabilna, drobne zmiany parametrów (stałych) prowadzą do znacznej zmiany zachowania. Częstymi zachowaniami są pełna praca sieci (wszystkie komórki gwałtownie pracują) lub szybkie wygaszenie sieci (najczęściej po wzmożonym okresie aktywacji)