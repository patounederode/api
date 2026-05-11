# Week 1
## wo 1 april
Mijn eerste idee: een film app met de MovieDB API. Ik wilde daarbij gebruik maken van paginaovergangen en de Web Share API. Ik heb gekeken naar voorbeelden op DLO

## Do 2 april
Voortgangsgesprek
Mijn idee bleek te simpel en te saai, nieuw idee bedenken.
Ik moest opnieuw nadenken over mijn concept en wat ik precies wilde maken. Daarna ben ik gaan kijken naar de lijst met API's https://developer.mozilla.org/en-US/docs/Web/API. Omdat ik toch graag iets met kunst wilde doen heb besloten  zelf de API van het rijksmuseum op de te zoeken. 
![Rijksmuseum api](/src/img/rijksmuseumapi.png)

## Vrij 3 april
Goede vrijdag

# Reflectie week 1:
In deze week ben ik begonnen met mijn eerste idee, maar ik kreeg tijdens de feedback dat het te simpel was. Daardoor moest ik opnieuw nadenken over wat ik ging maken. Uiteindelijk heb ik gekozen om iets met kunst te doen, wat beter bij mij past.

# Week 2
## wo 8 april
Ziek

## do 9 april
Ziek

## vrij 10 april
Ziek - geen voortgang gesprek.

# Reflectie week 2:
Deze week was ik ziek, dus heb ik niks kunnen doen aan mijn project. Daardoor liep ik achter op mijn planning. Toen ik weer begon, merkte ik dat ik meteen moest inhalen, wat best stress gaf. Voor volgende week wil ik meer hulp gaan vragen.

# WEEK 3
## wo 15 april
Ik ben begonnen met mijn nieuwe idee: een kunstapp. Ik wilde kunstwerken ophalen via een API, een favorietenpagina maken en detailpagina’s voor elk kunstwerk toevoegen. Mijn eerste poging was de Rijksmuseum API, maar die werkte helaas niet meer.
![Testen of api werkt](/src/img/testapi.png)
![Niet gevonden](/src/img/verwijderd.png)

Daarom heb ik een andere api gekozen, de Artic.edu API. 
!alt[](/src/img/chicagoapi.png)

Ook heb ik een pagina aangemaakt waarin je favorieten kunt opslaan met behulp van local storage. Hiervoor heb ik hulp gekregen van ChatGPT.

Deze code zorgt ervoor dat items op de pagina worden weergegeven en dat je ze kunt verwijderen.  
Wanneer je een item verwijdert, wordt de lijst meteen bijgewerkt in de browser via localStorage.

```javascript
// Zet het item op de pagina
list.appendChild(li);

const btn = document.getElementById(`delete-${index}`);

// Als je op de knop klikt:
btn.addEventListener("click", () => {
  // Verwijder 1 item op deze plek
  favorites.splice(index, 1);

  // Slaat de nieuwe lijst op in localStorage
  localStorage.setItem("favorites", JSON.stringify(favorites));

  // Laat de lijst zien
  renderFavorites();
});
```

## do 16 april
Vandaag heb ik Canvas api gebruikt. Met behulp van mdn:
https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API

```html
<canvas id="canvas" width="600" height="400" style="border:1px solid black;"></canvas>
```
Hiermee kon ik aangeven hoe groot mijn canvas moet zijn en de randen bepalen.
```html
 <label>Color: </label>
  <input type="color" id="color" value="#000000" />

  <label style="margin-left:10px;">Size: </label>
  <input type="range" id="size" min="1" max="20" value="5" />

  <button onclick="clearCanvas()" class="deletebtn">Delete</button>
```
Ook heb ik twee labels toegevoegd, color en range, zodat je kunt kiezen welke kleur je wilt gebruiken en de grootte van de pen/brush.
En een button toegevoegd om je kunstwerk te verwijderen.

```javascript
  window.clearCanvas = function () {
      // Wist het kunstwerk van je canvas
      ctx.clearRect(0, 0, canvas.width, canvas.height);
    };
```


