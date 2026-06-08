# Network Map Card

Card Lovelace personalizzata per visualizzare i dispositivi di rete monitorati dall'integrazione **Network Map** per Home Assistant.

## Requisiti

- Home Assistant 2023.1.0 o superiore
- Integrazione [Network Map](https://github.com/tuo-username/home-assistant-network-map) installata

## Installazione

### HACS (raccomandato)

1. Vai su **HACS → Frontend**
2. Clicca su **⋮ → Repository personalizzati**
3. Aggiungi l'URL di questo repository e seleziona categoria **Lovelace**
4. Cerca **Network Map Card** e installa
5. Aggiungi la risorsa alla dashboard se non viene fatto automaticamente

### Manuale

1. Copia `network-map-card.js` in `<config>/www/network-map-card.js`
2. Vai su **Impostazioni → Dashboard → ⋮ → Risorse → Aggiungi risorsa**
3. URL: `/local/network-map-card.js`
4. Tipo: **JavaScript Module**

## Configurazione

Aggiungi una card manuale alla dashboard:

```yaml
type: custom:network-map-card
title: La Mia Rete
height: 600
```

### Opzioni

| Nome | Tipo | Default | Descrizione |
|------|------|---------|-------------|
| `type` | string | obbligatorio | `custom:network-map-card` |
| `title` | string | `Network Map` | Titolo della card |
| `height` | number | `500` | Altezza in pixel |

## Funzionalità

- Visualizzazione nodi con emoji per tipo di dispositivo
- Colore verde/rosso per stato online/offline
- **Drag & drop** per spostare i dispositivi sulla mappa
- Persistenza automatica delle posizioni tramite servizio `network_map.update_position`
- Sfondo a griglia per aiutare il posizionamento

## Licenza

MIT
