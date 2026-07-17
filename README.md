# Portal AEGIS – Instancia IDEXUD

> Demo del Portal de Servicios AEGIS adaptado para **IDEXUD – Universidad Distrital Francisco José de Caldas**

---

## Estructura del repositorio

```
portal-aegis-idexud-demo/
├── index.html       ← Portal completo (React + Firebase + Make)
└── README.md        ← Este archivo
```

---

## Estado actual

| Item | Estado |
|------|--------|
| HTML base desde Sandor v2.18.0 | ✅ Listo |
| Branding IDEXUD completo (título, consecutivos, datos demo) | ✅ Aplicado |
| Firebase config | ⏳ Pendiente – reemplazar placeholders |
| Webhook Make | ⏳ Pendiente – reemplazar placeholder |
| GitHub Pages / deploy | ⏳ Pendiente |

---

## Configuración pendiente – Placeholders a reemplazar

Una vez tengas el proyecto Firebase de IDEXUD creado y el escenario Make clonado,
busca y reemplaza en `index.html` los siguientes valores:

### 1. Firebase Config

```js
// BUSCAR y REEMPLAZAR en index.html:
apiKey: "IDEXUD_FIREBASE_API_KEY"
authDomain: "IDEXUD_AUTH_DOMAIN"
projectId: "IDEXUD_PROJECT_ID"
storageBucket: "IDEXUD_STORAGE_BUCKET"
messagingSenderId: "IDEXUD_MESSAGING_SENDER_ID"
appId: "IDEXUD_APP_ID"
```

**Dónde obtenerlo:** Firebase Console → Proyecto IDEXUD → Configuración → Tu app web → `firebaseConfig`

### 2. Webhook Make

```js
// BUSCAR en index.html:
const WEBHOOK_URL = "IDEXUD_MAKE_WEBHOOK_URL_PLACEHOLDER";

// REEMPLAZAR por la URL del webhook del escenario clonado en Make:
const WEBHOOK_URL = "https://hook.us2.make.com/TU_WEBHOOK_IDEXUD";
```

**Dónde obtenerlo:** Make → Escenario clonado IDEXUD → Módulo Webhook → Copiar URL

---

## Zonas de branding en index.html

| Qué cambiar | Dónde buscarlo en el código | Valor actual |
|-------------|----------------------------|--------------|
| Título del portal | `<title>` línea 6 | `Portal de Servicios - IDEXUD` |
| Prefijo consecutivos | `generarConsecutivoLocal()` | `IDEXUD-COT-` |
| Nombre cliente en normalizador | `unificarNombreEmpresa()` | `IDEXUD - U. DISTRITAL` |
| Nombre en Centro de Ayuda | sección `soporte` | `Portal IDEXUD` |
| PIN de acceso Director | constante `MASTER_PIN` | `2025` (cambiar en producción) | | Email director CC | `IDEXUD_EMAIL_DIRECTOR_PLACEHOLDER` | Email director IDEXUD | | Email asesor CC | `IDEXUD_EMAIL_ASESOR_PLACEHOLDER` | Email asesor IDEXUD |

---

## Flujo de activación para nueva instancia (checklist)

- [ ] Crear proyecto Firebase con nombre `aegis-idexud` o similar
- [ ] Registrar Web App en Firebase Console
- [ ] Activar Firestore (modo producción)
- [ ] Activar Authentication (correo/contraseña o anónimo)
- [ ] Reemplazar los 6 placeholders de `firebaseConfig` en `index.html`
- [ ] Clonar escenario Make desde Sandor
- [ ] Obtener URL webhook del escenario clonado
- [ ] Reemplazar `IDEXUD_MAKE_WEBHOOK_URL_PLACEHOLDER` en `index.html`
- [ ] Activar GitHub Pages (`Settings → Pages → Deploy from branch: main`)
- [ ] Probar flujo completo: cotización → webhook → Firestore
- [ ] Cambiar `MASTER_PIN` por valor seguro para IDEXUD

---

## Base técnica

- **Versión base:** Portal AEGIS v2.18.0 (desde `portal-aegis-sandor`)
- **Stack:** React 18.3 (CDN) + Firebase 10.8 + Make (Integromat) + Tailwind CSS 3.4
- **Generador PDF:** html2pdf.js 0.10
- **Deploy target:** GitHub Pages

---

*Proyecto AEGIS Insurance – Consultoría técnica*
