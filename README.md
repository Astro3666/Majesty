# Majisty

Website for **Majisty**, an Omani fragrance house. *Three Cultures. One Journey.*

The page opens with a 3D model of the Journey oud vessel (Al Sadu woven cover, brass cap, O-ring seal, composite shell, sealed vial of oud chips) that comes apart layer by layer as you scroll. After that come the product ranges:

- **Bukhoor** in 50 g, 100 g, 200 g and 400 g
- **Frankincense**, high-quality gum in male and female grades
- **Oud fragrance oil**, Omani blend, in 3 ml, 6 ml and 12 ml
- **The Journey vessel**

Visitors add products to an order list, then send it on WhatsApp or copy it as a message.

## Set your prices and contact details

Open `index.html` and find the block marked `EDIT HERE` near the bottom. It looks like this:

```js
const MAJISTY = {
  prices: {
    bukhoor: { 50: null, 100: null, 200: null, 400: null },
    frankincense: { male: null, female: null },
    oud: { 3: null, 6: null, 12: null },
    vessel: null
  },
  whatsapp: '',   // digits only with country code, e.g. '96891234567'
  instagram: '',  // handle without @
  email: ''
};
```

- Prices are in Omani rials. For example, `100: 2.5` shows **OMR 2.500**. Any price left as `null` shows "Price to be set".
- Once `whatsapp` is filled in, a **Send on WhatsApp** button appears. It opens a chat with the full order and the total.

## Publish with GitHub Pages

1. Go to **Settings → Pages** in this repository.
2. Under *Build and deployment*, pick **Deploy from a branch**, then choose `main` and `/ (root)`.
3. After a minute the site goes live at `https://<your-username>.github.io/Majisty/`.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole site: layout, styles, the 3D scene (Three.js 0.160 loaded from jsDelivr) and the order list |
| `assets/frankincense.jpg` | Frankincense gum photo used in the Frankincense section |
| `assets/journey-vessel.jpg` | Product photo. It's used in the Flagship section and shown in place of the 3D scene if a browser can't run WebGL |
| `.nojekyll` | Tells GitHub Pages to serve the files exactly as they are |

To preview it on your own computer, open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
