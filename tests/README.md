# Pruebas

Aquí van las pruebas del proyecto. La regla: **cada requisito (RF) de la spec tiene al menos una prueba**, y el nombre de la prueba lo dice:

```
RF-2: si no hay resultados, muestra el mensaje de lista vacía
```

La CI (`.github/workflows/ci.yml`) las ejecuta en cada pull request. Detecta sola si el proyecto usa Node (`npm test`) o Python (`pytest`); si usan otra cosa, ajusten ese archivo.
