# teste-projeto

# teste-projeto

## Criar um modelo de previsão no Azure ML com pontos de extremidade
a) Criar um workspace no Azure ML
Vá para https://ml.azure.com

Crie um workspace (caso não tenha um)

Acesse o workspace criado

## Implantar o modelo como serviço (endpoint)
Vá em Endpoints > Real-time endpoints

Clique em "Deploy model"

Escolha o modelo (modelo.joblib)

Configure um endpoint com:

Nome do serviço (ex: previsao-endpoint)

Inference script (score.py)

Arquivo de ambiente (env.yml)

---

### **4. Salvar no repositório:**
- `README.md` com instruções
- `endpoints.json` com a estrutura dos endpoints (exemplo abaixo)

```json
{
  "endpoint": "https://previsao-endpoint.azurewebsites.net/score",
  "method": "POST",
  "input_format": {
    "data": [[valor]]
  },
  "output_format": [resultado]
}
