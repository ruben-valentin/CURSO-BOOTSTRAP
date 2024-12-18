## Módulo 2: Fundamentos del Sistema Grid

### 2.1 Sistema Grid

El sistema grid de Bootstrap 5 está basado en un layout de 12 columnas usando Flexbox, diseñado para ser responsive y móvil primero.

#### Contenedores
```html
<!-- Contenedor con máximo ancho fijo según breakpoint -->
<div class="container">
    <!-- Contenido -->
</div>

<!-- Contenedor que ocupa todo el ancho disponible -->
<div class="container-fluid">
    <!-- Contenido -->
</div>
```

#### Sistema de filas y columnas
```html
<div class="container">
    <div class="row">
        <div class="col-12 col-md-6 col-lg-4">
            Columna 1
        </div>
        <div class="col-12 col-md-6 col-lg-4">
            Columna 2
        </div>
        <div class="col-12 col-md-6 col-lg-4">
            Columna 3
        </div>
    </div>
</div>
```

#### Breakpoints responsive
- xs (< 576px)
- sm (≥ 576px)
- md (≥ 768px)
- lg (≥ 992px)
- xl (≥ 1200px)
- xxl (≥ 1400px)