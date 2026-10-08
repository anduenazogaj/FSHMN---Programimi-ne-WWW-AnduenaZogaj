# Java III — Klinika e CSS: Shpëto afishen

## Klubi i debatit

Kjo detyrë paraqet një afishe për Klubin e Debatit duke përdorur HTML dhe CSS.

## Çfarë është përdorur

- CSS i jashtëm
- Selektorë CSS
- Klasa të ripërdorshme
- Variabla CSS për ngjyrat dhe hapësirat
- Box model
- `box-sizing: border-box`
- `hover`
- `focus-visible`
- Media query
- Responsive design

## Tri etiketat

Në afishe janë përdorur tri etiketa:

- Falas
- Vende të kufizuara: 20
- Edhe online

Etiketat nuk dallohen vetëm përmes ngjyrës. Për shembull, etiketa "Vende të kufizuara" përdor edhe border të ndërprerë.

## Diagnostikimi i gabimeve

Në skedarin `gabime.css` janë diagnostikuar dy probleme.

### 1. Konflikti i specifikës

Selektorët `#poster` dhe `.poster` vendosin të dyja pronën `color`.

`#poster` është ID selector, ndërsa `.poster` është class selector.

ID selector ka specifikë më të madhe se class selector, prandaj rregulli i `#poster` fiton në kaskadë.

Problemi ishte se `#poster` kishte:

```css
color: white;
background: white;