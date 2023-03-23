# Layout Thrashing

Lession page jank behandel ik samen met de groep, meeste mensen komen hier niet uit. Maar het is wel heel leerzaam.

Handig tip is om de fps meter aan te zetten. In devtools `Ctrl+shift+p`, zoek fps, selecteer show fps meter

Oplossing:

De insert van 50 items verhogen naar 200 of 100
Zie dat dom inserts in een loop niet heel handig is, leg het gebruik van `createDocumentFragment` uit

Leg uit dat dom manupilatie niet handig is als je dom elementen over het scherm gaat bewegen. We hebben net geleerd dat html/dom voor structuur en data zorgt en dat css voor opmaak en styling is. Dus dat je animaties het beste kunt oplossen met css animaties

Zet de move functie uit. `// rAF = window.requestAnimationFrame(move);`

<https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations>

Voor de eerste animatie gebruik top

```css
.jank-logo {
  top: 0;
  animation: move infinite alternate ease-in-out;
}
@keyframes move {
  0% {
    top: 0vh
  }
  100% {
    top: 100vh
  }
}
```

Laat zien dat performance beter is maar nog niet goed genoeg. Als er meer items bij komen wordt de animatie traag en ze gaan allemaal te gelijk
Om de animaties verschillende timings te geven kan je het volgende gebruiken:

```js
// newLogo.style.top = top + "px";
newLogo.style.animationDelay = `${Math.random() * (i % 5) + 1}s`;
newLogo.style.animationDuration = `${Math.random() * (i % 20) + 1}s`;
```

Nu is het timings verschil opgelost, maar de performance kan nog beter als er van de gpu gebruikt wordt gemaakt
<https://www.smashingmagazine.com/2016/12/gpu-animation-doing-it-right/>

```css
@keyframes move {
  0% {
    transform: translateY(0vh);
  }
  100% {
    transform: translateY(95vh);
  }
}
```

Voeg 5000 items toe en zie 60 fps baby!
