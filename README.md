# 💸 BUDGET CALC — Calculadora Inteligente para Freelancers

**BUDGET CALC** es una herramienta web diseñada para ayudar a desarrolladores y creativos independientes a calcular presupuestos precisos, mitigando riesgos y asegurando la rentabilidad. A diferencia de una calculadora simple, esta herramienta aplica factores de complejidad técnica, riesgo de cliente y multiplicadores por stack tecnológico.

## ✨ Características Principales

* **🎚️ Lógica de Precisión:** Ajusta horas, tarifas, margen de beneficio y riesgo del cliente mediante sliders intuitivos.
* **🧠 Factor de Complejidad Exponencial:** Aplica una fórmula que refleja el aumento real del costo en proyectos de alta complejidad técnica.
* **🛠️ Stack Multiplier:** Incluye un catálogo de tecnologías (React, AWS, AI/ML, Blockchain, etc.) que ajustan el presupuesto según la demanda y especialización requerida.
* **🏢 Perfiles de Cliente:** Diferencia presupuestos según el tipo de cliente (Startup, PYME, Corporativo o Agencia).
* **📊 Resumen Financiero en Tiempo Real:** Visualiza la base neta, el precio con riesgos y la tarifa efectiva por hora.
* **📋 Exportación Estilizada:** Genera un resumen profesional en formato texto (ASCII Art) listo para copiar y enviar a clientes o incluir en propuestas.

## 🛠️ Tecnologías Utilizadas

* **HTML5 & CSS3:** Diseño minimalista tipo "Dashboard" con una paleta de colores profesional (Dark Mode).
* **JavaScript (Vanilla):** Lógica de cálculo reactiva sin dependencias externas.
* **Google Fonts:** Uso de *JetBrains Mono* para una estética técnica y *Syne* para los encabezados.

## 🧮 Lógica de Cálculo

La herramienta utiliza una serie de multiplicadores encadenados:
1.  **Base:** `(Horas Estimadas + Horas de Revisión) × Tarifa/Hr`.
2.  **Complejidad:** Multiplicador basado en una curva de potencia: `1 + Math.pow((complejidad - 1) / 9, 1.6) * 0.9`.
3.  **Riesgo:** Incremento porcentual sobre el subtotal ajustado para cubrir imprevistos.
4.  **Margen:** Beneficio neto final aplicado sobre el total con riesgos.

## 🚀 Instalación y Uso

Al ser una aplicación estática, no requiere servidor ni instalación compleja:

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/budget-calc-freelance.git](https://github.com/tu-usuario/budget-calc-freelance.git)
    ```
2.  **Abre el archivo:**
    Simplemente abre `index.html` en tu navegador.

## ⚙️ Personalización

Puedes ajustar las tarifas de las herramientas editando el objeto `TOOLS` en el script principal:
```javascript
const TOOLS = [
  { name: 'React', cost: 1.05 },
  { name: 'AWS', cost: 1.08 },
  // ... añade tus propias herramientas y sus multiplicadores
];