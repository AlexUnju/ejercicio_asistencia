## Ejercicio 20

Dibuje en toda la extensión del lienzo de (440, 420) rectángulos de idénticas medidas (40 ancho y 20 de alto) y que mantengan una distancia de 20 pixeles entre ellos tanto horizontal como verticalmente. Utilice la estructura de control repetitiva for. El lienzo debería verse así: </br>
<img src="https://i.ibb.co/6g0DjmY/Screenshot-2024-04-15-021039.png" alt="Screenshot-2024-04-15-021039" border="0"> </br>

## Análisis </br> 
**Datos de Entrada:** Rectángulos dibujados en el lienzo según las especificaciones dadas. </br>
**Datos de Salida:** Rectángulos dibujados en el lienzo según las especificaciones dadas. 	 

Proceso:  
**¿Quien debe realizar el proceso?:** El proceso puede ser realizado por un programa como processing. 
**¿Cual es el proceso que resuelve?:** dibujar una serie de rectángulos en un lienzo de tamaño específico, manteniendo una distancia específica entre ellos tanto horizontal como verticalmente, definiendo un bucle for para dibujar los rectángulos en el lienzo.
 </br>

## Diseño: 

**Entidad que resuelve el problema:** lienzo 

**Variables:**  
coordenadasRect: float //almacena un valor de coordenadas 

ancho, alto, distanciaEntreRect : int //almacena un valor entero 

anchoLienzo, altoLienzo: int //almacenan valores enteros 

 


## Proceso del algoritmo:</br>
**Nombre del Algoritmo: rectangulos_repetidos**</br>

```
    Inicio
    anchoLienzo ← 440
    altoLienzo ← 420
    ancho ← 40
    alto ← 20
    distanciaRect ← 20
    Para x ← coordenadasRect.x hasta anchoLienzo con paso (ancho+distanciaEntreRect) hacer
    Para y ← coordenadasRect.y hasta altoLienzo con paso (alto+distanciaEntreRect) hacer
    Dibujar rectángulo en (x, y, ancho, alto)
    Fin Para
    Fin Para
    Fin
```

## Codificación del algoritmo:

```

int distanciaEntreRect;
int alto;
int ancho;
PVector coordenadasRect;

void setup() {
  size(440, 420);
  background(235, 235, 200);
  distanciaEntreRect = 20;
  ancho = 40;
  alto = 20;
  coordenadasRect = new PVector(distanciaEntreRect, distanciaEntreRect);
}

void draw() {
  dibujarRectangulo();
}

void dibujarRectangulo() {
  for (float y = coordenadasRect.y; y < height; y += (alto + distanciaEntreRect)) {
    for (float x = coordenadasRect.x; x < width; x += (ancho + distanciaEntreRect)) {
      rect(x, y, ancho, alto);
      fill(255, 0, 0);
    }
  }
}

```



