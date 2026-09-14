<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Acceso al Sistema Contable</title>
  <style>
    :root {
      --primary: #2c3e50;
      --accent: #16a085;
      --bg: #f5f6fa;
      --border: #dcdde1;
      --danger: #d93025;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--bg);
      margin: 0;
      padding: 30px 20px;
      color: #333;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      box-sizing: border-box;
    }
    .login-card {
      width: 100%;
      max-width: 400px;
      background: white;
      padding: 35px 30px;
      border-radius: 10px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.08);
      box-sizing: border-box;
      text-align: center;
    }
    h2#nombreEmpresa {
      color: var(--primary);
      margin: 0 0 20px 0;
      font-size: 20px;
    }
    .logo-container img {
      width: 110px;
      height: auto;
      display: inline-block;
    }
    .fecha-sistema {
      font-weight: 700;
      color: var(--primary);
      margin: 10px 0 25px 0;
      font-size: 16px;
      letter-spacing: 0.5px;
    }
    .form-group {
      text-align: left;
      margin-bottom: 18px;
    }
    .form-group label {
      display: block;
      font-weight: 600;
      font-size: 14px;
      margin-bottom: 6px;
      color: var(--primary);
    }
    .form-group input {
      width: 100%;
      padding: 10px 12px;
      border: 1px solid var(--border);
      border-radius: 4px;
      font-size: 14px;
      box-sizing: border-box;
    }
    .form-group input:focus {
      outline: none;
      border-color: var(--accent);
    }
    .btn-ingresar {
      width: 100%;
      background-color: var(--accent);
      color: white;
      border: none;
      padding: 12px;
      border-radius: 4px;
      font-size: 15px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.2s;
      margin-top: 5px;
    }
    .btn-ingresar:hover { background-color: #117a65; }
    .btn-ingresar:disabled { opacity: 0.6; cursor: not-allowed; }

    .link-olvido {
      display: inline-block;
      margin-top: 18px;
      font-size: 13px;
      color: #1a73e8;
      cursor: pointer;
      text-decoration: underline;
      background: none;
      border: none;
    }
    .mensaje-error {
      display: none;
      background: #fce8e6;
      color: var(--danger);
      border: 1px solid #f5c2be;
      border-radius: 4px;
      padding: 10px;
      font-size: 13px;
      margin-bottom: 15px;
    }
    .mensaje-info {
      display: none;
      background: #e8f0fe;
      color: #1a73e8;
      border: 1px solid #aecbfa;
      border-radius: 4px;
      padding: 10px;
      font-size: 13px;
      margin-bottom: 15px;
    }

    /* === Pie de página centrado de Surtecol === */
    .surtecol-footer {
      width: 100%;
      max-width: 400px;
      text-align: center;
      margin-top: 20px;
      padding: 10px 0;
      box-sizing: border-box;
      position: absolute;
      bottom: 15px;
      left: 50%;
      transform: translateX(-50%);
    }
    .surtecol-footer p { margin: 4px 0; color: #000000; font-size: 12px; }
    .surtecol-footer p.marca { font-size: 13px; }
  </style>
</head>
<body>

<div class="login-card">
  <h2 id="nombreEmpresa">Cargando...</h2>

  <div class="logo-container">
    <img src="logo1.png?v=2" alt="Logo" onerror="this.src='logo1.PNG?v=2'">
  </div>
  <div class="fecha-sistema" id="fechaSistema">--/--/----</div>

  <div class="mensaje-error" id="mensajeError"></div>
  <div class="mensaje-info" id="mensajeInfo"></div>

  <form id="formLogin">
    <div class="form-group">
      <label for="usuario">Usuario</label>
      <input type="text" id="usuario" autocomplete="username" required>
    </div>
    <div class="form-group">
      <label for="clave">Clave</label>
      <input type="password" id="clave" autocomplete="current-password" required>
    </div>
    <button type="submit" class="btn-ingresar" id="btnIngresar">Ingresar</button>
  </form>

  <button type="button" class="link-olvido" onclick="solicitarRecuperacion()">¿Olvidó su clave?</button>
</div>

<div class="surtecol-footer">
  <p class="marca">Este es un desarrollo creado por <strong style="text-decoration: underline;">Surtecol</strong></p>
  <p><strong>Tel.: +573188097131 &nbsp;|&nbsp; email: surtecol@gmail.com &nbsp;|&nbsp; Colombia</strong></p>
</div>

<script>
  // Mismo Web App usado por el resto del sistema (index.html, fcompra.html, productos.html, etc.)
  const WEB_APP_URL = "https://script.google.com/macros/s/AKfycbzpYG9qByjvcK06ShRLpS9QnLEvQyYnO4OmeilNl6JGT1-U24P27gGRtgKgtPjT0hKv/exec";

  document.addEventListener("DOMContentLoaded", cargarDatosPublicos);

  function cargarDatosPublicos() {
    fetch(`${WEB_APP_URL}?action=getDatosPublicos`)
      .then(res => res.json())
      .then(res => {
        if (res.success) {
          document.getElementById("nombreEmpresa").textContent = res.data.nombreEmpresa || "Sistema Contable";
          document.getElementById("fechaSistema").textContent = formatearFecha(res.data.fecha);
        } else {
          document.getElementById("nombreEmpresa").textContent = "Sistema Contable";
        }
      })
      .catch(() => {
        document.getElementById("nombreEmpresa").textContent = "Sistema Contable";
      });
  }

  function formatearFecha(valor) {
    if (!valor) return "";
    // El valor puede llegar como texto ya formateado o como fecha ISO desde Apps Script
    const posibleFecha = new Date(valor);
    if (!isNaN(posibleFecha.getTime()) && valor.toString().indexOf('/') === -1) {
      const dia = String(posibleFecha.getDate()).padStart(2, '0');
      const mes = String(posibleFecha.getMonth() + 1).padStart(2, '0');
      const anio = posibleFecha.getFullYear();
      return `${dia}/${mes}/${anio}`;
    }
    return valor.toString();
  }

  document.getElementById("formLogin").addEventListener("submit", function(e) {
    e.preventDefault();
    ocultarMensajes();

    const usuario = document.getElementById("usuario").value.trim();
    const clave = document.getElementById("clave").value.trim();

    if (!usuario || !clave) {
      return mostrarError("Por favor ingresa el usuario y la clave.");
    }

    const btn = document.getElementById("btnIngresar");
    btn.disabled = true;
    btn.textContent = "Verificando...";

    fetch(WEB_APP_URL, {
      method: "POST",
      body: JSON.stringify({
        action: "validarAcceso",
        data: { usuario: usuario, clave: clave }
      })
    })
    .then(res => res.json())
    .then(res => {
      if (res.success && res.result.valido) {
        // Marca de sesión válida en este navegador para que menu.html permita el ingreso
        sessionStorage.setItem("accesoValido", "true");
        sessionStorage.setItem("nombreEmpresa", res.result.nombreEmpresa || "");
        window.location.href = "menu.html";
      } else if (res.success && !res.result.valido) {
        mostrarError("Usuario o clave incorrectos. Verifica tus datos e intenta nuevamente.");
      } else {
        mostrarError("Error: " + (res.error || "No se pudo validar el acceso."));
      }
    })
    .catch(err => {
      console.error(err);
      mostrarError("Error de red al validar el acceso.");
    })
    .finally(() => {
      btn.disabled = false;
      btn.textContent = "Ingresar";
    });
  });

  function solicitarRecuperacion() {
    if (!confirm("Se enviará un correo con el paso a paso para restablecer la clave al correo administrativo registrado. ¿Deseas continuar?")) {
      return;
    }

    ocultarMensajes();
    const linkOlvido = document.querySelector(".link-olvido");
    linkOlvido.disabled = true;
    linkOlvido.textContent = "Enviando correo...";

    fetch(WEB_APP_URL, {
      method: "POST",
      body: JSON.stringify({ action: "solicitarRecuperacionClave" })
    })
    .then(res => res.json())
    .then(res => {
      if (res.success) {
        mostrarInfo(res.result);
      } else {
        mostrarError("Error: " + res.error);
      }
    })
    .catch(err => {
      console.error(err);
      mostrarError("Error de red al solicitar la recuperación de clave.");
    })
    .finally(() => {
      linkOlvido.disabled = false;
      linkOlvido.textContent = "¿Olvidó su clave?";
    });
  }

  function mostrarError(texto) {
    const el = document.getElementById("mensajeError");
    el.textContent = texto;
    el.style.display = "block";
  }
  function mostrarInfo(texto) {
    const el = document.getElementById("mensajeInfo");
    el.textContent = texto;
    el.style.display = "block";
  }
  function ocultarMensajes() {
    document.getElementById("mensajeError").style.display = "none";
    document.getElementById("mensajeInfo").style.display = "none";
  }
</script>
</body>
</html>
