TALLER ESPECIFICIDAD

Parte 1: Introducción Teórica a la Especificidad (15 minutos)

1.  ¿Qué es la especificidad?
    R/ En CSS, la especificidad es un valor por cual los navegadores determinan, en caso de existir un conflicto, qué valores o propiedades de CSS son más relevantes y, por lo tanto, son aplicados(1). La cantidad de especificidad de un selector se mide usando cuatro valores diferentes, separados por coma, que tienen diferente peso y pueden describirse como millares, centenas, decenas y unidades (2). Los selectores más comunes son los IDs, clases, pseudoclases, atributos y elementos.

2.  Reglas de cálculo de especificidad:
    El selector universal, representado por un asterisco, tiene un valor 0. Los elementos (etiquetas directas de HTML como <h1> y <p>) y subelementos (selectores especiales que suelen ser identificados por el prefijo :: como ::before o ::after) tienen un peso en unidades. Las clases, atributos y pseudoclases (ejemplo: .clases, [atributos] y :pseudoclases) tienen un peso medido en decenas. Los IDs (por ejemplo, #id) tienen un peso medido en centenas y los estilos dentro de línea, tienen un peso medido en millares (por ejemplo, <p style="background-color: orange;">. Por último, cabe resaltar el !important, que se sobrepone a todos los anteriores (2).

Parte 2: Ejemplos Prácticos

1. Ejemplo básico: Demuestra como los diferentes selectores afectan la especificidad
   ![alt text] ()

   ![alt text](https://github.com/juandacf/tallerEspecificidad/blob/main/media/1ejemploBasico.jpg)

Referencias: 1.https://developer.mozilla.org/es/docs/Web/CSS/Specificity 2.https://dev.to/lupitacode/especificidad-en-css-que-es-y-como-funciona-52k6
