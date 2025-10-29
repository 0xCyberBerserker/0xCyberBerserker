# Investigación: n8n-nodes-linked-api

## 📋 Resumen

**n8n-nodes-linked-api** es un paquete de nodo comunitario para n8n que integra LinkedIn con la plataforma de automatización n8n mediante la API de Linked API. Permite automatizar tareas de LinkedIn como búsqueda de prospectos, envío de mensajes, gestión de conexiones, extracción de datos y más.

- **Paquete NPM**: `n8n-nodes-linked-api`
- **Versión actual**: 0.0.11
- **Licencia**: MIT
- **Sitio web**: https://linkedapi.io
- **Repositorio**: https://github.com/Linked-API/n8n-nodes-linked-api

---

## 🔧 Instalación

### Método 1: Instalación mediante la interfaz de n8n (Recomendado)

1. Abre tu instancia de n8n
2. Ve a **Settings** (Configuración) → **Community Nodes** (Nodos Comunitarios)
3. Ingresa: `n8n-nodes-linked-api`
4. Haz clic en **Install** (Instalar)
5. Espera a que se complete la instalación
6. Reinicia n8n si es necesario

### Método 2: Instalación manual (Self-hosted)

Si tienes n8n instalado localmente mediante npm:

```bash
cd ~/.n8n
npm install n8n-nodes-linked-api
```

Si usas Docker:

```bash
docker exec -it <n8n-container-name> sh
cd /home/node/.n8n
npm install n8n-nodes-linked-api
exit
docker restart <n8n-container-name>
```

---

## 🔑 Configuración de Credenciales

### Paso 1: Obtener API Token de Linked API

