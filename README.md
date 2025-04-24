# Mistral Impianti SRL - Sito Web Aziendale

Sito istituzionale realizzato con [Astro](https://astro.build/) e [TailwindCSS](https://tailwindcss.com/) per Mistral Impianti S.R.L., azienda specializzata in impianti tecnologici, antincendio, manutenzione e soluzioni innovative dal 1988.

## Caratteristiche principali
- **Framework:** Astro 5 + TailwindCSS
- **SEO avanzata:** meta tag Open Graph, Twitter Card, sitemap, robots.txt
- **Performance:** immagini ottimizzate, lazy loading, minificazione automatica, preload font
- **Accessibilità:** landmark, heading semantici, aria-label, alt descrittivi
- **Responsive:** design mobile-first
- **Certificazioni e partners**: sezione dedicata
- **Brochure e documenti**: download PDF

## Struttura del progetto

```
/
├── public/           # Asset statici (immagini, PDF, favicon)
├── src/
│   ├── assets/       # Asset importabili (SVG, background)
│   ├── components/   # Componenti riutilizzabili (Navbar, Footer)
│   ├── layouts/      # Layout principali (MainLayout.astro)
│   ├── pages/        # Pagine del sito (index, servizi, lavori, partners, contatti, 404)
│   └── styles/       # CSS globale (Tailwind)
├── astro.config.mjs  # Configurazione Astro e plugin
├── tailwind.config.cjs
├── package.json
└── tsconfig.json
```

## Comandi principali

| Comando              | Azione                                      |
|----------------------|---------------------------------------------|
| `npm install`        | Installa le dipendenze                      |
| `npm run dev`        | Avvia il server di sviluppo (localhost:4321)|
| `npm run build`      | Compila il sito statico in `./dist/`        |
| `npm run preview`    | Anteprima della build                       |
| `npm run astro ...`  | Comandi CLI Astro (es: add, check)          |

## Troubleshooting

- **Errore build immagini:** assicurati che tutte le immagini usate siano presenti in `/public` o importate da `/src/assets`.
- **Problemi con Tailwind:** se le classi non vengono applicate, riavvia il server di sviluppo e controlla la configurazione in `tailwind.config.cjs`.
- **404 su PDF o immagini:** verifica il percorso e la presenza dei file in `/public`.
- **Problemi SEO:** verifica che ogni pagina abbia un titolo e una descrizione univoci tramite la prop `title` e `description` del layout.
- **Problemi di deploy su Vercel/Netlify:** assicurati che la variabile `site` in `astro.config.mjs` sia corretta.

## Best practice e note tecniche

- Modifica i meta tag SEO in `src/layouts/MainLayout.astro` per personalizzare titolo, descrizione, immagini social.
- Per aggiungere nuove pagine, crea un file `.astro` in `src/pages/` e usa il layout principale.
- Le immagini di progetti e partner sono caricate da `/public` per semplicità, ma per ottimizzazione avanzata usa il componente `<Image />` di `astro:assets`.
- Il sito è ottimizzato per Lighthouse (performance, SEO, accessibilità): verifica con `npm run build` e strumenti Chrome DevTools.
- Per aggiornare la sitemap o robots.txt, modifica la configurazione dei plugin in `astro.config.mjs`.

## Riferimenti utili
- [Documentazione Astro](https://docs.astro.build/)
- [Deploy su Vercel](https://docs.astro.build/en/guides/deploy/vercel/)
- [TailwindCSS](https://tailwindcss.com/docs/installation)
- [Astro SEO Guide](https://docs.astro.build/en/guides/seo/)

---

© {2025} Mistral Impianti S.R.L. - Tutti i diritti riservati
