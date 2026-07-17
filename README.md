# Portal AEGIS – Instancia IDEXUD

> Demo del Portal de Servicios AEGIS adaptado para **IDEXUD – Universidad Distrital Francisco José de Caldas**

---

## Estructura del repositorio

```
portal-aegis-idexud-demo/
├── index.html    → Portal completo (React + Firebase + Make)
└── README.md     → Este archivo
```

---

## Estado actual

| Item | Estado |
|------|--------|
| HTML base desde Sandor v2.18.0 | ✅ Listo |
| Branding IDEXUD completo (título, consecutivos, datos demo) | ✅ Aplicado |
| Firebase config | ✅ Configurado – portal-idexud-prod |
| Webhook Make | ✅ Configurado – hook.us2.make.com/sh9iqa5... |
| GitHub Pages / deploy | ✅ Live – https://proyectosaegis.github.io/portal-aegis-idexud-demo/ |

---

## URL del Portal

**https://proyectosaegis.github.io/portal-aegis-idexud-demo/**

---

## Stack técnico

- **Frontend:** React 18 (CDN/UMD) + Babel Standalone
- **Estilos:** Tailwind CSS 3.4
- **Backend:** Firebase Firestore (`portal-idexud-prod`)
- **Automatización:** Make.com (webhook configurado)
- **PDF:** html2pdf.js
- **Deploy:** GitHub Pages (rama `main`, raíz `/`)
