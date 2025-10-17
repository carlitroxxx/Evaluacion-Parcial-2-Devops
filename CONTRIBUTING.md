# Guía de contribución al proyecto

A continuación se explican las reglas y buenas prácticas para mantener un flujo de trabajo limpio y ordenado.

---

## Reglas de commits

Sigue el formato estándar:
```
<tipo>(<área>): <descripción breve>
```

**Tipos comunes:**
- `feat` → nueva funcionalidad
- `fix` → corrección
- `docs` → documentación
- `style` → formato/código
- `test` → pruebas

---

## Estilo de código

- Usa **ESLint** para mantener consistencia en el código (`npx eslint .`).
- Asegúrate de que no haya errores antes de hacer commit.
- El código debe estar **testeado** antes de enviarse a `develop`.

---

## Testing

Antes de enviar cambios:
```bash
npm test
```
Los tests deben ejecutarse correctamente antes de hacer el **Pull Request**.

---

## Pull Requests

1. Crea tu rama desde `develop`.
2. Realiza tus cambios y confirma que pasan los tests.
3. Abre un **Pull Request** hacia `develop`.

---

## Revisión de calidad

El proyecto utiliza:
- **Snyk** → escaneo de vulnerabilidades.
- **SonarCloud** → revisión de calidad de código.
- **GitHub Actions** → ejecución automática del pipeline.

---

## Docker y CI/CD

- La imagen se construye automáticamente mediante el workflow de GitHub Actions.  
- No es necesario construir manualmente la imagen localmente.

