# 🎨 Actividad de Bootstrap: Tarjetas de Perfil con Estilo Glassmorphic

¡Hola! Este repositorio contiene el desarrollo de la actividad práctica de Bootstrap en la cual implementamos un diseño de tarjetas de presentación interactivas para perfiles de estudiantes, dándole un toque personalizado y moderno.

## 📷 Vista Previa del Proyecto
![Captura del proyecto](/images/captura-de-la-actividad.png)

## 🚀 ¿De qué trató la actividad?
La práctica consistió en consolidar los fundamentos de **Bootstrap 5**, aplicando conceptos clave como:
1. **Estructura base en HTML5** utilizando los componentes oficiales de Bootstrap.
2. **Sistema de Rejilla (Grid):** Uso de contenedores (`container`), filas (`row`) y columnas responsivas (`col-md-4`) para alinear tres tarjetas de forma horizontal que se adaptan automáticamente a dispositivos móviles y de escritorio.
3. **Clases de Utilidad:** Implementación de clases nativas de Bootstrap para espaciados, bordes redondeados (`rounded`), sombras (`shadow`) y alineación de textos (`text-center`).
4. **Personalización avanzada (UI/UX):** Salirse del diseño plano predeterminado incorporando estilos propios en CSS para lograr un aspecto moderno de **Glassmorphism (vidrio esmerilado)** con bordes translúcidos, sombras naranjas dinámicas al pasar el cursor y botones tipo pastilla.

---

## 💻 Tecnologías Utilizadas
* **HTML5** para la estructura semántica de la página.
* **Bootstrap 5.3.3 (CDN)** para el sistema de rejilla y estilos base.
* **CSS3 Personalizado** para efectos visuales avanzados (`backdrop-filter`, transiciones y paleta de colores oscura).

---

## 🛠️ Estructura del Código

### 1. El HTML (`index.html`)
Se organizó una sección contenedora de tres tarjetas distribuidas en columnas de tamaño mediano (`col-md-4`):

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfiles - Bootstrap</title>
    <!-- Bootstrap CSS -->
    <link href="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css)" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <!-- Estilos personalizados -->
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <div class="container my-5">
        <div class="row">
            <!-- Tarjeta 1 -->
            <div class="col-md-4">
                <div class="card h-100 shadow rounded text-center m-3 custom-card">
                    <img src="profile-image.jpg" class="card-img-top rounded-top" alt="Foto de perfil">
                    <div class="card-body">
                        <h5 class="card-title">Ana Sofia Peñaloza</h5>
                        <p class="card-text">Estudiante en Desarrollo de Software</p>
                        <a href="#" class="btn btn-primary">Ver Perfil</a>
                    </div>
                </div>
            </div>

            <!-- Tarjeta 2 -->
            <div class="col-md-4">
                <div class="card h-100 shadow rounded text-center m-3 custom-card">
                    <img src="profile-image-2.jpg" class="card-img-top rounded-top" alt="Foto de perfil">
                    <div class="card-body">
                        <h5 class="card-title">Marco</h5>
                        <p class="card-text">Estudiante en Ingenieria Mecatrónica</p>
                        <a href="#" class="btn btn-primary">Ver Perfil</a>
                    </div>
                </div>
            </div>

            <!-- Tarjeta 3 -->
            <div class="col-md-4">
                <div class="card h-100 shadow rounded text-center m-3 custom-card">
                    <img src="profile-image-3.jpg" class="card-img-top rounded-top" alt="Foto de perfil">
                    <div class="card-body">
                        <h5 class="card-title">Andrea</h5>
                        <p class="card-text">Estudiante en Diseño Grafico</p>
                        <a href="#" class="btn btn-primary">Ver Perfil</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Bootstrap JS Bundle -->
    <script src="[https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js)" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9NkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>

```css
html, body {
    background-color: #121212 !important;
    color: white !important;
    min-height: 100vh;
    margin: 0;
}

.custom-card {
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.03));
    backdrop-filter: blur(100px);
    -webkit-backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.15) !important;
    border-radius: 24px !important; 
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    color: white;
}

.custom-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 30px orange !important;
}

.custom-card .card-img-top {
    height: 220px;
    object-fit: cover;
}

.custom-card .btn-primary {
    background-color: rgba(255, 255, 255, 0.2);
    border: 1px solid rgba(255, 255, 255, 0.3);
    border-radius: 50px;
    color: white;
    font-weight: 500;
    transition: background 0.3s ease;
    width: 200px;
}

.custom-card .btn-primary:hover {
    background: rgba(255, 255, 255, 0.4);
    border-color: rgba(255, 255, 255, 0.5);
    color: #ffffff;
}