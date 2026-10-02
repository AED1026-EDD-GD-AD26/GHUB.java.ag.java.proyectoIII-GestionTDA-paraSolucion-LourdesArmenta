# Del TDA al programa: poniendo a prueba mi modelo

## Unidad III. Estructuras Lineales

1. Propósito de la actividad

En la Unidad I diseñaste un Tipo de Dato Abstracto (TDA) para representar una situación de la vida real.

Ahora tendrás que dar un paso más: convertir ese modelo en un programa en Java.

El propósito de esta actividad es que compruebes si el TDA que diseñaste contiene toda la información necesaria para desarrollar un programa funcional.

Durante la implementación podrás descubrir que necesitas agregar clases, atributos, relaciones u operaciones que no habías considerado originalmente. Esto es parte del aprendizaje.

No se busca que tu primer diseño sea perfecto. Se busca que aprendas a identificar y corregir las necesidades que aparecen al intentar implementarlo.

## NOTA: El resto de la información la encontrarás en el documento adjunto en la tarea de moodle.

## Uso del proyecto con make

### Default - Compilar+Probar+Ejecutar
```
make
```
### Compilar
```
make compile
```
### Probar todo
```
make test
```
### Ejecutar App
```
make run
```
### Limpiar binarios
```
make clean
```
## Comandos Git-Cambios y envío a Autograding

### Por cada cambio importante que haga, actualice su historia usando los comandos:
```
git add .
git commit -m "Descripción del cambio"
```
### Envíe sus actualizaciones a GitHub para Autograding con el comando:
```
git push origin main
```
## Comandos individuales
### Compilar

```
find ./ -type f -name "*.java" > compfiles.txt
javac -d build -cp lib/junit-platform-console-standalone-1.5.2.jar @compfiles.txt
```
Ejecutar ambos comandos en 1 sólo paso:

```
find ./ -type f -name "*.java" > compfiles.txt ; javac -d build -cp lib/junit-platform-console-standalone-1.5.2.jar @compfiles.txt
```


### Ejecutar Todas la pruebas locales de 1 Test Case

```
java -jar lib/junit-platform-console-standalone-1.5.2.jar -class-path build --select-class miTest.AppTest
```
### Ejecutar 1 prueba local de 1 Test Case

```
java -jar lib/junit-platform-console-standalone-1.5.2.jar -class-path build --select-method miTest.AppTest#appHasAGreeting
```
### Ejecutar App
```
java -cp build miPrincipal.Principal
```
Los comandos anteriores están considerados para un ambiente Linux. [Referencia.](https://www.baeldung.com/junit-run-from-command-line)
