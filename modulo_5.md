## Módulo 5: Componentes Interactivos

### 5.1 Modal
```html
<!-- Botón para abrir el modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
    Abrir modal
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Título del Modal</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                Contenido del modal
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cerrar</button>
                <button type="button" class="btn btn-primary">Guardar cambios</button>
            </div>
        </div>
    </div>
</div>
```

### 5.2 Carrusel
```html
<div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
                <div class="carousel-item active">
                    <img src="https://placehold.co/600x400?text=Hello+World" class="d-block w-100" alt="...">
                </div>
                <div class="carousel-item">
                    <img src="https://placehold.co/600x400?text=Hola+Mundo" class="d-block w-100" alt="...">
                </div>
                <div class="carousel-item">
                    <img src="https://placehold.co/600x400?text=Bonjour+le+Monde" class="d-block w-100" alt="...">
                </div>
            </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
        <span class="carousel-control-prev-icon"></span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
        <span class="carousel-control-next-icon"></span>
    </button>
</div>
```