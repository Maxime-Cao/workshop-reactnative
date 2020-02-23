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

Une fois le serveur de développement lancé, une page web devrait s'ouvrir dans votre navigateur (à l'adresse localhost:19002) :
- Ouvrez l'application Expo sur votre téléphone
- Choisissez l'option "Scan QR Code" et scanner le code QR qui est sur la page web ouverte devant vous (localhost:19002)
- Un lien va se faire entre votre mobile et votre ordinateur. A chaque changement que vous allez faire dans votre code, vous en rendez un "rendu" en temps-réel

Pour terminer, ouvrez le contenu du dossier my-app dans votre éditeur de code.

## Développement de l'appli <a id="appli"></a>
### Création des dossiers et fichiers :
- A la racine du dossier créez un dossier 'app'
- Dans le dossier 'app', créez un dossier 'components'
- Dans le dossier 'components', créez deux fichiers (deux components) => Main.js / Note.js

### Le composant Main.js :
Copiez ce code dans Main.js :

    import React from  'react';
    import  {  StyleSheet,  Text,  View,  TextInput,  ScrollView,  TouchableOpacity  }  from  'react-native';
    import Note from  './Note';
    
    export  default  class  Main  extends  React.Component  {
    
	constructor(props)  {
	super(props);
	this.state  =  {
	noteArray: [],
	noteText:  "",
		}
	}

	render()  {

	let  notes  =  this.state.noteArray.map((val,  key)  =>  {
	return  <Note  key={key} keyval={key} val={val}  deleteMethod={()  =>  this.deleteNote(key)} />
	});

	return (
	
	<View  style={styles.container}>
		<View  style={styles.header}>
			<Text  style={styles.headerText}>- Mes notes -</Text>
		</View>