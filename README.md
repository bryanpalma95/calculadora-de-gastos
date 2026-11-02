# 💰 Calculadora de Gastos

Aplicación web de control financiero personal y del hogar con sincronización en la nube.

## Funcionalidades

### 🏠 Hogar
- Registro de integrantes con su ingreso mensual
- Gastos del hogar se alimentan automáticamente desde los gastos fijos/recurrentes registrados en Personal
- Distribución proporcional según ingresos (cuánto paga cada uno, cuánto le sobra)

### 👤 Personal
- Registro de ingresos y gastos con categorías
- Categorías personalizadas (el usuario puede crear las suyas)
- Marcado de gastos fijos/recurrentes
- Filtros por tipo (todos, gastos, ingresos)
- Gráfico donut por categoría
- Mini calculadora integrada en el campo de monto

### 🎯 Metas Financieras
- Ahorro mensual (10% del sueldo) — asignación manual
- Gustos y salidas (20% del sueldo) — cálculo automático desde categorías Entretenimiento/Ropa
- Gastos fijos (70% del sueldo) — cálculo automático desde gastos recurrentes
- Fondo de emergencia (4 sueldos) — acumulado manual
- Meta de inversión (200 sueldos) — proyección basada en el ahorro
- Presupuestos por categoría con alertas al 80% y 100%

### 📅 Resumen Mensual
- Vista consolidada por mes/año
- Estadísticas: ingresos, gastos, balance, promedio
- Gráfico por categoría
- Cargar gastos fijos del mes
- Exportar a CSV (compatible con Excel)

### 🧮 Calculadora
- Calculadora completa con operaciones básicas
- Soporte de teclado (números, operadores, Enter, Escape, Backspace)
- Botón "Copiar a Monto" que envía el resultado al formulario
- Mini calculadora accesible desde el campo de monto (ícono 🧮)

### Extras
- Modo oscuro / claro con persistencia
- Menú lateral con navegación, calendario y fecha actual
- Recuerda la pestaña activa al refrescar
- Login con email y contraseña (Firebase Auth)
- Recuperar contraseña por email
- Datos sincronizados en la nube (Firebase Firestore)
- Funciona en móvil y escritorio (responsive)

## Estructura del Proyecto

```
calculadora-de-gastos/
├── index.html              # App principal (login + app completa)
├── index2.html             # Versión alternativa
├── negocio.html            # Vista enfocada en gastos de negocio
├── respaldo-index.html     # Respaldo anterior
├── css/styles.css          # Estilos globales con modo oscuro/claro
├── js/app.js               # Lógica completa: Firebase, UI, finanzas
├── tests/
│   ├── tests.html          # Suite de pruebas visual
│   └── run-tests.js        # Runner de pruebas
└── backup_pre_mejoras/     # Respaldo antes de refactorizaciones grandes
```

## Cómo usar

1. Abre `index.html` en el navegador (requiere conexión para Firebase)
2. Regístrate con email y contraseña o inicia sesión
3. Navega por las secciones usando el menú lateral

## Tecnologías

- HTML / CSS / JS vanilla
- Firebase 10 (Auth + Firestore)
- Sin frameworks ni bundler — carga directa en el navegador

## Privacidad y datos

- Los datos se almacenan en **Firebase Firestore** bajo la cuenta del usuario
- Cada usuario ve únicamente sus propios datos
- La API key incluida es la anon key pública del proyecto, protegida por reglas Firestore
