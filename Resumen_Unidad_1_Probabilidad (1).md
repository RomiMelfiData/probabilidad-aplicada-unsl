# Resumen — Unidad 1: Fundamentos de la Probabilidad

---

## 📚 Bibliografía de referencia

### 📘 Libro 1 — Mendenhall, Beaver & Beaver
> **"Introducción a la Probabilidad y Estadística"** — 13ª edición  
> *Cengage Learning*

| Sección | Tema | Páginas |
|---------|------|---------|
| 4.2 | Eventos y el Espacio Muestral | 129 – 130 |
| 4.3 | Cálculo de probabilidades con eventos sencillos | 131 – 136 |
| 4.4 | Reglas útiles de conteo *(permutaciones y combinaciones)* | 137 – 143 |
| 4.5 | Relaciones de eventos y reglas de probabilidad *(complemento, unión, intersección)* | 145 – 148 |
| 4.6 | Independencia, probabilidad condicional y regla de la multiplicación | 149 – 158 |
| 4.7 | Regla de Bayes *(opcional)* | 159 – 162 |

---

### 📗 Libro 2 — Jay L. Devore
> **"Probabilidad y Estadística para Ingeniería y Ciencias"** — 7ª edición  
> *Cengage Learning*

| Sección | Tema | Páginas |
|---------|------|---------|
| 2.1 | Espacios muestrales y eventos | 47 – 50 |
| 2.2 | Axiomas, interpretaciones y propiedades de probabilidad | 51 – 58 |
| 2.3 | Técnicas de conteo *(permutaciones y combinaciones)* | 59 – 66 |
| 2.4 | Probabilidad condicional | 67 – 75 |
| 2.5 | Independencia | 77 – 81 |

---

## 1. Conceptos básicos
> 📘 *Mendenhall et al.* — Cap. 4 (p. 128) | 📗 *Devore* — Sec. 2.2 (pp. 51–58)

La **probabilidad** es una medida cuantitativa que evalúa la posibilidad de que ocurra un evento. Sus valores se encuentran entre 0 y 1:

$$0 \leq P(A) \leq 1$$

| Valor | Interpretación |
|-------|---------------|
| $P(A) = 0$ | Evento imposible |
| $P(A) = 1$ | Evento seguro |
| $0 < P(A) < 1$ | Grado de posibilidad |

Las probabilidades se expresan como fracciones, decimales o porcentajes (ej.: $\frac{1}{4}$, $0.25$, $25\%$).

---

## 2. Tipos de decisión bajo incertidumbre
> 📘 *Mendenhall et al.* — Cap. 4 (pp. 128–129)

- **Certeza:** se conoce un único resultado para cada alternativa.
- **Riesgo:** a cada alternativa se asocia más de un resultado posible, con probabilidades conocidas.
- **Incertidumbre:** las probabilidades son desconocidas o no tienen sentido por no ser hechos repetitivos.

---

## 3. Tipos de probabilidad
> 📘 *Mendenhall et al.* — Sec. 4.3 (pp. 131–136) | 📗 *Devore* — Sec. 2.2 (pp. 51–58)

### 3.1 Probabilidad Clásica (a priori) — Regla de Laplace

Aplicable cuando todos los resultados son **equiprobables**:

$$P(A) = \frac{\text{Número de resultados favorables a } A}{\text{Número total de resultados posibles}}$$

### 3.2 Probabilidad Frecuencial (empírica)

Se basa en la **frecuencia relativa** observada de un evento en un gran número de ensayos:

$$P(A) \approx \frac{\text{Número de veces que ocurrió } A}{\text{Número total de ensayos}}$$

### 3.3 Probabilidad Subjetiva

Asignada por un individuo basándose en su experiencia, información disponible y juicio personal. No requiere experimentos repetibles.

---

## 4. Espacio muestral y eventos
> 📘 *Mendenhall et al.* — Sec. 4.2 (pp. 129–130) | 📗 *Devore* — Sec. 2.1 (pp. 47–50)

