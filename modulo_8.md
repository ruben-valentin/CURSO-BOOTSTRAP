## Módulo 8: Personalización y Temas

### 8.1 Personalización con CSS personalizado
```css
/* Sobrescribir variables de Bootstrap */
:root {
    --bs-primary: #your-color;
    --bs-secondary: #your-color;
    --bs-font-sans-serif: your-font-family;
}

/* Personalizar componentes */
.btn-primary {
    background-color: var(--bs-primary);
    border-color: var(--bs-primary);
}

/* Agregar nuevas utilidades */
.custom-class {
    /* tus estilos */
}
```

## Proyecto Final

### Estructura sugerida para el proyecto final
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proyecto Final Bootstrap 5</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="css/custom.css" rel="stylesheet">
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <!-- ... -->
    </nav>

    <!-- Hero Section -->
    <header class="bg-primary text-white py-5">
        <div class="container">
            <!-- ... -->
        </div>
    </header>

    <!-- Main Content -->
    <main class="container my-5">
        <!-- ... -->
    </main>

    <!-- Footer -->
    <footer class="bg-dark text-white py-4">
        <div class="container">
            <!-- ... -->
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="js/custom.js"></script>
</body>
</html>
```

## Recursos Adicionales

### Enlaces útiles
- Documentación oficial: [https://getbootstrap.com/docs/5.3/](https://getbootstrap.com/docs/5.3/)
- Bootstrap Icons: [https://icons.getbootstrap.com/](https://icons.getbootstrap.com/)
- Bootstrap Examples: [https://getbootstrap.com/docs/5.3/examples/](https://getbootstrap.com/docs/5.3/examples/)

### Mejores prácticas
1. Utilizar la estructura de contenedor apropiada
2. Aprovechar las utilidades integradas
3. Mantener el HTML limpio y semántico
4. Optimizar para producción
5. Seguir las convenciones de nomenclatura de Bootstrap
6. Documentar las personalizaciones
7. Mantener la consistencia en el diseño
8. Probar en múltiples dispositivos y navegadores