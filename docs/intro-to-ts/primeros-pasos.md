---
sidebar_position: 2
---

# Primeros pasos

Vamos a inicializar un script en TS.
Primero, vamos al directorio donde queremos crear nuestro script (deberíamos elegir uno nuevo ya que se crearán varios archivos). Debemos tener Node y npm instalado en nuestro sistema.

Ejecutamos:

```shell
npm init
```

Indicamos un nombre para nuestro proyecto. El resto de campos los podemos dejar con los valores por defecto, los modificaremos y entenderemos más adelante.

Creamos el archivo `index.ts` dentro de nuestro directorio y lo abrimos.
Este será el archivo donde escribiremos nuestro código en TS (vemos que la extensión para archivos TS es _.ts_).

Pero antes de empezar a escribir nuestro código debemos instalar el paquete de TS. Lo hacemos mediante:

```shell
npm i -D typescript
```

Vemos que utilizamos la flag _-D_. Esto significa que el paquete solo estará disponible durante el desarrollo, jamás en producción. Esto se debe a que, como hemos comentado anteriormente, lo que se ejecuta realmente es código JS. Este paquete lo utilizaremos para compilar el código TS en JS.

Luego, ejecutamos:

```shell
npx tsc --init
```

Esto nos habrá inicializado el proyecto creando el fichero `tsconfig.json`. Más adelante endenderemos en profundidad este fichero.

Ahora sí, podemos empezar a escribir código en TS.

Abrimos el archivo que hemos creado y escribimos el siguiente código de ejemplo:

```typescript
const numero1: number = 2;
const numero2: number = 4;

const resultado: number = numero1 + numero2;

console.log(resultado);
```

Este código suma dos variables, almacena el resultado en otra variable e imprime el resultado en la consola.
Este código podría ser simplemente JS, pero si nos fijamos le hemos añadido el tipo de datos `number`. Más adelante hablaremos sobre la sintaxis de TS, por ahora vamos a intentar ejecutrar el código con Node.js.

## Compilar y ejecutar

Como hemos dicho, no podemos ejecutar este código directamente. Primero debemos compilarlo a JS. Esto lo hacemos ejecutando `tsc index.ts`. Crearemos un script que haga eso de la siguiente manera:

- Abrimos el archivo `package.json`.
- Creamos un nuevo script llamado `compile`.
- Accedemos al fichero `tsconfig.json` y añadimos `"outDir": "./dist/"` dentro de `compilerOptions`.

Ahora, abrimos nuestra terminal y lanzamos:

```shell
npm run compile
```

Vemos que se creará una carpeta llamada `dist` con un fichero `index.js`. Si abrimos el fichero veremos nuestro código pero siendo este JS en vez de TS. Este código ya lo podemos ejecutar con:

```shell
node dist/index.js
```

Vemos que el código se ha ejecutado.
