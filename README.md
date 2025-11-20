## **SmartWork – Monitor de Bem-Estar no Trabalho (Arduino UNO)**

Projeto desenvolvido para a disciplina **GLOBAL SOLUTIONS 2025 – O Futuro do Trabalho** da FIAP.

Este protótipo demonstra como sistemas embarcados e sensores podem melhorar o **bem-estar, ergonomia e produtividade** no ambiente de trabalho, alinhado às necessidades e desafios do futuro.

---

# 🎯 **1. Problema**

O futuro do trabalho envolve ambientes híbridos, longas jornadas em frente ao computador e desafios de ergonomia e saúde.
Ambientes inadequados — como temperatura alta, pouca luz ou umidade fora do ideal — prejudicam:

* Conforto
* Saúde física
* Produtividade
* Concentração

Profissionais nem sempre percebem quando é necessário ajustar o ambiente ou fazer pausas.

---

# 💡 **2. Solução Desenvolvida: SmartWork**

O **SmartWork** é um sistema baseado em **Arduino UNO** que monitora, em tempo real:

✔ Temperatura (DHT22)
✔ Umidade (DHT22)
✔ Luminosidade (Módulo LDR analógico)

O sistema analisa as condições e classifica o ambiente como:

* **Confortável**
* **Crítico**

Se estiver crítico, o sistema:

🔥 Acende automaticamente um **LED vermelho de alerta**
🔥 Envia pelo Serial uma **requisição HTTP simulada**, igual a um servidor IoT, contendo os dados em **JSON**

Isso representa como soluções reais de IoT podem funcionar no futuro do trabalho.

---

# 🧱 **3. Componentes Utilizados**

* Arduino UNO
* Sensor DHT22
* Módulo LDR analógico (A0)
* LED Vermelho
* Resistor 220Ω (LED)
* Jumpers
* Protoboard

---

# 🔌 **4. Ligações do Circuito**

### **DHT22**

* VCC → 5V
* DATA → pino **7**
* GND → GND

### **Módulo LDR**

* VCC → 5V
* GND → GND
* A0 → pino **A0** do Arduino
* D0 → **não utilizado**

### **LED**

* Anodo → Resistor 220Ω → pino **9**
* Catodo → GND

---

# 🛰️ **5. Comunicação IoT Simulada (HTTP + JSON)**

O sistema envia no Monitor Serial:

### Cabeçalho HTTP real:

```
POST /api/smartwork/dados HTTP/1.1
Host: api.smartwork.com
Content-Type: application/json
Content-Length: XX
```

### Corpo JSON com os dados:

```json
{
  "temperature": 27.5,
  "humidity": 55.2,
  "light": 350,
  "status": "critico",
  "reason": "Luminosidade baixa; Temperatura alta;"
}
```

Isso demonstra como sistemas podem enviar dados para dashboards ou APIs de monitoramento.

---

# 🧪 **6. Simulação Wokwi**

🔗 **LINK DO PROJETO WOKWI (PÚBLICO):**

> [PROJETO SMARTWORK](https://wokwi.com/projects/448151961120284673)

*https://wokwi.com/projects/448151961120284673)*

---

# 🧠 **7. Funcionamento**

1. Arduino lê temperatura, umidade e luz
2. Avalia se o ambiente está crítico
3. Acende o LED caso necessário
4. Gera uma requisição HTTP com JSON
5. Exibe tudo no Serial Monitor em tempo real

---

# 📂 **8. Estrutura do Repositório**

```
/SmartWork
 ├── README.md
 ├── smartwork.ino
 └── imagens/
```

---

# 🌍 **9. Impacto no Futuro do Trabalho**

O SmartWork mostra como tecnologias simples podem:

* Garantir ambientes de trabalho mais saudáveis
* Reduzir fadiga
* Melhorar ergonomia
* Auxiliar empresas em monitoramento ambiental
* Automatizar processos de bem-estar

É um protótipo simples, escalável e alinhado às tendências de IoT e saúde ocupacional.

---

# 👨‍🏫 **10. Integrantes do Grupo**

**Equipe:**

* Lucas Alves de Souza RM
* Kaio Vinicius Meireles Alves RM553282

---

# 🧾 **11. Professor(a)**

Nome do Professor(a): **[ Gedeane ]**

---

# 🎓 **12. Instituição**

FIAP – Global Solutions 2025
Curso: [Engenharia de Software 3ESPR]

---

# **13. Vídeo Explicativo**


LINK: [https://youtu.be/52TBHHGuU80]

---


# ✔ DONE!

Se quiser, eu agora gero também:

✅ **PDF pronto para enviar**
✅ **Slide PowerPoint pronto**
✅ **Texto que você deve falar no vídeo**
✅ **Resumo curto para postar no Teams**

É só pedir!
