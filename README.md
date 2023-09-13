# bun-vs-node
Benchmarked projects for testing Bun performance versus NodeJS performance while running NestJS projects out of the box.

The comparison results are presented on [this article](https://dev.to/mourishitz/running-nestjs-server-with-bun-4cdl).

## Benchmarking
To benchmark, install all dependencies using `npm install` and `bun install`.

After it, run both projects using `npm run start` and `bun start`.

By default Bun project will expose the `3333` port on localhost, and NodeJS project will expose `4444`.
This configuration can be changed inside src/main.ts on both projects.

As a benchmarking tool, it was used the wrk lib installed via AUR package.
Check here the [official wrk repository](https://github.com/wg/wrk/).

The configuration tags for benchmarking are:

``` bash
wrk -t12 -c400 -d30s http://127.0.0.1:3333/
```
*Note: remember to change ports and never run benchmarking at the same time, it may cause interference on the final results.

Made with 💜 by [@Mourishitz](https://github.com/Mourishitz)
