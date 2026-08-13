# Tienda de Midu — Web

## Bases del proyecto
Ver: `D:\midu\bases\AGENTS.md`

## Recursos compartidos
- Excel canonical: `D:\midu\bases\Catálogo.xlsx`
- Imágenes producto: `D:\midu\bases\productos\producto-XX\img_XX.*`
- Script principal: `D:\midu\bases\scripts\generar_catalogo_web.py`

## Este repo
Catálogo web estático generado desde Excel. Sin backend.

## Catálogo
- Archivo: `catalogo.html` (generado automáticamente)
- Columnas de control en Excel:
  - `Disponible` (true/false) - si false, producto no aparece
  - `Destacado` (true/false) - si true, aparece primero con borde rojo
  - `Remate (S/)` - si tiene valor, muestra precio tachado + precio remate

## Flujo de actualización
```
1. Editar Excel en D:\midu\bases\Catálogo.xlsx
2. python D:\midu\bases\scripts\generar_catalogo_web.py
3. Verificar catalogo.html en navegador
4. Commit y push (cuando haya hosting)
```

## Convenciones
- HTML estático, sin frameworks
- Python 3 + openpyxl para generación
- Precios en Soles (S/), idioma español (Perú)

## No hacer
- No frameworks JS/React/Next
- No backend
- No editar `productos.csv` (derivado legacy en `D:\midu\bases\`)
