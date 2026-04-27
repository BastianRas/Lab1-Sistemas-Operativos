# Lab1-Sistemas-Operativos

Ejecucion:

Flujo de trabajo para una ejecución "Limpia"
Ahora que ya sabes qué hace cada comando, te sugiero seguir este orden exacto para tu validación final:


Limpiar compilación: Ejecuta "make clean" para asegurar que no haya restos de código viejo.

Compilar: Ejecuta "make". Verás que se crean lab1.o, funciones.o y el ejecutable lab1.


Generar nueva imagen: Usa el script de Python para crear un nuevo caso de prueba.
"python3 GenerarDatos.py -o entrada.bin -r 50 -p 0.01"


Procesar: Corre tu programa en C.
"./lab1 -i entrada.bin -r 50 -t 100 -o reporte.csv -d"

Para ver si la imagen se limpió bien:
Este comando leerá tu archivo preprocesada.bin y generará un archivo .png que podrás abrir normalmente dándole doble clic en tu explorador de archivos.
"python3 Visualizer.py preprocesada.bin preprocesada.png"



. Para ver los círculos detectados (Esto abrirá una ventana):
Este script tomará la imagen original y las coordenadas de tu archivo reporte.csv, y abrirá una ventana visual (usando matplotlib) mostrando la imagen con cruces rojas donde tu programa detectó los centros
"python3 VerificacionVisual.py -i entrada.bin -c reporte.csv -r 50"
