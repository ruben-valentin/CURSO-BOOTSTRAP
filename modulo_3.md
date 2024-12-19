## Módulo 3: Componentes Básicos

### 3.1 Tipografía

#### Encabezados
```html
<h1>Encabezado h1</h1>
<h2>Encabezado h2</h2>
<h3>Encabezado h3</h3>
<h4>Encabezado h4</h4>
<h5>Encabezado h5</h5>
<h6>Encabezado h6</h6>

<h1 class="display-1">Display 1</h1>
<h1 class="display-2">Display 2</h1>
<h1 class="display-3">Display 3</h1>
<h1 class="display-4">Display 4</h1>
<h1 class="display-5">Display 5</h1>
<h1 class="display-6">Display 6</h1>

```

#### Clases de texto
```html
<p class="lead">Texto destacado</p>
<p class="text-primary">Texto con color primario</p>
<p class="text-secondary">Texto secundario</p>
<p class="fw-bold">Texto en negrita</p>
<p class="fst-italic">Texto en cursiva</p>
```

### 3.2 Botones

#### Tipos de botones
```html
<button class="btn btn-primary">Primario</button>
<button class="btn btn-secondary">Secundario</button>
<button class="btn btn-success">Éxito</button>
<button class="btn btn-danger">Peligro</button>
<button class="btn btn-warning">Advertencia</button>
<button class="btn btn-info">Información</button>
```

#### Tamaños de botones
```html
<button class="btn btn-primary btn-lg">Botón grande</button>
<button class="btn btn-primary">Botón normal</button>
<button class="btn btn-primary btn-sm">Botón pequeño</button>
```

### 3.3 Formularios

#### Formulario básico
```html
<form>
    <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <input type="email" class="form-control" id="email">
    </div>
    <div class="mb-3">
        <label for="password" class="form-label">Contraseña</label>
        <input type="password" class="form-control" id="password">
    </div>
    <div class="mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="remember">
        <label class="form-check-label" for="remember">Recordarme</label>
    </div>
    <button type="submit" class="btn btn-primary">Enviar</button>
</form>
```