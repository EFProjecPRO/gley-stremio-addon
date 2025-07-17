# GleyAddon - Professional Stremio Addon

🎬 Професионален Stremio addon за филмови и серии со magnet linkови

## Карактеристики

- ✅ Интеграција со TMDB API за метаподатоци
- ✅ Поддршка за magnet linkови (torrent)
- ✅ Професионален дизајн со custom лого и позадина
- ✅ Admin панел за лесно додавање содржина
- ✅ Поддршка за филмови и серии
- ✅ Претрага и категории
- ✅ Повеќе квалитети за секој содржина

## Инсталација

1. Инсталирај dependencies:
```bash
npm install
```

2. Стартај го серверот:
```bash
npm start
```

3. Серверот ќе работи на: `http://localhost:3000`

## Додавање во Stremio

1. Отвори Stremio
2. Оди на Add-ons
3. Внеси: `http://localhost:3000/manifest.json`
4. Кликни "Install"

## Користење на Admin панелот

1. Отвори `http://localhost:3000/admin.html`
2. Избери тип на содржина (Movie/Series)
3. Внеси TMDB ID (најди го на themoviedb.org)
4. Додај magnet linkови за различни квалитети
5. Кликни "Add Content"

## Структура на JSON фајлот

\`movieandseries.json\` содржи:

```json
{
  "movies": [
    {
      "id": "tmdb:550",
      "tmdb_id": "550",
      "streams": [
        {
          "quality": "1080p",
          "size": "2.1 GB",
          "language": "English",
          "magnet": "magnet:?xt=urn:btih:..."
        }
      ]
    }
  ],
  "series": [...]
}
```

## API Endpoints

- `GET /manifest.json` - Addon manifest
- `GET /catalog/:type/:id.json` - Каталог содржина
- `GET /meta/:type/:id.json` - Метаподатоци
- `GET /stream/:type/:id.json` - Stream linkови
- `POST /admin/add/:type` - Додавање нова содржина

## TMDB API

Користи TMDB API за:
- Метаподатоци за филмови/серии
- Постери и позадини
- Рејтинзи и описи
- Претрага

## Безбедност

- Сите magnet linkови се чуваат локално
- Нема директно споделување на торент фајлови
- Користи само јавни TMDB API

## Поддршка

За прашања и поддршка, контактирај го развивачот.