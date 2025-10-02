# 📈 Uplift Modeling para Retención / Cross-sell

**Objetivo negocio:** maximizar **ROI incremental** seleccionando a quién contactar.  
**Dataset:** Bank Marketing (Portugal, UCI) + costes/beneficios supuestos.

---

## 🔧 Metodología
- **T-Learner** (dos modelos) y **Uplift Trees**.
- **Evaluación**: **Qini**, **Uplift@k**, **ROI incremental** con matriz de costes.
- **Política** de targeting: regla por **top-k** o **umbral** de uplift.

---

## ▶️ Cómo ejecutar
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

make prepare   # descarga/prepara datos
make train     # entrena T-Learner y Uplift Trees
make eval      # Qini/CGains + ROI incremental