- **Experimento aleatorio:** proceso que genera resultados determinados; en cada repetición hay uno y solo uno de los posibles resultados.
- **Espacio muestral** $S$: conjunto de **todos** los posibles resultados de un experimento.
  - Ejemplo moneda: $S = \{\text{Cara, Ceca}\}$
  - Ejemplo pieza: $S = \{\text{Defectuosa, Sin defecto}\}$
- **Evento:** uno o más resultados del espacio muestral.

### Tipos de eventos

| Tipo | Definición |
|------|-----------|
| **Mutuamente excluyentes** | No pueden ocurrir al mismo tiempo (ej.: cara y ceca en un lanzamiento) |
| **No mutuamente excluyentes** | Pueden ocurrir simultáneamente (ej.: As y Copa al sacar una carta) |
| **Colectivamente exhaustivos** | La lista incluye **todos** los posibles resultados del experimento |
| **Estadísticamente independientes** | Un evento no afecta la probabilidad del otro |

---

## 5. Reglas de conteo (Análisis Combinatorio)
> 📘 *Mendenhall et al.* — Sec. 4.4 (pp. 137–143) | 📗 *Devore* — Sec. 2.3 (pp. 59–66)

### 5.1 Principio Multiplicativo

Si hay $n_1$ formas de hacer la tarea 1, $n_2$ formas de hacer la tarea 2, …, $n_k$ formas de hacer la tarea $k$ (todas independientes), entonces el número total de resultados posibles es:

$$\text{Total} = n_1 \times n_2 \times n_3 \times \cdots \times n_k$$

> **Ejemplo:** Menú con 5 entradas, 5 platos y 5 postres → $5 \times 5 \times 5 = 125$ combinaciones.

---

### 5.2 Factorial de un número

El factorial de un número natural $n$ se define como:

$$n! = n \cdot (n-1) \cdot (n-2) \cdots 2 \cdot 1$$

Por convención: $0! = 1$

---

### 5.3 Permutaciones sin repetición

Ordenación de **todos** los elementos de un conjunto, donde **importa el orden** y **no se repiten** elementos.

$$P(n) = n!$$

> **Ejemplo:** ¿De cuántas formas pueden sentarse 4 personas en 4 sillas?
> $P(4) = 4! = 4 \times 3 \times 2 \times 1 = 24$

---

### 5.4 Permutaciones con repetición

Cuando $n$ elementos se permutan, pero algunos se repiten ($m$ veces uno, $r$ veces otro, …, $s$ veces el último):

$$PR_n^{m,\, r,\, \ldots,\, s} = \frac{n!}{m! \cdot r! \cdots s!}$$

> **Ejemplo:** Anagramas de MATEMÁTICA (10 letras: M×2, T×2, A×3):
> $$PR_{10}^{2,2,3} = \frac{10!}{2! \cdot 2! \cdot 3!} = \frac{3{.}628{.}800}{24} = 151{.}200$$

---

### 5.5 Permutaciones circulares

Ordenación de $n$ elementos en **círculo**, donde importa el orden:

$$PC(n) = \frac{n!}{n} = (n-1)!$$

> **Ejemplo:** 4 personas alrededor de una mesa circular:
> $PC(4) = (4-1)! = 3! = 6$

---

### 5.6 Variaciones sin repetición

Agrupaciones **ordenadas** de $n$ elementos tomados de $m$ en total ($n \leq m$), sin repetición. **Sí importa el orden.**

$$V(m,n) = V_m^n = \frac{m!}{(m-n)!}$$

> **Ejemplo:** Elegir Presidente, Vicepresidente y Secretario de un grupo de 6:
> $$V(6,3) = \frac{6!}{(6-3)!} = \frac{720}{6} = 120$$

---

### 5.7 Combinaciones

Agrupaciones de $n$ elementos tomados de $m$ en total, donde **NO importa el orden** y no se repiten elementos.

$$C(m,n) = \binom{m}{n} = \frac{V(m,n)}{P(n)} = \frac{m!}{(m-n)! \cdot n!}$$

> **Ejemplo:** Elegir 3 administrativos de un grupo de 6 (sin jerarquía):
> $$C(6,3) = \frac{6!}{3! \cdot 3!} = \frac{720}{6 \cdot 6} = 20$$

