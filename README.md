# Photo Tools

Calcolatore fotografico responsive per profondità di campo e distanza di inquadratura, installabile come PWA e utilizzabile offline.

## Funzioni
- Focale, diaframma e circolo di confusione modificabili
- Dimensione sensore, orientamento, altezza soggetto e margine
- Distanza soggetto modificabile, con modalità **mantieni altezza** o **mantieni margine**
- Limiti vicino e lontano con etichette **INIZIO** e **FINE** sulla barra DoF
- Iperfocale e confronto f/1.8, f/2.8, f/4, f/5.6, f/8, f/11

## Avvio Docker

```bash
cd /opt/stacks
git clone git@github.com:farinad/photo-tools.git
cd photo-tools
cp .env.example .env
vi .env
docker compose up -d
```

Predefinito: http://127.0.0.1:8097 (loopback del container Docker).
Per un reverse proxy esterno, impostare PHOTO_TOOLS_BIND_IP all'IP dell'host/LXC Docker raggiungibile da Caddy.

## PWA
Pubblicare via HTTPS per installare sulla schermata Home di iPhone e abilitare il service worker. Dopo il primo caricamento i calcoli sono disponibili offline.

## Note
I calcoli seguono un modello a lente sottile e usano millimetri internamente. La DoF è una stima convenzionale, non una garanzia di nitidezza al pixel. .env è escluso dal repository.
