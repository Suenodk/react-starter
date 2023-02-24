# Hello API
In deze challenge gaan we onze eigen Mosquito backend aanroepen om een uitvaartkist op te halen!

Succes!

## Opzet
Om API calls te maken gebruiken we Axios. Open een Terimal die in dezelfde folder staat waar de package.json van dit project staat en voer het volgende commando uit: `yarn add axios`

Gefeliciteerd! Je hebt nu Axios geïnstalleerd.

- Maak in de `src` folder een nieuwe folder genaamd `axios`
- Maak in de folder `axios` een file genaamd `clientAxios.ts`
- In de file `clientAxios.ts` voeg het volgende import statement toe: `import Axios from 'axios'`
- Maak nu een `export const` variabele genaamd `clientAxios` gebruik hiervoor de volgende guidelines: https://axios-http.com/docs/instance
- <b>`export const`</b> zorgt ervoor dat deze variabele in een ander file geïmporteerd kan worden
- Voor de BaseURL raadpleeg Team MUG
- Voeg nu een header toe voor voor elk request met behulp van `interceptors.request` gebruik hiervoor de volgende guidelines: https://axios-http.com/docs/interceptors hier staat uitgelegd hoe het werkt met een POST request: https://stackoverflow.com/questions/45578844/how-to-set-header-and-options-in-axios. Wij willen dit op <b>alle</b> requesten
- Voor de header waardes raadpleeg Team MUG

Good job! Nu hebben we een client voor Axios geconfigureerd om API calls te maken. Laten we een API call maken en deze tonen op de pagina!

- Open HelloWorld.tsx en maak een variabele aan genaamd `locationId` gebruik hiervoor de guidelines https://reactjs.org/docs/hooks-state.html
- Maak ook een state variabele aan genaamd `location`
- Open HelloWorld.tsx en maak een methode aan genaamd `getLocation` gebruik hiervoor de guidelines van https://reactjs.org/docs/hooks-reference.html#usecallback geef hierbij de state variabele `locationId` mee als dependency
- Importeer nu in dit component de `clientAxios` vanuit de `axios` folder. De import hiervan is vergelijkbaar met de import van het `HelloWorld` component in de `App.tsx` file
- Voeg een button toe op aan het component HelloWorld.tsx die de methode `GetLocation` aanroept
- Gebruik de clientAxios in de `getLocation` callback om een get request aan te roepen gebruik hiervoor de guidelines https://www.educative.io/answers/how-to-make-an-axios-get-request vang de response af in een variabele genaamd response
- Zet de waarde van de variabele `location` nu gelijk aan de waarde van `response`
- Zet in de render methode van het `HelloWorld.tsx` component de stringified waarde van de variabele `location`. Gebruik hiervoor `{JSON.stringify(location)}` gebruik hiervoor deze guidelines: https://thinkster.io/tutorials/rendering-variables-in-react