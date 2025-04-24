# Estaciones
https://github.com/XBruno1/Estaciones.git

🌤️ Sistema Meteorológico con Seguridad HMAC
📌 Descripción
Este sistema permite registrar y validar datos meteorológicos de forma segura utilizando HMAC-SHA256 para proteger la información. Organizado bajo el patrón Modelo-Vista-Controlador (MVC), se asegura de mantener una estructura clara y modular. La interfaz de usuario está desarrollada con Gradio, ofreciendo una experiencia visual amigable y fácil de usar.

Características Principales
✅ Estructura organizada con Modelo-Vista-Controlador (MVC) para mayor claridad y mantenimiento.
✅ HMAC-SHA256 garantiza la integridad de los datos mediante encriptación segura.
✅ Interfaz gráfica interactiva creada con Gradio, mejorando la experiencia del usuario.
✅ Lista predeterminada de estaciones meteorológicas, que incluye:
🌧️ Lluvia
☀️ Sol
🌥️ Nublado
❄️ Nevado
⛈️ Tormenta
🌫️ Neblina
💨 Viento fuerte
✅ Verificación de registros encriptados, lo que asegura la autenticidad de los datos ingresados.
✅ Función para guardar los datos en CSV, facilitando su disponibilidad futura.

Estructura del Proyecto
/EstacionMeteo/
├── modelo/
│ └── estacion_meteorologica.py # Manejo de datos y encriptación con HMAC
├── vista/
│ └── vista_gradio.py # Interfaz gráfica interactiva
├── controlador/
│ └── controlador.py # Coordinación entre modelo y vista
├── main.py # Conexión de todos los componentes
├── requirements.txt # Dependencias del proyecto
├── README.md # Documentación del proyecto
└── .gitignore # Archivos a excluir del repositorio

Instalación de dependencias:

bash
Copiar
Editar
pip install -r requirements.txt
Ejecutar el sistema:

bash
Copiar
Editar
python main.py

Seguridad

Este sistema emplea HMAC-SHA256 para proteger los registros meteorológicos. Cada entrada se cifra usando una clave secreta (CLAVE_SECRETA) y no se puede revertir. 💡 Nota importante:

Los datos cifrados solo pueden ser verificados con la clave secreta.

Si la clave no coincide, los datos no serán aceptados por el sistema.
Este enfoque asegura que la información no pueda ser manipulada sin que se detecte.

