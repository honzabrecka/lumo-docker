# lumo-docker

[lumo](https://github.com/anmonteiro/lumo) with [boot](http://boot-clj.com/), [npm](https://docs.npmjs.com/cli/npm) and [yarn](https://yarnpkg.com/lang/en/)

```console
docker run --rm -it honzabrecka/lumo:1.8.0-beta
docker run --rm -it honzabrecka/lumo:1.7.0
```

```console
docker run --rm -it honzabrecka/lumo:1.8.0-beta bash
> npm install node-fetch
> boot -d funcool/promesa:1.9.0
> lumo -D "funcool/promesa:1.9.0"
>> (require '[promesa.core :as p])
>> (def fetch (js/require "node-fetch"))
>> (p/then
     (fetch "https://honzabrecka.com/api/status")
     #(println (.. % -status)))
```
