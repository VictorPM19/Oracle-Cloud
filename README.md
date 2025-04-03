# 📌 Guía para Crear una Cuenta en Oracle Cloud y Lanzar una Instancia Gratuita para Estudiantes

## 1️⃣ Crear una Cuenta en Oracle Cloud

### 🔹 Paso 1: Ir al sitio web de Oracle Cloud
1. Abre tu navegador y visita:  
   [🔗 Oracle Cloud Free Tier](https://www.oracle.com/cloud/free/)
2. Haz clic en **"Sign Up" (Registrarse)** o **"Try Oracle Cloud Free Tier"**.

### 🔹 Paso 2: Rellenar el formulario de registro
1. **Correo electrónico:** Usa un correo válido para recibir un código de verificación.  
2. **País:** Selecciona tu país de residencia.  
3. **Tipo de cuenta:** Si eres estudiante, revisa si hay una opción especial para estudiantes.  
4. **Contraseña:** Debe cumplir con los requisitos de seguridad de Oracle.

### 🔹 Paso 3: Verificación de identidad y pago
1. Recibirás un código de verificación en tu correo electrónico.  
2. **Verificación de pago:** Oracle pide una tarjeta de crédito/débito, pero NO te cobrará nada a menos que hagas un upgrade.  
3. Completa la información y finaliza el registro.

### 🔹 Paso 4: Confirmación y acceso a la consola
- Una vez aprobado tu registro, recibirás un correo de confirmación.  
- Inicia sesión en **Oracle Cloud Console** desde:  
  [🔗 https://cloud.oracle.com/](https://cloud.oracle.com/).

---

## 2️⃣ Crear una Instancia Gratuita (VM)

### 🔹 Paso 1: Acceder al Dashboard
1. Inicia sesión en **Oracle Cloud Console**.  
2. En el menú de la izquierda, ve a **Compute → Instances**.

### 🔹 Paso 2: Crear una nueva instancia
1. **Haz clic en "Create Instance"**.  
2. **Asigna un nombre** (Ejemplo: "MiServidor").  
3. **Selecciona la configuración gratuita:**  
   - **Shape:** Elige **"VM.Standard.E2.1.Micro"**, que es parte del Free Tier.  
   - **Imagen del SO:** Puedes elegir **Oracle Linux**, **Ubuntu**, **CentOS**, etc.  
4. **Configurar red:** Deja las opciones predeterminadas.

### 🔹 Paso 3: Configurar acceso SSH
1. **Genera un par de claves SSH** si aún no tienes uno:  
   - En Windows: Usa **PuTTYgen** o **Git Bash** con:  
     ```sh
     ssh-keygen -t rsa -b 2048
     ```
   - En Linux/macOS:  
     ```sh
     ssh-keygen -t rsa -b 2048 -f ~/.ssh/oracle_key
     ```
2. **Carga la clave pública en Oracle Cloud** cuando te lo pida.  
3. Guarda la clave privada en tu PC para conectarte más tarde.

### 🔹 Paso 4: Crear la instancia
1. **Haz clic en "Create"**.  
2. Espera unos minutos hasta que el estado cambie a **"Running"**.

---

## 3️⃣ Conectar a la Instancia (SSH)

### 🔹 Desde Linux/macOS:
```sh
ssh -i ~/.ssh/oracle_key opc@<IP-de-tu-VM>
