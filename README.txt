NEXO (celular) - Actualizacion
==============================

Archivos actualizados (reemplaza los existentes en tu repo de GitHub):
- app.js        (cambios principales: integracion PC completa)
- index.html     (boton "PC: probar conexion" en el menu)

El resto de archivos (manifest.json, style.css, sw.js, iconos) no cambiaron.

Cambios en app.js:
- Conexion directa con la PC via puente pc_bridge.js (http://IP_PC:8766).
- Herramientas nuevas para NEXO (pc_*):
  Volumen: pc_volumen
  Archivos: pc_listar, pc_archivo, pc_descargar_carpeta, pc_subir
  Apps/web: pc_abrir_url, pc_abrir_app, pc_buscar
  Info: pc_info
  OpenCode: pc_opencode, pc_sesiones_opencode
  Portapapeles: pc_portapapeles_leer, pc_portapapeles_escribir
  Pantalla: pc_screenshot
  Media: pc_media (play/pause/siguiente/anterior)
  Voz PC: pc_tts
  Procesos: pc_procesos, pc_matar
  Ventanas: pc_ventanas, pc_ventana
  Busqueda: pc_buscar_archivos
  Brillo: pc_brillo
  Notificaciones: pc_notificaciones
  Terminal: pc_terminal
  Wake-on-LAN: pc_wol
  Backup: pc_backup
  Estado: pc_estado

Configuracion:
- IP de la PC y token en app.js (variables PC_URL y PC_TOKEN) o via localStorage:
  ls("nexo_pc_url", "http://192.168.40.25:8766")
  ls("nexo_pc_token", "nexo-pc-2026")
- El puente pc_bridge.js debe estar corriendo en la PC (ver carpeta AURA).

Notas:
- NEXO corre en el celular (PWA). La PC debe estar en la misma red WiFi.
- El puente usa token para seguridad; no expongas el puerto a internet.