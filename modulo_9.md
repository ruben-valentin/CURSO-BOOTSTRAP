## Módulo 9: Componentes Avanzados

### 9.1 Acordeón
```html
<div class="accordion" id="accordionExample">
    <div class="accordion-item">
        <h2 class="accordion-header">
            <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne">
                Sección 1
            </button>
        </h2>
        <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
            <div class="accordion-body">
                Contenido de la sección 1
            </div>
        </div>
    </div>
    <div class="accordion-item">
        <h2 class="accordion-header">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo">
                Sección 2
            </button>
        </h2>
        <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
            <div class="accordion-body">
                Contenido de la sección 2
            </div>
        </div>
    </div>
</div>
```

### 9.2 Tooltips y Popovers

#### Tooltips
```html
<button type="button" class="btn btn-secondary" 
        data-bs-toggle="tooltip" 
        data-bs-placement="top" 
        title="Tooltip en la parte superior">
    Botón con Tooltip
</button>

<script>
// Inicializar todos los tooltips
const tooltipTriggerList = document.querySelectorAll('[data-bs-toggle="tooltip"]')
const tooltipList = [...tooltipTriggerList].map(tooltipTriggerEl => new bootstrap.Tooltip(tooltipTriggerEl))
</script>
```

#### Popovers
```html
<button type="button" class="btn btn-lg btn-danger" 
        data-bs-toggle="popover" 
        title="Título del Popover" 
        data-bs-content="Contenido del popover aquí.">
    Clic para toggle popover
</button>

<script>
// Inicializar todos los popovers
const popoverTriggerList = document.querySelectorAll('[data-bs-toggle="popover"]')
const popoverList = [...popoverTriggerList].map(popoverTriggerEl => new bootstrap.Popover(popoverTriggerEl))
</script>
```

### 9.3 Offcanvas
```html
<button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample">
    Abrir Offcanvas
</button>

<div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasExample">
    <div class="offcanvas-header">
        <h5 class="offcanvas-title">Título del Offcanvas</h5>
        <button type="button" class="btn-close" data-bs-dismiss="offcanvas"></button>
    </div>
    <div class="offcanvas-body">
        <div>
            Contenido del offcanvas aquí
        </div>
    </div>
</div>
```

## Módulo 10: Formularios Avanzados

### 10.1 Validación de Formularios
```html
<form class="needs-validation" novalidate>
    <div class="mb-3">
        <label for="username" class="form-label">Usuario</label>
        <input type="text" class="form-control" id="username" required>
        <div class="invalid-feedback">
            Por favor ingresa un nombre de usuario.
        </div>
    </div>
    <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <input type="email" class="form-control" id="email" required>
        <div class="invalid-feedback">
            Por favor ingresa un email válido.
        </div>
    </div>
    <button class="btn btn-primary" type="submit">Enviar</button>
</form>

<script>
// Ejemplo de JavaScript para la validación de formularios
(function () {
    'use strict'
    const forms = document.querySelectorAll('.needs-validation')
    Array.from(forms).forEach(form => {
        form.addEventListener('submit', event => {
            if (!form.checkValidity()) {
                event.preventDefault()
                event.stopPropagation()
            }
            form.classList.add('was-validated')
        }, false)
    })
})()
</script>
```

### 10.2 Input Groups
```html
<div class="input-group mb-3">
    <span class="input-group-text">@</span>
    <input type="text" class="form-control" placeholder="Username">
</div>

<div class="input-group mb-3">
    <input type="text" class="form-control" placeholder="Cantidad">
    <span class="input-group-text">€</span>
</div>

<div class="input-group mb-3">
    <button class="btn btn-outline-secondary" type="button">Botón</button>
    <input type="text" class="form-control" placeholder="Búsqueda">
</div>
```

## Módulo 11: Animaciones y Transiciones

### 11.1 Animaciones con CSS
```css
/* Definir animaciones personalizadas */
.fade-in {
    animation: fadeIn 0.5s ease-in;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Transiciones de Bootstrap */
.fade {
    transition: opacity .15s linear;
}

.collapse {
    transition: height .35s ease;
}
```

### 11.2 Implementación de Animaciones
```html
<!-- Ejemplo de uso de animaciones -->
<div class="alert alert-success fade-in">
    ¡Operación exitosa!
</div>

<!-- Transición de collapse -->
<p>
    <button class="btn btn-primary" type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample">
        Toggle Collapse
    </button>
</p>
<div class="collapse" id="collapseExample">
    <div class="card card-body">
        Contenido que se muestra/oculta con animación
    </div>
</div>
```

