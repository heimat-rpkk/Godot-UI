## PanelContainer

1.  Osaa laskea kokonsa automaattisesti sen sisällä olevien solmujen koon ja marginaalien mukaan.

2.  Keskittäminen ruudun keskelle (Anchoring)

    Valitse CenterMenuPanel (PanelContainer) Scene-puusta.

    Katso 2D-ikkunan yläpalkkiin ja valitse Layout / Anchor Preset (vihreät neliökuvakkeet).

    Valitse listasta Center tai VCenter Wide.

        Nyt paneeli ja sen sisältö pysyvät aina täydellisesti ruudun keskellä.

3.  Tummaksi ja läpinäkyväksi määrittely (StyleBoxFlat)

    Valitse CenterMenuPanel (PanelContainer).

    Katso oikealle Inspector-paneeliin ja etsi kohta Theme Overrides -> Styles.

    Kohdan Panel vieressä klikkaa 'empty' ja valitse New StyleBoxFlat.

    Klikkaa luomaasi StyleBoxFlat-ruutua avataksesi sen asetukset:

        Bg Color (Taustaväri):

            Klikkaa väriympyrää.

            Valitse musta tai hyvin tummanruskea väri.

            Säädä alhaalla olevaa A (Alpha / Läpinäkyvyys) -liukukytkintä pienemmälle (esim. arvot 150–200 asteikolla 0–255, eli noin 60–80 % peittävyys).

        Corner Radius (Kulmat):

            Aseta kaikki 4 kulmaa arvoon 0 px, jos haluat terävät pikselikulmat.

        Border / Reunat (Valinnainen):

            Voit halutessasi lisätä pienen reunan kohdasta Border Width (esim. 2 px) ja valita reunan väriksi hieman vaaleamman sävyn.

## MarginContainer

Sisämarginaalien säätäminen (valinnainen). Myös negatiiviset marginaalit ovat mahdollisia.

    Mene Inspectorissa kohtaan Theme Overrides -> Constants.

    Laita rasti ruutuun ja aseta arvot seuraaville marginaaleille:

        Margin Top / Bottom: esim. 16 px tai 20 px

        Margin Left / Right: esim. 20 px tai 30 px

## VBoxContainer

Järjestää sen sisällä olevat solmut automaattisesti pystysuoraan allekkain.

Nappien välien säätäminen

    Valitse ButtonContainer (VBoxContainer).

    Mene Inspectorissa kohtaan Theme Overrides -> Constants -> Separation.

    Aseta sopiva väli nappien väliin (esim. 8 px tai 12 px).