1. Registra una cuenta en [https://linkedapi.io](https://linkedapi.io)
2. Conecta tu cuenta de LinkedIn
3. Obtén tu API Token desde el panel de control
4. Guía detallada: [Creating credential](https://linkedapi.io/integrations/n8n/creating-credential/)

### Paso 2: Configurar credenciales en n8n

1. En n8n, ve a **Credentials** → **New**
2. Busca "Linked API"
3. Ingresa tu **API Token**
4. Guarda las credenciales
5. Prueba la conexión

---

## 💡 Casos de Uso

### 1. **Pipeline de Generación de Leads**
Busca prospectos según criterios específicos, envía solicitudes de conexión automáticamente, espera la aceptación y luego envía mensajes de seguimiento personalizados. Conecta los resultados a tu CRM para rastrear todo en un solo lugar.

**Workflow ejemplo:**
```
Trigger (Cron) → Linked API (Search Prospects) → Filter → Linked API (Send Connection Request) → Delay → Linked API (Send Message) → CRM (Update)
```

### 2. **Sincronización con CRM**
Cuando un nuevo lead entra en tu CRM, encuentra automáticamente su perfil de LinkedIn, envía una solicitud de conexión y actualiza el CRM con sus datos de LinkedIn.

**Workflow ejemplo:**
```
CRM Trigger (New Lead) → Linked API (Find Profile) → Linked API (Send Connection) → CRM (Update Lead)
```

### 3. **Engagement de Contenido**
Monitorea cuando tus cuentas objetivo publican en LinkedIn, reacciona o comenta automáticamente en sus publicaciones, y registra el engagement en tu hoja de cálculo.

**Workflow ejemplo:**
```
Trigger (Schedule) → Linked API (Monitor Posts) → Linked API (React/Comment) → Google Sheets (Log)
```

### 4. **Workflows de Reclutamiento**
Busca candidatos con habilidades específicas, envía InMails personalizados a través de Sales Navigator, rastrea respuestas en tu ATS y haz seguimiento automático con candidatos interesados.

**Workflow ejemplo:**
```
Trigger → Linked API (Search Candidates) → Linked API (Send InMail) → ATS (Create Entry) → Linked API (Follow-up)
```

### 5. **Outreach Multicanal**
Combina LinkedIn con email, Slack y otros canales. Cuando alguien acepta tu solicitud de conexión, activa una secuencia de emails, notifica a tu equipo en Slack y crea una tarea en tu herramienta de gestión de proyectos.

**Workflow ejemplo:**
```
Linked API (Connection Accepted) → SendGrid (Email Sequence) → Slack (Notify Team) → Asana (Create Task)
```

---

## 🎯 Acciones Disponibles

El nodo de Linked API proporciona múltiples acciones para automatizar LinkedIn:

### Gestión de Conexiones
- Enviar solicitudes de conexión
- Aceptar solicitudes pendientes
- Eliminar conexiones
- Listar conexiones existentes

### Mensajería
- Enviar mensajes directos
- Enviar mensajes de seguimiento
- Gestionar conversaciones
- Enviar InMails (con Sales Navigator)

### Búsqueda y Prospección
- Buscar personas por criterios
- Buscar empresas
- Filtrar resultados por ubicación, industria, cargo, etc.
- Exportar datos de perfiles

### Engagement
- Reaccionar a publicaciones
- Comentar en posts
- Compartir contenido
- Seguir perfiles

### Extracción de Datos
- Obtener información de perfil
- Extraer experiencia laboral
- Obtener educación
- Listar habilidades

---

## 📚 Recursos y Documentación

### Guías Oficiales
1. **Crear credenciales**: https://linkedapi.io/integrations/n8n/creating-credential/
2. **Construir workflows**: https://linkedapi.io/integrations/n8n/building-workflows-0/
3. **Acciones disponibles**: https://linkedapi.io/integrations/n8n/available-actions/

### Recursos Adicionales
- **Documentación API**: https://linkedapi.io/docs
- **Seguridad y Límites**: https://linkedapi.io/safety/
- **Soporte**: support@linkedapi.io
- **GitHub Issues**: https://github.com/Linked-API/n8n-nodes-linked-api/issues

---

## ⚠️ Consideraciones Importantes

### Seguridad
- Linked API prioriza la seguridad y cumplimiento con las políticas de LinkedIn
- Implementa rate limiting para evitar detección
- Usa comportamientos similares a humanos para mayor seguridad
- Documentación de seguridad: https://linkedapi.io/safety/

### Límites
- Los límites dependen de tu plan de Linked API
- LinkedIn tiene sus propios límites de solicitudes y mensajes
- Se recomienda usar delays entre acciones para simular comportamiento humano

### Mejores Prácticas
1. **Personalización**: Personaliza siempre tus mensajes para mayor efectividad
2. **Timing**: Usa delays razonables entre acciones (30-60 segundos)
3. **Segmentación**: Filtra bien tus prospectos antes de contactarlos
4. **Testing**: Prueba tus workflows con pocos contactos primero
5. **Monitoreo**: Revisa regularmente los logs y resultados
6. **Compliance**: Respeta las políticas de uso de LinkedIn

---

## 🚀 Ejemplo de Workflow Completo

### Workflow: "Lead Generation con Seguimiento Automático"

**Objetivo**: Buscar prospectos, conectar y enviar mensaje de presentación

```
1. [Schedule Trigger]
   - Ejecutar todos los días a las 10:00 AM
   
2. [Linked API - Search People]
   Credentials: Linked API
   Resource: People
   Operation: Search
   Parameters:
     - Keywords: "Product Manager"
     - Location: "Spain"
     - Company Size: "51-200 employees"
     - Limit: 10
   
3. [Filter]
   Conditions:
     - Has LinkedIn URL
     - Not already in database
   
4. [Linked API - Send Connection Request]
   Credentials: Linked API
   Resource: Connection
   Operation: Send Request
   Parameters:
     - Profile URL: {{ $json.profileUrl }}
     - Message: "Hola {{ $json.firstName }}, me gustaría conectar..."
   
5. [Delay]
   - Wait: 24 hours
   
6. [Linked API - Check Connection Status]
   Credentials: Linked API
   Resource: Connection
   Operation: Get Status
   
7. [IF - Connection Accepted]
   
8. [Linked API - Send Message]
   Credentials: Linked API
   Resource: Message
   Operation: Send
   Parameters:
     - Recipient: {{ $json.profileUrl }}
     - Message: "Gracias por conectar, {{ $json.firstName }}..."
   
9. [Google Sheets - Log]
   - Registrar todos los prospectos contactados
```

---

## 🔍 Verificación de Instalación

Para verificar que el nodo está correctamente instalado:

1. Abre el editor de workflows en n8n
2. Haz clic en el botón "+" para añadir un nuevo nodo
3. Busca "Linked API" en el buscador de nodos
4. Si aparece, la instalación fue exitosa

---

## 🐛 Troubleshooting

### El nodo no aparece después de instalar
- Reinicia completamente n8n
- Verifica que tienes permisos para instalar nodos comunitarios
- Revisa los logs de n8n para errores

### Error de autenticación
- Verifica que tu API Token es correcto
- Asegúrate de que tu cuenta de Linked API está activa
- Revisa que tu cuenta de LinkedIn está conectada en Linked API

### Rate limiting / Demasiadas solicitudes
- Reduce la frecuencia de tus workflows
- Añade delays entre acciones
- Contacta a Linked API para aumentar tus límites

### Los mensajes no se envían
- Verifica que tienes conexión con el prospecto
- Algunos perfiles pueden tener mensajería deshabilitada
- Respeta los límites diarios de LinkedIn

---

## 📊 Comparación con Alternativas

| Característica | n8n-nodes-linked-api | Zapier LinkedIn | PhantomBuster |
|----------------|----------------------|-----------------|---------------|
| Open Source | ✅ Si (n8n) | ❌ No | ❌ No |
| Self-hosted | ✅ Si | ❌ No | ❌ No |
| Precio | Variable | $$ | $$$ |
| Integraciones | 400+ (n8n) | 5000+ | Limitadas |
| Flexibilidad | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| Seguridad | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |

---

## 💬 Conclusión

**n8n-nodes-linked-api** es una herramienta poderosa para automatizar LinkedIn dentro de n8n. Combina la flexibilidad de n8n con las capacidades de LinkedIn, permitiendo crear workflows complejos de:

- ✅ Generación de leads
- ✅ Gestión de relaciones
- ✅ Reclutamiento
- ✅ Sales automation
- ✅ Content engagement

**Ventajas principales:**
- Fácil instalación y configuración
- Seguro y conforme a políticas de LinkedIn
- Múltiples acciones disponibles
- Integración nativa con n8n
- Soporte activo y documentación completa

**Ideal para:**
- Sales teams
- Recruiters
- Marketing teams
- Business developers
- Automatización de procesos

---

## 📝 Notas Adicionales

- Este nodo requiere una cuenta activa de Linked API
- Linked API es un servicio de pago (consulta sus planes en linkedapi.io)
- Siempre respeta las políticas de uso de LinkedIn
- Usa esta herramienta de manera ética y profesional
- Mantén el paquete actualizado para nuevas funcionalidades

---

**Fecha de investigación**: 29 de octubre de 2025  
**Versión del paquete investigado**: 0.0.11  
**Estado**: Activo y mantenido
