# Ball Chain Reaction – 1.4.7

Láncreakciós golyós fejtörő: a játékos eszközöket tesz le, és a lánc végén a golyó célba ér, megszólal a csengő vagy felkapcsol a lámpa.
Készítő: Joó Ferenc

## Tartalom

- 10 világ × 20 pálya = **200 pálya**, rendre nehezedő láncokkal (1–2 rekesztől 6 rekeszes, 20+ lépéses gépezetekig)
- **113 gyűjthető eszköz** (a játékterv 98 hétköznapi tárgya + alap elemek), 10 golyótípus saját fizikával
- Rendszerek: lökés, súly, kötél/csiga, levegő, áram, fény (tükör, napelem), hang (tapskapcsoló), víz, hő, forgás (fogaskerék, csörlő)
- Szabad építés: csak a már megszerzett eszközökkel
- Nyelvek: magyar, német, angol

## Újdonságok az 1.4.7-ben

- A kisautó kerekei a talajon állnak (nem lóg a levegőben).
- **Cső:** a hajlított cső most ugyanolyan stílusú, mint a cső-képek (sötét kontúr, fényes zöld, csillanás), a vastagsága illik a bejárathoz és a kijárathoz, a kijárat a cső irányába fordul.
- **Csőposta:** átlátszó üvegcső-stílus kék gyűrűkkel (nem keveredik a zöld csővel).

## Újdonságok az 1.4.6-ban

- **+79 új kép** (összesen 123): a 2. és 3. adag – pl. ventilátorok, lámpák, kapcsolók, víz- és hőeszközök, fogaskerekek, csörlő, metronóm, új halvány gyerekszoba-háttér (`bg_w1`), menü-háttér, barna fa indító.
- Állapotképek működnek: `toggle_on`, `bulb_on`, `clap_on`, `solar_on`, `flashlight_on`, `pedalbin_open`; mozgó részek: `gear_big`/`gear_small`, `belt_wheel`, `winch_drum`, `float_b`, `scale_base`, `metronome_base`, `hourglass_glass` (pergő homok).
- Képjavítások: átlátszó háttér lett a `peg`, `pulley` (rárajzolt sakktábla), `clap_on`, `radio`, `toggle`, `tray` képeken; a `gear_big` a `gear_small`-ból készült ezüst színben; `winch_durm` → `winch_drum` átnevezve.
- Több kép arányhelyesen illeszkedik (nem torzul).

## Újdonságok az 1.4.5-ben

- **Kosár:** a kosár a golyók előtt rajzolódik, így a beleesett golyó eltűnik benne (nem látszik át rajta).
- Új, barna fa hatású prompt az indítóhoz (`starter.png`) a képtáblázatban.

## Újdonságok az 1.2.4-ben

- **Jobban látszanak az eszközök:** a játék a háttérképet halványítja, kicsit fakóbbá teszi és enyhén elmossa, így a pályaelemek elválnak tőle. (Erősség: `KG.BGDIM`, alapból 0,45.)
- Új, nyugodtabb háttér-promptok a képtáblázatban (vonalak, polcok, ablakkeretek nélkül).

## Újdonságok az 1.2.3-ban

- **Saját képek:** benne van az első 46 kép (10 háttér + eszközök). A hátterek JPG-ben vannak (kisebb, gyorsabban tölt), a `.png` háttér is működik.
- A képek **arányosan** kerülnek a helyükre (nem torzulnak); a vékony lécek, polcok, falak a játék méretére igazodnak.
- **Állapot- és részképek:** a játék kezeli a `_on` / `_open` állapotképeket (pl. `toggle_on`, `bulb_on`, `pedalbin_open`) és a több részből álló, mozgó tárgyakat (pl. `scale_base`, `gear_big` + `gear_small`, `winch_drum`, `belt_wheel`, `float_b`, `card`, `hourglass_glass`). A víz, a homok, a mutatók, a számok és a jelzőlámpák a kép fölött animálódnak.
- **Javítva:** a kék rugós ruhacsipesz már nem löki el a golyót indítás előtt (a golyó a csipesz testébe lógott). Az érintett pályák újra lettek generálva és ellenőrizve.
- Képjavítások: `candle_on` háttere átlátszó lett, `bg_w7` 16:9-re vágva, a hibás `pipe_in` kimaradt (újra kell).

## Újdonságok az 1.2.1-ben

- **Android:** teljes képernyő (rejtett óra, akku- és navigációs sáv), a játék **mindig fekvő módban** marad, akkor is, ha megfordítják a készüléket.
- **Nagyítás:** két ujjal széthúzva nagyítható és mozgatható a pálya, egérrel görgővel. A nagyító gombbal vagy a **Start** megnyomásakor visszaáll az eredeti nézet.
- **Finomabb mozgatás:** érintéssel a lerakott tárgy lassabban követi az ujjat, a kijelölt tárgy a ◀ ▲ ▼ ▶ gombokkal 5 egységenként tolható.
- **Gyorsabb futás régebbi tableten:** gyorsabb ütközésvizsgálat, előre megrajzolt háttér, legfeljebb 2× felbontás, és ha a gép lassú, a játék automatikusan árnyék nélküli, egyszerűbb grafikára vált.
- **Webapp (PWA)** iPhone-ra és bármilyen böngészőre.

## Android (Android Studio)

Projekt: `C:\AndroidAppok\BallChainReaction2`, csomagnév: `com.jooferenc.ballchainreaction`

| Fájl | Helye |
|---|---|
| `index.html` | `app/src/main/assets/` |
| saját képek (`*.png`, háttér `.jpg` is) | `app/src/main/assets/img/` |
| `MainActivity.java` | `app/src/main/java/com/jooferenc/ballchainreaction/` |
| `AndroidManifest.xml` | `app/src/main/` |
| `build.gradle.kts` (Module :app) | `app/` |

Fordítás: Build → Clean Project, majd Run ▶. A verzió a Beállítások alján látszik: **Ball Chain Reaction 1.4.7**.

Ha „Incompatible Gradle JVM version” hiba jön: a `gradle/wrapper/gradle-wrapper.properties` fájlban a Gradle-verzió legyen **9.6.0** (vagy újabb).

## Webapp (iPhone / Safari)

A `web` mappa tartalmát egy HTTPS-es tárhelyre kell feltenni (pl. Netlify Drop, GitHub Pages). A mappa tartalma:

- `index.html` – maga a játék
- `manifest.webmanifest`, `sw.js` – telepíthető alkalmazás, offline is működik
- `icons/` – az alkalmazásikon

**iPhone-on:** Safari → nyisd meg a címet → Megosztás gomb → **Főképernyőhöz adás**. Így ikonról, teljes képernyőn indul.
Az iPhone nem engedi rögzíteni a fekvő módot. Ha a telefon álló helyzetben van (vagy be van kapcsolva a tájolászár), a játék magától 90°-kal elforgatva jelenik meg, így oldalra fordított telefonnal ugyanúgy játszható.

Saját képek a webappban: tedd a PNG-ket (háttérnél JPG is jó) az `img` mappába, és a nevüket (kiterjesztés nélkül) írd be az `index.html` elején a `KG_IMGLIST` listába, pl. `['ball_red', 'bg_w1']`.

## Képek

A ChatGPT-promptokat a `BallChainReaction_kepek_promptok.xlsx` tartalmazza. Mindegyik sorban szerepel a pontos fájlnév, a méret és az arány. A hiányzó képek helyett a játék a saját rajzolt grafikáját használja.