## Módulo 12: Optimización y Rendimiento

### 12.1 Optimización del CSS
```html
<!-- Cargar solo los componentes necesarios -->
<link href="bootstrap.min.css" rel="stylesheet">

<!-- CSS personalizado al final -->
<link href="custom.min.css" rel="stylesheet">
```

### 12.2 Optimización de JavaScript
```html
<!-- Cargar scripts al final del body -->
<script src="bootstrap.bundle.min.js"></script>

<!-- Inicialización eficiente de componentes -->
<script>
document.addEventListener('DOMContentLoaded', function() {
    // Inicializar todos los tooltips de una vez
    const tooltipTriggerList = document.querySelectorAll('[data-bs-toggle="tooltip"]');
    [...tooltipTriggerList].map(tooltipTriggerEl => new bootstrap.Tooltip(tooltipTriggerEl));

    // Inicializar todos los popovers
    const popoverTriggerList = document.querySelectorAll('[data-bs-toggle="popover"]');
    [...popoverTriggerList].map(popoverTriggerEl => new bootstrap.Popover(popoverTriggerEl));
});
</script>
```

## Módulo 13: Integración con Otros Frameworks

### 13.1 Uso con JavaScript Moderno
```javascript
// Importar Bootstrap en un proyecto moderno
import 'bootstrap/dist/css/bootstrap.min.css';
import { Modal } from 'bootstrap';

// Usar componentes programáticamente
document.addEventListener('DOMContentLoaded', () => {
    const modalElement = document.getElementById('myModal');
    const modal = new Modal(modalElement);
    
    // Abrir modal
    document.getElementById('openModal').addEventListener('click', () => {
        modal.show();
    });
    
    // Eventos del modal
    modalElement.addEventListener('shown.bs.modal', () => {
        console.log('Modal mostrado');
    });
});
```

### 13.2 Integración con Frameworks Frontend
```javascript
// React ejemplo
import { useState } from 'react';
import 'bootstrap/dist/css/bootstrap.min.css';

function App() {
    const [show, setShow] = useState(false);
    
    return (
        <div className="container">
            <button 
                className="btn btn-primary"
                onClick={() => setShow(!show)}>
                Toggle Content
            </button>
            
            {show && (
                <div className="alert alert-info mt-3">
                    Contenido Condicional
                </div>
            )}
        </div>
    );
}
```

## Ejercicios Prácticos

### Ejercicio 1: Landing Page
Crear una landing page responsive que incluya:
- Navbar con menú hamburguesa
- Hero section con imagen de fondo
- Sección de características con cards
- Formulario de contacto
- Footer con links sociales

### Ejercicio 2: Dashboard
Crear un dashboard administrativo que incluya:
- Sidebar navegación
- Gráficos y estadísticas
- Tablas de datos
- Formularios de entrada
- Modales y alertas

### Ejercicio 3: E-commerce
Crear una página de producto que incluya:
- Galería de imágenes
- Información del producto
- Selector de variantes
- Botón de compra
- Productos relacionados

## Recursos y Referencias

### Documentación Oficial
- [Bootstrap Documentation](https://getbootstrap.com/docs/)
- [Bootstrap Examples](https://getbootstrap.com/docs/5.3/examples/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)

### Herramientas Útiles
- [Bootstrap Themes](https://themes.getbootstrap.com/)
- [Bootstrap CDN](https://www.bootstrapcdn.com/)
- [Bootstrap Build Tools](https://getbootstrap.com/docs/5.3/getting-started/build-tools/)

### Comunidad y Soporte
- [Stack Overflow Bootstrap Tag](https://stackoverflow.com/questions/tagged/bootstrap-5)
- [GitHub Issues](https://github.com/twbs/bootstrap/issues)
- [Bootstrap Blog](https://blog.getbootstrap.com/)

## Evaluación y Certificación

### Criterios de Evaluación
1. Comprensión de conceptos fundamentales
2. Implementación correcta de componentes
3. Uso apropiado del sistema grid
4. Responsive design
5. Optimización y buenas prácticas
6. Personalización y creatividad

### Proyecto Final
El proyecto final debe demostrar:
- Uso correcto del sistema grid
- Implementación de componentes avanzados
- Diseño responsive
- Personalización del framework
- Optimización del código
- Documentación del proyecto