# Simulación de Aparcamiento Concurrente con Semaphore

## Descripción
Este proyecto simula un aparcamiento con 3 plazas y 7 coches que intentan acceder simultáneamente, utilizando la clase `Semaphore` de Java para gestionar los recursos limitados (plazas de aparcamiento). El objetivo es demostrar el uso de semáforos para controlar el acceso concurrente a recursos compartidos.

## Clases
- **Aparcamiento**: Gestiona las plazas y controla el acceso concurrente utilizando un semáforo.
- **Coche**: Representa cada coche, actuando como un hilo que intenta acceder al aparcamiento, se estaciona durante un tiempo aleatorio y luego sale.
- **PrincipalParking**: Es el punto de entrada donde se inicializan el aparcamiento y los coches, y se lanzan los hilos.

## Cómo ejecutar
1. Clona el repositorio.
2. Compila y ejecuta la clase `PrincipalParking`.
3. Se iniciarán 7 hilos, cada uno representando un coche, que intentará aparcar en el aparcamiento.

## Uso de `Semaphore`
La clase `Semaphore` se utiliza para controlar el número de coches que pueden estar estacionados al mismo tiempo. Utilizar semáforos garantiza que nunca haya más de 3 coches estacionados, evitando condiciones de carrera y garantizando la seguridad de los hilos.

### Ventajas de `Semaphore` frente a otras alternativas
- **Ventajas sobre `synchronized`**: `Semaphore` permite un control más fino de los permisos, ofreciendo un número configurable de permisos simultáneos, mientras que `synchronized` solo permite acceso exclusivo a un recurso.
- **Ventajas sobre `ReentrantLock`**: `Semaphore` es más adecuado cuando se gestionan recursos con un número limitado de permisos (como las plazas de aparcamiento), ya que no requiere una adquisición explícita de bloqueos o liberar los recursos manualmente.

## Capturas de Pantalla

