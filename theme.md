## Theme-resurssin luominen

Theme-resurssin luominen Godot 4:ssä helpottaa työskentelyä huomattavasti, sillä sen avulla voit määrittää esim. kaikkien nappien tyylin, fontin ja värit yhdessä paikassa ilman, että niitä tarvitsee säätää jokaiselle napille erikseen.

### Uusi Theme-resurssi

Valitse päänäkymässä valikkosi juurisolmu (esim. PanelContainer- tai VBoxContainer-solmu).

Katso oikealle Inspector-paneeliin ja etsi kohta Control -> Theme.

Klikkaa kohdan Theme vieressä olevaa <empty>-kenttää ja valitse valikosta New Theme.

Klikkaa juuri luomaasi Theme-resurssia avataksesi sen.

Tallenna teema tiedostoksi: klikkaa teeman vieressä olevaa pientä nuolta/tallennuskuvaketta ja valitse Save, anna nimeksi esimerkiksi main_menu_theme.theme ja tallenna se res://-kansioon.

Kun teema on valittuna, Godot avaa ruudun alalaitaan Theme Bottom Panel -työkalurivin.

### Button-tyylien määrittäminen Theme-paneelissa

Ruudun alalaidan Theme-paneelissa klikkaa Add Type -painiketta (tai plus-kuvaketta +).

Kirjoita hakukenttään Button ja lisää se tyyppilistaan.

Nyt voit säätää Button-komponentin kaikkia oletusominaisuuksia:

A. Fontin ja tekstikoon asettaminen kaikille napeille:

    Valitse alapaneelista tai Inspectorista kohta Fonts -> font ja vedä lataamasi .ttf-pikselifontti siihen.

    Fonttejä löytyy esim. 'https://itch.io/game-assets/free/tag-fonts'

    Valitse kohta Font Sizes -> font_size ja aseta haluamasi koko (esim. 16 px tai 24 px).

B. Napin ulkoasun (StyleBox) luominen eri tiloille:

Siirry Styles-osioon. Täällä määritetään napin eri tilat:

    normal: Napin perustila.

    hover: Tila, kun hiiri on napin päällä.

    pressed: Tila, kun nappia painetaan.

    focus: Valitun napin reunat (hyödyllinen näppäimistö-/ohjainnavigoinnissa).

Luodaan tyyli perustilalle (normal):

    Klikkaa kohdan normal vierestä ja valitse New StyleBoxFlat (tai New StyleBoxTexture, jos käytät valmiita kuva-assetteja).

    Klikkaa luotua StyleBoxFlat-laatikkoa avataksesi sen säädöt Inspectorissa:

        Bg Color: Aseta ruskea taustaväri.

        Border Width: Aseta arvot esim. Top: 2, Bottom: 2, Left: 2, Right: 2.

        Border Color: Aseta tummempi/vaaleampi reuna.

        Corner Radius: Varmista, että kaikki 4 kulmaa ovat 0 px, jotta saat terävät pikselikulmat.

        Content Margins: Säädä sisämarginaaleja (esim. Top/Bottom: 6, Left/Right: 12), jotta teksti ei osu reunoihin.

Luodaan tyylit muille tiloille (hover ja pressed):

    Klikkaa luomaasi normal-tilan StyleBoxFlattia hiiren oikealla painikkeella ja valitse Copy.

    Klikkaa hiiren oikealla kohdan hover vierestä ja valitse Paste.

    Klikkaa 'tee uniikiksi', jotta voit muuttaa vain tämän StyleBoxin ominaisuuksia.

    Klikkaa liitettyä StyleBoxia ja muuta sen värejä:

        Vaihda Bg Color ja Border Color vaaleansiniseksi (kuten luomassamme kuvassa valitussa napissa).

    Toista Copy-Paste kohdalle pressed ja tee sen taustaväristä hieman tummempi.

3. Teeman käyttö kaikissa valikon napeissa

Koska asetit Theme-resurssin yläsolmulle, kaikki sen sisällä olevat napit perivät tämän teeman automaattisesti.

    Sinun ei tarvitse muokata jokaista Button-solmua erikseen.

    Jos lisää uuden napin (Button), se saa välittömästi täysin saman pikselitaide-ilmeen ja fontin!

    Jos haluat myöhemmin muuttaa esimerkiksi napin fonttia tai reunuksen väriä, muutat sitä vain kerran tässä .theme-tiedostossa, ja kaikkien nappien ulkoasu päivittyy kerralla.