De functie getBoundingClientrect() begreep ik niet, deze functie zegt dus "hier zit het mijn canvas op de pagina, zodat je muis of podloot er correct op kan tekenen.
```javascript

    canvas.onmousedown = function (e) {
      // Start met tekenen als je muis indrukt
      //  e is event, waar de muis is
      drawing = true;

      let rect = canvas.getBoundingClientRect();
      // https://developer.mozilla.org/en-US/docs/Web/API/Element/getBoundingClientRect
      // Dit vraagt: Waar staat het canvas op de pagina

      // Zet startpunt van de lijn, gebruikt om de positie van de muis op het canvas zelf te berekenen:
      lastX = e.clientX - rect.left;
      lastY = e.clientY - rect.top;
    };
```
Als je dit niet gebruikt tekent je muis niet op het juiste punt op het canvas:
![Trekt een lijn vanuit linksboven](/src/img/voorbeeld.png)

Ook heb ik vandaag gewerkt aan de styling van de pagina's zodat de kunstwerken netjes naast elkaar staan met grid, en het er beter uit ziet.
![Grid](/src/img/grid.png)

## Vrij 17 april
The Web You Want – inspiratie

# Reflectie week 3:
Deze week ben ik begonnen met mijn nieuwe idee. Het werken met de API vond ik best lastig, vooral omdat de Rijksmuseum API niet werkte. Daarom heb ik een andere API gekozen. Ook vond ik het moeilijk om de code helemaal te begrijpen.
Maar met hulp van klasgenoten en Chatgpt is het gelukt.


# WEEK 4

## Wo 22 april
Mijn werk heb ik besproken met Jad, mijn idee moet nog aangepast worden, het mag iets creatiever. Hij heeft me ook geholpen met code, hij zei zelf dat het te veel werd om allemaal in één keer uit te leggen daarom ben van plan klasgenoten om hulp te vragen. Dit om mijn achterstand in te halen, en te zorgen dat ik mijn code begrijp.

## Vrij 24 april 
Tijdens het voorgang gesprek heb ik mijn nieuwe concept uitgelegd, een kunstapp met een pagina waar je schilderijen kunt bekijken voor inspiratie, en opslaan in je favorieten, een detailpagina voor elk schilderij en een pagina waarop je zelf digitaal je eigen kunstwerk kan maken. Dit concept was voldoende, alleen werd al snel duidelijk dat mijn door vooral is om mijn code te gaan begrijpen in plaats van alleen kopiëren. Daarna pas styling verbeteren.

# Wo 7 mei
Mijn site online gezet via render. Ik heb het zelf geprobeerd, maar het online zetten gaf veel errors waar ik zelf niet uit kwam, Jad heeft mij geholpen deze errors te fixen. 
![](/src/img/render.png)
Vandaag en morgen wil ik gebruiken om mijn code te gaan begrijpen, notities maken. En voor zover het lukt extra css toe te passen.

# Do 8 mei (deadline)
Vandaag heb ik extra styling toegepast, lettertypes, kleuren en de buttons aangepast:
![Styling toegepast](/src/img/Stylingtoegepast.png).
Mijn code doorgelopen en notities gemaakt erbij gezet in mijn code:
```javascript
 window.onload = function () {
    // Wacht tot de hele pagina klaar is

    const canvas = document.getElementById("canvas");

    // 2D tekenvlak (canvas om op te tekenen)
    const ctx = canvas.getContext("2d");

    // gekozen kleur
    const color = document.getElementById("color");

    // dikte van de lijn
    const size = document.getElementById("size");

    // teken aan/uit
    let drawing = false;

    // bewaart positie van de muis, nodig om een lijn te maken
    let lastX = 0;
    let lastY = 0;

    canvas.onmousedown = function (e) {
      // Start met tekenen als je muis indrukt
      //  e is event, waar de muis is
      drawing = true;

      let rect = canvas.getBoundingClientRect();
      // https://developer.mozilla.org/en-US/docs/Web/API/Element/getBoundingClientRect
      // Dit vraagt: Waar staat het canvas op de pagina

      // Zet startpunt van de lijn
      lastX = e.clientX - rect.left;
      lastY = e.clientY - rect.top;
    };
```


