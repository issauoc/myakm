# myakm — Shopify theme files for the AKM store

Any session that works on this repo reads this file first. Its facts are fixed
until the user changes them. If something here contradicts what the user says
in the conversation, follow the user and update this file.

## The store and its themes

| What | Value |
|---|---|
| Store | `jxawnn-99` |
| **Main theme** (the one the user works on) | **`189672751332`** — [open the editor](https://admin.shopify.com/store/jxawnn-99/themes/189672751332/editor) |
| Wholesale theme (الجملة) | `189721346276` |

### Rules

1. **Do not create a new theme.** The wholesale theme already exists (`189721346276`).
   Wholesale files are uploaded to it only.
2. **Do not change the main theme `189672751332`** (upload, edit, publish, or delete
   files) without asking the user first and getting a clear yes.
3. Before you write anything to a theme, name the theme ID you are about to change.
   After the write, read the file back and confirm the upload worked.
4. Never publish a theme (make it live) unless the user asks for it.

## What is in this repo

These are files from the used-car section of the store (سيارات مستعملة). They are
Arabic and RTL (`dir="rtl" lang="ar"`):

| File | Role |
|---|---|
| `sections/used-cars-listing.liquid` | Listing page: hero, filter bar, car card grid, compare (schema name: `AKM Used Cars`) |
| `snippets/vehicle-card.liquid` | One car card, rendered from the listing |
| `sections/used-car-product-details.liquid` | Car details page (schema name: `Used Car Details`) |
| `sections/main-product.liquid` | Default product page (schema name: `صفحة تفاصيل السيارة`) |
| `templates/product.used-car.json` | Alternate product template → `used-car-product-details` |
| `templates/product.json` | Default product template → `main-product` |
| `snippets/vehicle-seo-meta.liquid` | SEO meta tags, rendered in `<head>` |
| `snippets/vehicle-structured-data.liquid` | Schema.org JSON-LD for the car |
| `layout/theme.liquid` | Reference only: shows the `<head>` block to merge into the live theme's layout. Do not overwrite the live layout with it. |

The car data comes from product metafields in the `car_details` namespace
(`brand`, `model`, `year`, `mileage`, `transmission`, `fuel_type`, `condition`,
`location`, `color`, `drive_type`, `dealer_name`, `phone`, `whatsapp`, `verified`).
Some fields fall back to Shopify standard metafields in the `shopify` namespace.

The wholesale (الجملة) files are not in this repo yet. When they are added,
list them here along with the theme they go to.

## Working on the repo

- Work branch: `claude/myakm-upload-files-ws47eu`.
- Keep the file names here the same as in the live theme. A rename breaks the upload.
- The user writes in Egyptian Arabic. Reply in the same language.
