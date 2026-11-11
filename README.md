<h1 align="center">reelqueue</h1>
<p align="center">A watch-later list for films and series: what to watch, where it streams, and its genre, in one queue.</p>

<p align="center">
  <img alt="React" src="https://img.shields.io/badge/ui-React%2018-61dafb">
  <img alt="Express" src="https://img.shields.io/badge/api-Express-444">
  <img alt="MongoDB" src="https://img.shields.io/badge/db-MongoDB-47a248">
</p>

<p align="center"><img src="sc.png" alt="reelqueue: the list with its platform and genre filters" width="720"></p>

## What it does

- Add a title with its platform (Netflix, Amazon Prime, Disney+, Hotstar, Jio Cinema and others), its genre and a link to it.
- Filter the queue by platform and by genre.
- Edit or remove an entry once it is watched.

Built in January 2024 as the take-home assignment in Stagewise's hiring process.

## Stack

| Part | Tools |
|---|---|
| Interface | React 18, Bootstrap 5, Axios |
| API | Node.js, Express, Mongoose |
| Database | MongoDB (local, `watch_later_list`) |

## Run it

Start MongoDB on `localhost:27017`, then in two terminals:

```sh
cd watch-later-list-backend && npm install && node app.js    # API on :5000
cd watch-later-list-frontend && npm install && npm start     # interface on :3000
```

## API

| Method | Path | Does |
|---|---|---|
| `GET` | `/api/records` | Every entry |
| `POST` | `/api/records` | Add one: `{ name, platform, genre, link }` |
| `PUT` | `/api/records/:id` | Update one |
| `DELETE` | `/api/records/:id` | Remove one |

---

By [Ziyam Khan](https://ziyamkhan.com) · [GitHub](https://github.com/ziyam-khan)
