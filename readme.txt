URL aplikacije: https://web2-lab6-fm0z.onrender.com/

1. interpolation/one-way binding - Da, frontend/src/components/TimedGame.vue, linija 3 (varijabla score kao primjer, samo u toj datoteci ima još primjera)

2. two-way binding - Da, frontend/src/components/TimedGame.vue, linija 27 (v-model i varijabla playerName, sve slično kao u TimedGame ima i u UntimedGame)

3. methods - Da, frontend/src/components/TimedGame.vue, linija 79 (analogno i u UntimedGame, metode su startGame, guess, endGame, pushScore)

4. computed properties - Da, frontend/src/components/TimedGame.vue, linija 62 (opet analogno i u UntimedGame, imamo highScore, highScorePlayer i formattedTimeLeft)

5. barem jedan scoped style -  Da, frontend/src/components/TimedGame.vue, linija 141 (opet analogno i u UntimedGame) te u frontend/src/components/AppHeader.vue, linija 27

6. koristiti barem jedan lifecycle hook -  Da, frontend/src/components/TimedGame.vue. linija 133 (opet analogno i u UntimedGame) te frontend/src/App.vue, linija 29 i 33

7. routing (više stranica) - Da, router je definiran u frontend/src/main.js linije 10-20, koristi se u frontend/src/App.vue, linija 7
aplikacija mora biti bookmarkable, tako da rade linkovi (ne samo na root, već i moj-web.com/stranica1, moj-web.com/stranica2) - Da, radi na /timed i /untimed
dinamičko usmjeravanje s 404 stranicom ("catch all") - Da, u frontend/src/components postoji stranica NotFoundPage.vue koja se koristi u frontend/src/main.js, linija 14.

8. (barem) dvije komponente - Da, u frontend/src/components postoi 5 različitih komponenti
komponenta bez stanja, koristiti properties - Da, primjer je frontend/src/components/AppHeader.vue, koristi props na liniji 14
komponenta sa stanjem - Da, npr. frontend/src/components/TimedGame.vue, linija 48, stanje se definira podatcima 
barem jedna komponenta mora emitirati barem jedan event - Da, frontend/src/components/AppHeader.vue u linijama 5 i 6 emitira event promjene modea

10. store (Pinia) - Da, frontend/src/stores/store.js kreira pinia store i on se onda koristi u više datoteka i komponenti, npr frontend/src/components/TimedGame.vue, linije 134 i 135 prikazuju korištenje storea. Ima još primjera u UntimedGame i AppHeader

11. asinkroni dohvat podataka s backenda - Da, u frontend/src/stores/store.js postoji asinkroni dohvat s backenda koji ima u JSON fileu pohranjene sve podatke

Aplikacija je postavljena na danom linku u production modeu.
Za lokalno pokretanje, pokrenuti "npm i" i u frontend i backend folderu te se pozicionirati u backend folder i pokrenuti "npm run dev", port frontenda je 8080, a port backenda je 3000
Alternativno, pozicionirati se u backend folder i pokrenuti "npm run serve". Ta naredba odrađuje i instalaciju i pokretanje.