# Reflectie week 4:
Deze week heb ik feedback gekregen dat mijn project nog beter kon. Ik liep nog wat achter en heb daarom hulp gevraagd aan klasgenoten, jad en Chatgpt. Mijn doel werd vooral om mijn code beter te begrijpen voor mijn Eindbeoordeling, inplaats van alleen dingen laten werken. Dit was veel werk, maar ik ben wel blij dat alles uiteindelijk online staat en werkt. 
![Home pagina](/src/img/homepage.png)
![Favorites pagina](/src/img/favoritespagina.png)
![Create artwork pagina](/src/img/createartwork.png)


# Eindreflectie
Tijdens dit project heb ik een webapp gemaakt over kunst. Ik haal kunstwerken op via een API en gebruikers kunnen die gebruiken als inspiratie en opslaan als favoriet, ook kunnen ze via een canvas API zelf een kunstwerk maken. Als je klikt op 
het schilderij kom je op de pagina van het kunst instituut zelf waar je meer informatie kan lezen over het schilderij.

In het begin had ik een ander idee (een filmapp), maar door feedback ben ik overgestapt naar kunst omdat dat beter bij mij past.

Ik vond het best lastig om de code echt te begrijpen, vooral het werken met Astro en API's. Soms kreeg ik het wel werkend, maar snapte ik niet precies hoe het werkte. Daarom heb ik veel hulp gevraagd, aan Jad, andere studenten, met Chatgpt en zelf dingen opgezocht. En te snappen wat code doet in plaats van het alleen te kopiëren.

Uiteindelijk ging dat wel steeds beter. Door het vaak terug te kijken en notities te maken begon ik het iets meer te begrijpen. Code zelf schrijven blijft lastig maar het toepassen lukt nu iets beter.

Als ik terugkijk heb ik vooral geleerd dat ik het pas echt ga begrijpen als ik hulp vraag van anderen en dat de achterstand  aan het begin van deze weken, het extra moeilijk heeft gemaakt, maar dat ik het uiteindelijk wel zoveel mogelijk heb kunnen inhalen.



# Herkansing
Omdat ik nog geen eigen detailpagina per schilderij heb ik deze aangemaakt, en op dezelfde manier gestyled als de rest van de app.
Op de pagina zie je de titel, afbeelding van het kunstwerk, kunstenaar en jaartal, andere details, hoe is dit kunstwerk gemaakt (medium), afmetingen en herkomst. Onderaan zie je info over de kunstenaar. En een link terug naar de overzichtspagina.
Ik wilde graag een tekst laten zien over het schilderij. Ik heb deze geprobeerd (chatgpt):
```javascript
{artwork.discription}
{artwork.thumbnail?.alt_text}
{artwork.provenance_text}
```
Maar deze waren niet beschikbaar
Dus heb ik gekozen dat je informatie kan lezen de artist zelf (als deze beschikbaar is). 
```javascript
{artwork.artist_display}
```

![Detailpagina:](/src/img/detailpagina.png)

Code [art].astro:
```javascript
<Layout>
  <!-- titel -->
  <h1>{artwork.title}</h1>

  <a href="/">← Back to all artworks</a>

    <!-- naam artist -->
  <h2>{artwork.artist_title}</h2>

  <!--  informatie over de artist --> 
  {artwork.artist_display && (
    <section>
      <p>{artwork.artist_display}</p>
    </section>
  )}
  
<!-- afbeelding kunstwerk -->
  {artwork.image_id && (
    <img
      src={`https://www.artic.edu/iiif/2/${artwork.image_id}/full/800,/0/default.jpg`}
      alt={`Artwork titled ${artwork.title} by ${artwork.artist_title}`}
    />
  )}
  
    <!-- datum -->
  <h3>Date ({artwork.date_display})</h2>


<!-- info over het kunstwerk -->
  <ul>
    <li><strong>Medium:</strong> {artwork.medium_display}</li>
    <li><strong>Dimensions:</strong> {artwork.dimensions}</li>
    <li><strong>Origin:</strong> {artwork.place_of_origin}</li>
  </ul>

</Layout>
```



Bronnen:
- https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API
- https://api.artic.edu/docs/#quick-start
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- https://docs.astro.build/en/basics/layouts/
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/strokeStyle
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineWidth
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D
- https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event
- https://developer.mozilla.org/en-US/docs/Web/API/Element/mousemove_event
- ChatGPT
- Jad
<!--   // JSON.stringify(object) -> object naar string
  // JSON.parse(string) -> string naar object
 -->