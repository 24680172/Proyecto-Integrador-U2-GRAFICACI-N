# 1. Configuración del Espacio de Trabajo (Setup)
Blender no es solo para cubos 3D; tiene un entorno específico para dibujo 2D llamado Grease Pencil.

Selección de Plantilla: Al inicio, se elige 2D Animation. Esto configura la cámara en una vista ortográfica perfecta y cambia el fondo a un color sólido (normalmente gris claro o blanco).

Capas de Dibujo: En el panel de propiedades del objeto (icono de garabato verde), se crean niveles de organización. Es vital separar Lines (contornos) de Fills (rellenos) para que, al colorear, la pintura no "pise" el trazo negro.

# 2. Definición de Materiales y Pinceles
A diferencia de Photoshop, en Blender un trazo es un objeto vectorial con un "material" asignado.

Stroke vs Fill: Se crean materiales específicos. Uno que solo tenga activado el Stroke (para el delineado) y otro que solo tenga activado el Fill (para el color sólido).

Sensibilidad: Se ajusta el radio y la opacidad del pincel para que reaccione a la presión de la tableta gráfica, logrando trazos con terminaciones finas y orgánicas.

# 3. El Proceso de Animación: "Pose a Pose"
El autor no dibuja cada cuadro desde cero (eso sería eterno). Utiliza una técnica de animación planificada:

Keyframes Primarios: Dibuja la "Pose A" (inicio) y la "Pose B" (fin).

Onion Skinning (Papel Cebolla): Activa esta función para ver el dibujo anterior en color verde y el siguiente en azul. Esto sirve de guía para que el personaje no cambie de tamaño accidentalmente.

Modo Esculpir (Sculpt Mode): En lugar de borrar y redibujar, el autor usa herramientas como Push o Grab (como si fuera plastilina) para mover ligeramente las líneas del dibujo anterior y crear la nueva posición. Esto mantiene la consistencia del trazo perfectamente.

![8049563](https://github.com/user-attachments/assets/a008d15f-3ca2-4ec8-a6e7-f944e03f5e64)


# 4. Interpolación Automática (Sequence)
Esta es la magia del video. Blender puede calcular el movimiento intermedio entre dos dibujos si tienen la misma cantidad de puntos.

Se seleccionan los dos fotogramas clave en el Dope Sheet.

Se ejecuta el comando Grease Pencil > Interpolate > Sequence.

Blender genera automáticamente todos los dibujos intermedios, creando una fluidez que manualmente tomaría horas.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/62d1a7f0-0db3-480a-a236-1fc3471aaa28" />


# 5. Efectos de Post-Procesamiento (VFX)
Para que la animación no se vea "plana" o demasiado digital, se añaden modificadores y efectos de capa:

Noise Modifier: Añade un ligero temblor a las líneas para que parezca dibujado a mano tradicionalmente (estilo vibrating lines).

Glow/Blur: En el panel de Visual Effects Properties, se añade un brillo suave para que los colores "sangren" un poco y se sientan más vivos.

# 6. Renderizado y Salida
Finalmente, se prepara el archivo para compartirlo:

Se define la resolución (usualmente 1920x1080).

Se configura el Frame Rate (el video original suele estar a 24 o 12 fps para ese look cinematográfico).

Se exporta usando el motor Eevee, que es extremadamente rápido para procesar dibujos 2D.
