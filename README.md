# Workshop - React Native
![Logo React](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png)
## Sommaire
### Partie théorique :
- **[Lien vers les slides](https://docs.google.com/presentation/d/1aprbfnAXfBVSbw0MCSaAIarE197XDdSNHpqg3IiU1dY/edit?usp=sharing)**
### Partie pratique, développement d'une appli mobile :
- **[Démo de l'appli](#demo)**
- **[Les installations](#installations)**
- **[L'appli: étape par étape](#appli)**
## La demo de l'appli <a id="demo"></a>
![](Gif-demoapp.gif)
## Les installations <a id="installations"></a>
Vérifier si npm est bien installé sur votre machine :

    npm -v
    
Si ce n'est pas le cas :

    npm install npm@latest -g
    
Pour installer react native (par l'intermédiaire d'expo)  :

    npm install -g expo-cli

Il faudra également installer une appli sur votre mobile :
"Expo" pour Android / "Expo Client" sur iOS

Ensuite, créez un dossier du nom de votre choix sur le bureau et puis allez dans ce dossier avec le terminal.

Une fois positionné dans ce dossier avec le terminal, on va générer un nouveau projet React Native :

    expo init my-app
(my-app étant le nom de l'appli que j'ai choisi, vous pouvez mettre autre chose).

Votre terminal va vous demander de faire un choix ('choose a template') :
Choisissez l'option 'Blank'.

Une fois l'installation terminée, se diriger vers le nouveau dossier créé :

    cd my-app
  
Et puis faire :

    npm start
(pour lancer le serveur de développement).

Pour terminer, ouvrez le contenu du dossier my-app dans votre éditeur de code.

## Développement de l'appli <a id="appli"></a>