---

### 5.8 Número combinatorio

El **número combinatorio** $\binom{n}{k}$ representa el número de formas de seleccionar $k$ elementos de $n$ sin importar el orden:

$$\binom{n}{k} = \frac{n!}{(n-k)!\cdot k!}$$

> Es equivalente a $C(n,k)$ y se usa extensamente en probabilidad y estadística.

---

### Tabla resumen de técnicas de conteo

| Técnica | ¿Importa el orden? | ¿Todos los elementos? | ¿Repetición? | Fórmula |
|---------|-------------------|----------------------|--------------|---------|
| Permutación sin repetición | ✅ Sí | ✅ Todos | ❌ No | $n!$ |
| Permutación con repetición | ✅ Sí | ✅ Todos | ✅ Sí | $\frac{n!}{m!\cdot r!\cdots s!}$ |
| Permutación circular | ✅ Sí | ✅ Todos | ❌ No | $(n-1)!$ |
| Variación sin repetición | ✅ Sí | ❌ Subgrupo | ❌ No | $\frac{m!}{(m-n)!}$ |
| Combinación | ❌ No | ❌ Subgrupo | ❌ No | $\frac{m!}{(m-n)!\cdot n!}$ |

---

## 6. Cálculo de probabilidades
> 📘 *Mendenhall et al.* — Sec. 4.5 y 4.6 (pp. 145–158) | 📗 *Devore* — Sec. 2.2, 2.4 y 2.5 (pp. 51–81)

### 6.1 Probabilidad simple (marginal)

Probabilidad de un único evento:

$$P(A) = \frac{\text{casos favorables}}{\text{casos totales}}$$

### 6.2 Complemento de un evento

Los eventos $A$ y $\overline{A}$ (no $A$) son **mutuamente excluyentes y exhaustivos**:

$$P(A) + P(\overline{A}) = 1 \implies P(\overline{A}) = 1 - P(A)$$

---

### 6.3 Regla de la adición — eventos mutuamente excluyentes

Si $A$ y $B$ **no pueden ocurrir simultáneamente**:

$$P(A \cup B) = P(A \text{ o } B) = P(A) + P(B)$$

> **Ejemplo:** Probabilidad de que salga cara o que salga ceca en un lanzamiento:
> $P(\text{C o +}) = \frac{1}{2} + \frac{1}{2} = 1$

---

### 6.4 Regla de la adición — eventos NO mutuamente excluyentes

Si $A$ y $B$ **pueden ocurrir al mismo tiempo** (se evita el doble conteo):

$$P(A \cup B) = P(A \text{ o } B) = P(A) + P(B) - P(A \cap B)$$

> **Ejemplo:** Probabilidad de sacar un As **o** Copa de una baraja de 50 cartas:
> $$P(\text{As o Copa}) = \frac{4}{50} + \frac{12}{50} - \frac{1}{50} = \frac{15}{50} = 0.30$$

---

### 6.5 Probabilidad conjunta — eventos independientes

Cuando dos eventos **no se afectan mutuamente**:

$$P(A \cap B) = P(A \text{ y } B) = P(A) \times P(B)$$

> **Ejemplo:** Probabilidad de obtener 3 caras consecutivas con una moneda:
> $$P(\text{CCC}) = \frac{1}{2} \times \frac{1}{2} \times \frac{1}{2} = \frac{1}{8} = 0.125$$

---

### 6.6 Probabilidades conjuntas y marginales (tablas)

Las **probabilidades conjuntas** involucran dos eventos simultáneos; las **probabilidades marginales** involucran un solo evento y aparecen en los márgenes de la tabla.

**Ejemplo:** Corporación de 1200 agentes (960 hombres, 240 mujeres; 324 promovidos, 36 mujeres):

|  | Hombre | Mujer | **Total** |
|--|--------|-------|-----------|
| **Promovido** | $288/1200 = 0.24$ | $36/1200 = 0.03$ | **0.27** |
| **No promovido** | $672/1200 = 0.56$ | $204/1200 = 0.17$ | **0.73** |
| **Total** | **0.80** | **0.20** | **1.00** |

