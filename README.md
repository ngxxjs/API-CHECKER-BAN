# 📝 Documentação da API
📝 -> [DOCS](https://bot-api.spgunk.eu.org/docs)

##  API de verificar banimentos da conta
Rota da API = https://bot-api.spgunk.eu.org/check_ban?uid={uid}

**Endpoint:** `check_ban`

Este endpoint verifica banimentos da conta pelo ID do jogador.

### 📨 Exemplo de requisição:
```http
GET https://bot-api.spgunk.eu.org/check_ban?uid=883620604
```

### ☑️ Query Parameters

| Parameter | Type   | Required | Description                   |
|-----------|--------|----------|-------------------------------|
| `uid`     | int | Yes      | The user ID.                  |                 |


📚 **Objetivo da API**  

O objetivo principal de fornecer esta API gratuita é melhorar a experiência da comunidade Free Fire. 


🧩 **Frameworks e Biblioteca usada**  
- **FastAPI**:FastAPI é um framework web moderno, rápido (de alto desempenho) para criar APIs com Python com base em dicas de tipo padrão do Python.
- **Requests**: Para fazer solicitações HTTP ao servidor.

### 💬 Exemplo de resposta para conta não banida.
```json
{
  "status": "success",
  "message": "Essa conta não utilizou nenhuma trapaça, não foi banida.",
  "is_banned": 0,
  "period": 0,
  "credits": "https://t.me/ngxjs"
}
```

### 💬 Exemplo de resposta para conta banida.
```json
{
  "status": "success",
  "message": "Essa conta foi banida por uso de trapaça.",
  "is_banned": 1,
  "period": 6,
  "credits": "https://t.me/ngxjs"
}

```

API Made By Lucas(ngxjs),
