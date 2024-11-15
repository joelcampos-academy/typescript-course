---
sidebar_position: 1
---

# Tipos primitivos

En los ejemplos anteriores has entendido como indicar el tipo de un dato. Ahora es el momento de conocer los tipos primitivos que tienes disponibles. Son los siguientes:

- `number`: número entero o decimal. También existe `bigint` para números grandes.
- `string`: cadena de texto.
- `boolean`: valor verdadero o falso.
- `symbol`: identificadores únicos.
- `null`: utilizado literalmente para valores nulos.
- `undefined`: utilizado literalmente para valores `undefined`.

Ejemplos de uso:

```typescript
const edad: number = 20;
const nombre: string = "Puppycat";
const esHumano: boolean = false;
const comidaFavorita: null = null;
const casa: undefined = undefined;
const identificador: symbol = new Symbol(nombre);
```

La definición de los tipos puede parecer un poco redundante, entenderemos como hacerlo de una forma mejor en el siguiente punto.
