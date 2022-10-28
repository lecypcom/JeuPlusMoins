# JeuPlusMoins

## CLASSES

- Score{ username, score }


## VARIABLES GLOABLES

- scores : array<Score>


## FONCTIONS

# Core
- newGame(playerName: string, difficulty: int) -> Initialise la partie en créant un générant un nombre aléatoire $mysteryValue
- checkValue(inputValue: int) -> Compare $mysteryValue avec inputValue

# Interface
- configGameRender() -> Demande le nom d'utilisateur et le nombre maximum (difficulté)
- startGameRender() -> Initialise l'interface de jeu et appelle newGame()
- checkValueRender() -> Indique le résultat de la comparaison après avoir appelé checkValue()
- endGameRender() -> Initialise l'écran final de la partie
- displayScoreRender() -> Appel displayScore() et affiche le tableau des scores 
- searchScore() -> Appel getScoreByName() et affiche la réponse

# Scoreboard
- savecode(username: string, score: int): [ position: int, isNewPosition: boolean ] -> Enregistre le score + nom du joueur, retourne la meilleure position actuelle dans le scoreboard (postion mise à jour a la suite de cette partie ou d'un précèdente et précisé la quand ce record a été fait : tableau[int position, bool newPosition])
- resetScore(): void -> Remet a zéro le LocalStorage
- displayScore(): array<Score> -> Retourne un tableau contenant les scores
- getScoreByName(playerName: string): Score -> A partir du nom d'un joueur (enregistré dans le tableau des parties/scores) retrouve son meilleur score