# 🚀 Actividad: ¡Sube de Nivel! (Perfil de Videojuego)

En esta actividad vas a crear el perfil de un personaje de videojuego. Aprenderás a usar cajas fuertes (const) para las cosas que nunca cambian, y cajas normales (let) para las cosas que se actualizan mientras juegas. ¡También veremos qué pasa si intentas hackear el juego! 👾

Al final, tu programa simulará que tu personaje subió de nivel y mostrará sus estadísticas actualizadas.

## 🛠️ Lo que necesitas (Requisitos)

1. Intérprete de **JavaScript** instalado en tu computadora. Te recomendamos usar `Node.js`. Puedes verificar si lo tienes abriendo tu terminal y escribiendo:
   ```bash
   which node # Debería mostrar algo como /usr/local/bin/node o una ruta similar
   ```
2. Un editor de código para escribir tu código. Te recomendamos usar **Visual Studio Code**. Verifica si lo tienes con:
   ```bash
   which code # Debería mostrar algo como /usr/local/bin/code o una ruta similar
   ```
3. Recordar la diferencia entre texto (`String`) y números (`Number`). ¡Acuérdate de las comillas!
4. ¡Un cerebro humano funcional! 🧠

## 💡 Tip Pro: ¡Usa Emojis en tus Strings!
¡Puedes hacer que tu texto (`Strings`) sea mucho más divertido usando emojis! 🚀
* En **Mac**, puedes abrir el teclado de emojis presionando `Ctrl + Cmd + Espacio` al mismo tiempo.
* También puedes copiarlos y pegarlos desde páginas como [emojicopy.com](https://emojicopy.com/).
¡Pruébalo cuando escribas el nombre o la clase de tu personaje!

## 📝 Pasos a seguir
1. Dentro de tu carpeta dedicada a estas clases, crea una nueva carpeta llamada `practica_2_personaje_videojuego`.
2. Entra a esa nueva carpeta y crea un archivo llamado `app.js` ¡Aquí vivirá tu código!
3. Abre tu archivo `app.js` con code.
4. Todo buen personaje necesita un nombre y una clase (Mago, Guerrero, Ninja). Como **estas cosas no cambian a mitad del juego**, usa variables inmutables (`const`) y texto (`String`):

```js
const nombre_personaje = "Master Chief 🪖";
const clase = "Soldado";
```
_(¡Ponle el nombre y la clase que tú quieras!)_

5. Ahora, tu personaje necesita estadísticas: un nivel y puntos de vida (HP). Como estas cosas **sí van a cambiar cuando juegues**, usa variables mutables (`let`) y números (`Number` - ¡sin comillas!):

```js
let nivel = 1;
let puntos_vida = 100;
```

6. Muestra en la pantalla las estadísticas iniciales de tu personaje usando `console.log()`:

```js
console.log("¡Bienvenido al juego, " + nombre_personaje + " el " + clase + "!");
console.log("Nivel actual: " + nivel);
console.log("Vida actual: " + puntos_vida);
```

7. **¡Acción!** Imagina que acabas de derrotar a un monstruo. Vamos a actualizar tus variables mutables (let). Súmale 1 a tu nivel y réstale 20 a tus puntos de vida por los golpes que recibiste:

```js
nivel = nivel + 1;
puntos_vida = puntos_vida - 20;
```

_Nota que aquí ya no pusimos la palabra let al principio. Como la caja ya estaba creada, solo la estamos abriendo para cambiar lo que tiene adentro._

8. Imprime un mensaje anunciando la victoria y las nuevas estadísticas:

```js
console.log("⚔️ ¡Monstruo derrotado! ⚔️");
console.log("Nuevo nivel: " + nivel);
console.log("Vida restante: " + puntos_vida);
```

9. **Ejecuta tu programa** en la terminal con `node app.js` y revisa que los números hayan cambiado correctamente.

10. **El Reto Hacker (El error intencional)**: Vamos a intentar hacer trampa. Al final de tu código, intenta cambiar el nombre de tu personaje (que es un `const`):

```js
nombre_personaje = "Darth Vader";
```

11. Vuelve a ejecutar el programa con `node app.js`. ¡BOOM! 💥 La terminal te lanzará un error rojo. Lee el error. Te dirá `TypeError: Assignment to constant variable`.. ¡Felicidades, acabas de comprobar que una const es una caja fuerte que nadie puede hackear! Borra o comenta esa línea para que tu programa vuelva a funcionar.

## 🌟 Programa completo (Sin el error)
Si seguiste los pasos, tu archivo app.js se verá más o menos así:

```js
// 1. Datos fijos (const + Strings)
const nombre_personaje = "Master Chief 🪖";
const clase = "Soldado";

// 2. Datos que cambian (let + Numbers)
let nivel = 1;
let puntos_vida = 100;

// 3. Mostrar estado inicial
console.log("¡Bienvenido al juego, " + nombre_personaje + " el " + clase + "!");
console.log("Nivel actual: " + nivel);
console.log("Vida actual: " + puntos_vida);

// 4. Actualizar las variables (El juego en acción)
nivel = nivel + 1;
puntos_vida = puntos_vida - 20;

// 5. Mostrar estado final
console.log("⚔️ ¡Monstruo derrotado! ⚔️");
console.log("Nuevo nivel: " + nivel);
console.log("Vida restante: " + puntos_vida);
```