<h2>Laboratorium 2 - sprawozdanie</h2>
<h3>Dominika Skolimowska, I2S2.4</h3>
<br />
Plik YAML, ktory jest manifestem deploymentu wykorzystujacego obraz serwera nginx w wersji 1.9, nosi nazwe <i>lab6.yaml</i>. Wdrozenie posiada typ proxy. Maksymalna liczba podow niedostepnych w czasie aktualizacji zostala ograniczona do 2 <i>maxUnavailable: 2</i>. 
<br />
W przypadku ustawienia <i>maxSurge: 3</i>, oznacza to, że w trakcie aktualizacji może być utworzonych maksymalnie 3 dodatkowe repliki, ponad liczbę replik zdefiniowaną jako docelowa liczba. Docelowa liczba replik została określona jako 5: <i>replicas: 5</i>.
<br />
Uruchomienie pliku: <i>kubectl apply -f lab6.yaml</i><br />
Informacje o deploymencie: <i>kubectl describe deployment nginx-deployment</i><br />
<image src="dep.png" /> <br />
Stan podow: <i>kubectl get pods</i> <br />
<image src="pods.png" />
