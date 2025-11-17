# TxGhost_pub

>[!NOTE]
>TxGhost es 100% modular: cada parte monitor, oráculo, simulador de gas puede funcionar y actualizarse de forma independiente.

TxGhost es un bot modular para monitoreo en tiempo real y oráculos en TRON, que ofrece características como notificaciones de transacciones y simulación de costos de gas.

## **TxGhost – Monitor Modular para TRON**

TxGhost es un bot modular diseñado para ofrecer monitoreo en tiempo real y funciones de oráculo dentro de Telegram.

### **Arquitectura modular**

>[!IMPORTANT]
>El sistema está dividido en módulos independientes para asegurar estabilidad y facilidad de mantenimiento.

Módulo de monitoreo: escucha contratos TRC20 en tiempo real, detecta movimientos on-chain y los notifica automáticamente.

Módulo de oráculo: permite consultar precios de tokens y costos de transacción en tiempo real.

### **Configuración en grupos**

>[!TIP]
>La configuración es minimalista: solo necesitás una clave temporal generada por un admin.

Para habilitar el monitoreo en un grupo, el administrador genera una clave temporal mediante comando.

Se inicia con /start <clave> en el grupo donde se desea recibir notificaciones.

El bot valida permisos de administrador y elimina mensajes de comandos en chats públicos para mantener el orden.

### **Flujo de notificaciones**

>[!NOTE]
>El bot permanece silencioso hasta detectar actividad on-chain real.

Permanece en silencio hasta detectar transacciones.

Notifica en el grupo y en privado a los usuarios que hayan interactuado con el bot.

Cada mensaje incluye:
```
- Nombre del token  
- Monto de la compra  
- Dirección del holder  
- Supply al cierre de la compra  
- Precio pagado y holders actuales  
- Link a T-explorer para revisar la transacción sin salir de Telegram  
```
Trazabilidad de las interacciones de los contratos hasta la wallet del comprador

### **Funciones adicionales**

- `Topholders` Muestra ranking de los principales holders ordenados por tenencia
- `/mipuesto <dirección>` Informa la posición y % de participación en la lista global
- `info` Devuelve información detallada del token y enlaces a redes oficiales
- `Informe diario de transparencia` publica balances de unstake del TRX del contrato y de la wallet, precio del token en TRX y su equivalente en USDD
- `Gráfico` muestra evolución de los últimos 7 días
- `SR` informa la posición del Super Representante y cantidad de votos

### **Ghostlink – Oráculo independiente**
Ghostlink opera de forma autónoma, centralizando datos de precios y transacciones:

>[!NOTE]
>Ghostlink opera como servicio autónomo: no depende del monitor.

Muestra cotizaciones en tiempo real de tokens del ecosistema TRON

`/pr <parámetro>` devuelve una tarjeta con precio, admitiendo ticker, nombre o búsqueda aproximada

### **Simulador de Gas**

>[!IMPORTANT]
>Puede simular costos en múltiples cadenas, no solo TRON.

Calcula costos de transacciones en distintas cadenas

Puede usar APIs o ejecutar simulaciones de contratos

Incluye respaldo con transacciones de prueba y detalle del cálculo de precios

TxGhost no es solo un monitor, es una herramienta integral para seguimiento de contratos, transparencia y análisis on-chain.

[!CAUTION]
Los costos varían según congestión; el simulador incluye protección ante precios extremos.

---
## **Fantasmas de logo:**

>[!TIP]
>Cada fantasma tiene un color alusivo a una cripto distinta.
>TRON, PIVX, VERTCOIN, ZCASH, NEAR, POLKADOT, RAVENCOIN

---

📺 https://free2z.cash/uploadz/public/carover0/ghost.mp4
