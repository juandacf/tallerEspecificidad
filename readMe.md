TALLER ESPECIFICIDAD

Parte 1: Introducción Teórica a la Especificidad (15 minutos)

1.  ¿Qué es la especificidad?
    R/ En CSS, la especificidad es un valor por cual los navegadores determinan, en caso de existir un conflicto, qué valores o propiedades de CSS son más relevantes y, por lo tanto, son aplicados(1). La cantidad de especificidad de un selector se mide usando cuatro valores diferentes, separados por coma, que tienen diferente peso y pueden describirse como millares, centenas, decenas y unidades (2). Los selectores más comunes son los IDs, clases, pseudoclases, atributos y elementos.

2.  Reglas de cálculo de especificidad:
    El selector universal, representado por un asterisco, tiene un valor 0. Los elementos (etiquetas directas de HTML como h1 y p) y subelementos (selectores especiales que suelen ser identificados por el prefijo :: como ::before o ::after) tienen un peso en unidades. Las clases, atributos y pseudoclases (ejemplo: .clases, [atributos] y :pseudoclases) tienen un peso medido en decenas. Los IDs (por ejemplo, #id) tienen un peso medido en centenas y los estilos dentro de línea, tienen un peso medido en millares. Por último, cabe resaltar el !important, que se sobrepone a todos los anteriores (2).

Parte 2: Ejemplos Prácticos

1. Ejemplo básico: Demuestra como los diferentes selectores afectan la especificidad
   ![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/1ejemploBasico.jpg)

   R/En este ejemplo, el color del texto es rojo porque el selector de ID tiene mayor especificidad que los selectores de clase y etiqueta

2. Demostración de !important
   ![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/demostracionImportant.jpg)

   R/ En este caso, el color del texto es azul porque el !important se sobrepone a cualquier elemento.

Parte 3: Ejercicios Prácticos

Ejercicio 1: Calculando la Especificidad

Dado el siguiente código, pide a los participantes que calculen la especificidad y determinen qué estilos se aplicarán:

![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/ejercicio1CalculandoEspecificidad.jpg)

En este caso, la especificidad del selector h1 es (0,0,1), la de .content h1 es (0,1,1) y la de #main h1 es (1,0,1).

¿Qué color tendrá el título h1?
R/ Ya que el valor de especificidad más grande es el de #main h1, se aplicará el color rojo:

![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/ceResuelto.jpg)

Ejercicio 2: Resolviendo Conflictos de Especificidad

Modifica el siguiente código para que el párrafo tenga color amarillo, sin usar !important.

![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/ejercicio2Conflictos.jpg)

Para lograr que el párrafo tenga color amarillo, se usó como selector #box .text porque el un selector de ID tiene un valor de especificidad más alto que uno de clase, como se muestra en la siguiente imagen:

![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/ejercicio2Resuelto.jpg)

Parte 4: Desafío Final

Dales a los participantes un archivo HTML con múltiples elementos y clases, y pídeles que agreguen estilos CSS para lograr un diseño específico. Deberán aplicar todo lo aprendido sobre especificidad para resolver los conflictos y obtener el resultado correcto.

Desafio CSS:

El h1 en el .header debe ser de color blanco.
El texto del p en .content debe ser rojo.
El texto del footer debe ser gris.

Para la solución de este ejercicio, se utilizaron los siguientes selectores:

![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/ejercicioFinal.jpg)

Referencias:

1.https://developer.mozilla.org/es/docs/Web/CSS/Specificity

2.https://dev.to/lupitacode/especificidad-en-css-que-es-y-como-funciona-52k6
