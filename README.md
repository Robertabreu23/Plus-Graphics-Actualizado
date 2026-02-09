# Plus Graphics - Sistema de Gestión Empresarial

**Sistema integral de gestión para Plus Graphics** - Empresa especializada en servicios GFX (Graphics) y VFX (Visual Effects).
Hecho por Robert Abreu y Jose Rodriguez.
## 🚀 Características Principales

- ✅ **Dashboard Principal** con estadísticas en tiempo real
- ✅ **Gestión de Clientes** con detalles completos y historial
- ✅ **Catálogo de Productos/Servicios** (GFX y VFX) con edición completa
- ✅ **Sistema de Pedidos** con seguimiento de estados
- ✅ **Punto de Venta** integrado
- ✅ **Cuentas por Pagar/Cobrar** con códigos automáticos
- ✅ **Sistema de Reportes** con exportación a Excel
- ✅ **Base de datos SQLite** con relaciones completas

## 📋 Stack Tecnológico

**Frontend:**
- Next.js 14 + TypeScript
- Tailwind CSS + shadcn/ui
- Lucide Icons

**Backend:**
- Python Flask
- SQLite Database
- Flask-CORS habilitado

## 🛠️ Instalación Local

### Requisitos Previos
- Python 3.11+
- Node.js 18+
- npm o pnpm

### 1. Clonar e Instalar Backend

```bash
# Instalar dependencias Python
pip install -r requirements-clean.txt

# Inicializar base de datos
python models.py
```

### 2. Instalar Frontend

```bash
cd fronted-vo
npm install
```

## 🚀 Ejecutar en Desarrollo

### Terminal 1: Backend (Ejecutar PRIMERO)
```bash
# Activar entorno virtual si existe
venv\Scripts\activate  # Windows
# o
source venv/bin/activate  # Linux/Mac

# Ejecutar servidor Flask
python app.py
```
**✅ Backend:** http://localhost:5000

### Terminal 2: Frontend
```bash
cd fronted-vo
npm run dev
```
**✅ Frontend:** http://localhost:3000

## 🌐 Deployment en Producción

### Opción 1: Railway (Recomendado)

Railway es ideal para aplicaciones fullstack Python + Node.js.

1. **Crear cuenta en [Railway](https://railway.app)**

2. **Conectar repositorio de GitHub:**
   - Fork este repositorio
   - Conecta tu repositorio en Railway

3. **Configurar variables de entorno:**
   ```
   FLASK_ENV=production
   PORT=5000
   ```

4. **Deploy automático:** Railway detectará el `railway.json` y desplegará automáticamente.

### Opción 2: Render

1. **Crear cuenta en [Render](https://render.com)**

2. **Deploy Backend (Web Service):**
   - Repository: Tu fork del proyecto
   - Build Command: `pip install -r requirements-clean.txt`
   - Start Command: `python app.py`
   - Environment: `FLASK_ENV=production, PORT=5000`

3. **Deploy Frontend (Static Site):**
   - Root Directory: `fronted-vo`
   - Build Command: `npm install && npm run build`
   - Publish Directory: `out`

### Opción 3: Docker

```bash
# Construir imagen
docker build -t plusgraphics .

# Ejecutar contenedor
docker run -p 5000:5000 plusgraphics
```

## 📱 Acceso al Sistema

### Usuarios de Prueba (Seedeados)

**Administrador:**
- **Email:** admin@plusgraphics.com
**Empleados:**
- vex@plusgraphics.com
- gilbert@plusgraphics.com  
- randy@plusgraphics.com
- sergio@plusgraphics.com
- hiroshi@plusgraphics.com
- rene@plusgraphics.com

## 🎯 Funcionalidades Completadas

### ✅ Módulos Funcionales al 100%

| Módulo | Funcionalidad | Estado |
|--------|---------------|---------|
| **Dashboard** | Estadísticas reales en tiempo real | ✅ Completo |
| **Clientes** | CRUD + Modal de detalles con historial | ✅ Completo |
| **Productos** | CRUD + Modal de edición pre-llenado | ✅ Completo |
| **Pedidos** | Gestión completa de pedidos | ✅ Completo |
| **Ventas** | Punto de venta funcional | ✅ Completo |
| **Cuentas por Pagar** | Códigos automáticos BILL001, BILL002 | ✅ Completo |
| **Cuentas por Cobrar** | Códigos automáticos FAC-0001, FAC-0002 | ✅ Completo |
| **Reportes** | Sistema completo con exportación Excel | ✅ Completo |

### 🔧 Últimos Retoques Implementados

- **✅ Botón Editar Productos:** Modal de edición con formulario pre-llenado
- **✅ Botón Ver Detalles Clientes:** Modal con información completa e historial de pedidos
- **✅ API Cliente Individual:** Endpoint GET /api/clientes/<id> funcional
- **✅ Configuraciones de Deploy:** Railway, Render, Docker listos

## 📊 Base de Datos

### Estructura SQLite
- **Usuarios** - Sistema de autenticación
- **Clientes** - Información de clientes
- **Productos** - Catálogo GFX/VFX
- **Pedidos** - Gestión de pedidos
- **Pedido_Productos** - Relación productos-pedidos
- **Ventas** - Registro de ventas
- **Cuentas_por_Cobrar** - Facturación automática
- **Cuentas_por_Pagar** - Gestión de gastos

### IDs y Secuencias
- ✅ **Secuencias reseteadas** para clientes, pedidos, ventas, cuentas
- ✅ **Productos mantienen secuencia** (datos de producción)
- ✅ **Códigos automáticos** para facturas y bills

## 🔒 Seguridad y Producción

### Variables de Entorno Requeridas
```env
FLASK_ENV=production
FLASK_DEBUG=False
PORT=5000
DATABASE_URL=sqlite:///database.db
SECRET_KEY=tu-clave-secreta-aqui
```

### Configuraciones de Seguridad
- CORS configurado para múltiples dominios
- Validaciones de entrada en todos los endpoints
- Manejo seguro de errores
- Base de datos con validaciones

## 📞 Soporte y Contacto

### Empresa
- **Nombre:** Plus Graphics
- **Industria:** Servicios GFX y VFX
- **Sistema:** Gestión empresarial integral

### Soporte Técnico
Para soporte técnico o consultas sobre deployment, contactar al desarrollador del sistema.

## 🗃️ Archivos de Configuración

- **railway.json** - Configuración para Railway
- **render.yaml** - Configuración para Render  
- **Dockerfile** - Contenedor Docker
- **requirements-clean.txt** - Dependencias Python limpias
- **.env.example** - Variables de entorno ejemplo

## 🎉 Sistema Listo para Producción

**Estado:** ✅ **100% Funcional y listo para deploy**

El sistema Plus Graphics está completamente terminado con todas las funcionalidades implementadas, retoques finales aplicados y configuraciones de deployment preparadas. Listo para presentar al cliente y poner en producción.

---
<img width="1599" height="814" alt="image" src="https://github.com/user-attachments/assets/f901aed2-5e1f-4337-93a6-dc46dd2fc669" />

*Desarrollado con ❤️ para Plus Graphics*  
*Última actualización: 2025-08-09*
