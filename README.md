# Subtitles playground

This playground serve to play with subtitles on movies.

## Requirements

- [`docker`](https://www.docker.com/)

## How to launch

First launch container:

```sh
$ docker compose up -d
[+] Running 8/8
 ✔ nginx 7 layers [⣿⣿⣿⣿⣿⣿⣿]      0B/0B      Pulled                     5.1s
   ✔ 2f44b7a888fa Pull complete                                         1.1s
   ✔ 8b7dd3ed1dc3 Pull complete                                         1.3s
   ✔ 35497dd96569 Pull complete                                         0.4s
   ✔ 36664b6ce66b Pull complete                                         0.9s
   ✔ 2d455521f76c Pull complete                                         1.4s
   ✔ dc9c4fdb83d6 Pull complete                                         1.5s
   ✔ 8056d2bcf3b6 Pull complete                                         1.7s
[+] Running 2/2
 ✔ Network test-subtitles_default     Created                           0.1s
 ✔ Container test-subtitles-nginx-1  Started
```

Then go to `http://localhost:80`. You will be able to see [`index.html`](./src/index.html).

You can now edit [`index.html`](./src/index.html) and refresh your browser to see
updates.

## Why are we using a web server

You can ask, why are we using a [`web server`](https://en.wikipedia.org/wiki/Web_server)
instead of open [`index.html`](./src/index.html) in browser?

This is because of browsers security, we can't open subtitles from files or
different origin, so we must use a [`web server`](https://en.wikipedia.org/wiki/Web_server)
to allow browser to accept vtt file.

# LICENSE

[MIT](/LICENSE)