- Los valores interiores (zona amarilla) = **probabilidades conjuntas**
- Los valores del margen (totales) = **probabilidades marginales**

---

## 7. Diagrama de Venn

Herramienta visual para representar eventos y su espacio muestral:
- El **rectángulo** representa el espacio muestral completo (área = 1).
- Los **círculos** representan eventos.
- Si los círculos **no se superponen** → eventos mutuamente excluyentes.
- Si los círculos **se superponen** → eventos no mutuamente excluyentes; la intersección es $P(A \cap B)$.

---

## 8. Síntesis de fórmulas clave

$$\boxed{P(A) = \frac{\text{casos favorables}}{\text{casos totales}}} \qquad \boxed{P(\overline{A}) = 1 - P(A)}$$

$$\boxed{P(A \cup B) = P(A) + P(B)} \quad \text{(mutuamente excluyentes)}$$

$$\boxed{P(A \cup B) = P(A) + P(B) - P(A \cap B)} \quad \text{(no mutuamente excluyentes)}$$

$$\boxed{P(A \cap B) = P(A) \times P(B)} \quad \text{(independientes)}$$

$$\boxed{n! = n \cdot (n-1) \cdots 1} \qquad \boxed{P(n) = n!} \qquad \boxed{PC(n) = (n-1)!}$$

$$\boxed{PR_n^{m,r,\ldots,s} = \frac{n!}{m!\cdot r!\cdots s!}} \qquad \boxed{V(m,n) = \frac{m!}{(m-n)!}} \qquad \boxed{C(m,n) = \frac{m!}{(m-n)!\cdot n!}}$$

---

## 9. Tipos de problemas del Trabajo Práctico N° 1

A continuación se clasifican los 28 problemas del TP por técnica:

| Problema | Tema | Técnica principal |
|----------|------|-------------------|
| 1 | Múltiple choice (4 preguntas × 5 opciones) | Principio multiplicativo |
| 2 | Asientos en ómnibus (familia de 4) | Permutaciones / prob. simple |
| 3 | Chapas patentes (2 letras + 3 números + 2 letras) | Principio multiplicativo |
| 4 | Anagramas de PROCESAMIENTO | Permutaciones con repetición |
| 5 | Equipo de gestión empresarial | Principio multiplicativo |
| 6 | Clave Home Banking (4 letras + 4 números) | Principio multiplicativo |
| 7 | Carrera de 10 caballos (3 primeros puestos) | Variaciones sin repetición |
| 8 | Menú más costoso (3 platos) | Probabilidad simple |
| 9 | Directorio rotativo (5 socios, 5 cargos) | Permutaciones sin repetición |
| 10 | Guardias pasivas (11 empleados, grupos de 2) | Combinaciones |
| 11a | Comisión directiva con jerarquía (20 candidatos, 4 puestos) | Variaciones sin repetición |
| 11b | Vocales sin jerarquía (3 de los 16 restantes) | Combinaciones |
| 12 | Capelinas de helado (31 sabores, 3 bolas) | Combinaciones |
| 13 | Condimentos para hamburguesa (8 condimentos) | Subconjuntos / $2^n$ |
| 14a | Becas iguales (3 de 17 empleados) | Combinaciones |
| 14b | Becas de importes distintos (orden importa) | Variaciones sin repetición |
| 15 | Asientos en el cine (mujeres juntas, varones juntos) | Permutaciones + principio multiplicativo |
| 16 | Mesa redonda (5 sillas, 6 amigos) | Permutaciones circulares |
| 17 | Decisión en empresa láctea | Tipos de decisión (certeza/riesgo/incertidumbre) |
| 18 | Contraseñas alfanuméricas sin repetición | Variaciones sin repetición |
| 19–28 | Problemas de aplicación abierta | Probabilidad frecuencial / subjetiva |

---

> **Nota:** Los problemas 19 a 28 son de análisis y argumentación: se aplican los **tipos de probabilidad** (clásica, frecuencial y subjetiva) en contextos de negocios, tecnología, salud y logística, sin una única respuesta numérica correcta.
