# Java 

## Soccer League 

Lies die SoccerLeague.csv ein und baue dir aus diesen Spielen eine League auf. 
Dafür solltest du für jede Zeile eine Instanz der Klasse "Game" erstellen und sie 
unserer TestLeague durch Aufruf der `addGameResult(newGame)` Methode hinzufügen.
In `addGameResult` müssen gegebenefalls neue Teams angelegt werden und für die jeweiligen Teams
muss `addGame` aufgerufen werden um das Spiel dem Team hinzuzufügen.

Die Klasse `Game` sollte folgende Attribute besitzen:
* Team homeTeam
* Team guestTeam
* int goalsForHomeTeam
* int goalsForGuestTeam
und folgende Methoden bereitstellen: 
* Team getHomeTeam()
* Team getGuestTeam()
* int getGoalsForHomeTeam()
* int getPointsForHomeTeam()
* int getGoalsForGuestTeam()
* int getPointsForGuestTeam()

Für einen Sieg liefert ein Spiel 3 Punkte, bei einem unentschieden gibt's einen Punkt und für eine Niederlage gibt es keine Punkte.
Die Punkte speichern wir nicht in einer Variable sondern wir sollten einfach im getPoints die anzahl der Tore für die Berechnung des Returnwerts heranziehen.

Die Klasse `Team` sollte folgende Attribute besitzen:
* String name
* List<Game> games
und folgende Methoden bereitstellen: 
* void addGame(Game game)
* String getName() 
* int getPoints() - returniert die Summe aller Punkte im spiel
* int getGoalDifference() - returniert die Differenz der Summe aller Tore und der Summe aller gegnerischen Tore
* int getWins() - returniert die Anzahl an gewonnen Spielen
* int getDraws() - returniert die Anzahl an unentschiedenen Spielen
* int getDefeats() - returniert die Anzahl an verlorenen Spielen
* int getGoalsShot() - returniert die Summe aller Tore
* int getGoalsReceived() - returniert die Summe aller gegnerischen Tore

Für all diese Methoden gilt es keine Variablen anzulegen sonder mit Hilfe von Streams
auf der games Liste die jeweiligen Zahlen zu errechnen.

Die Klasse `League` sollte folgende Attribute besitzen: 
* List<Team> teamTable
und folgende Methoden bereitstellen: 
* void addGameResult(Game game)
* List<Team> getTeamTable() 

⚠️ Wir brauchen also nur Getter und keine Setter! Es wäre gut wenn wir alle Variablen, deren Wert sich nicht mehr ändern kann nach konstruktion, `final` setzen.

Schreibe ausführliche Unit Tests!