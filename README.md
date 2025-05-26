# 🎙️ Azure Speech Studio & Language Studio – Análise de Fala e Linguagem Natural

Este repositório documenta o uso das ferramentas **Azure Speech Studio** e **Azure Language Studio**, com foco em **análise de fala** e **processamento de linguagem natural (NLP)**.

---

## 📚 Índice

- [🔍 Visão Geral](#-visão-geral)
- [🧠 Azure Speech Studio](#-azure-speech-studio)
- [🧠 Azure Language Studio](#-azure-language-studio)
- [🛠️ Recursos e Funcionalidades](#-recursos-e-funcionalidades)
- [🚀 Casos de Uso](#-casos-de-uso)
- [⚙️ Como Usar](#-como-usar)
- [📊 Comparativo](#-comparativo)
- [💡 Boas Práticas](#-boas-práticas)
- [🔗 Referências](#-referências)

---

## 🔍 Visão Geral

As ferramentas **Azure Speech Studio** e **Language Studio** são parte dos **Serviços Cognitivos do Azure** e possibilitam:

- Interpretação automática da fala  
- Transcrição e tradução  
- Geração de fala a partir de texto  
- Análise de texto com NLP  
- Extração de sentimentos, entidades e tópicos  

---

## 🧠 Azure Speech Studio

O **Speech Studio** é uma plataforma visual para criar e testar serviços de fala.

### 🎤 Funcionalidades principais

- **Reconhecimento de Fala (ASR)**: converte voz em texto.  
- **Tradução de Fala**: traduz áudio entre idiomas.  
- **Síntese de Fala (TTS)**: converte texto em voz natural.  
- **Modelos Customizados**: permite treinar modelos com vocabulário técnico.  
- **Análise de Áudio**: detecta pausas, ruído, entonação, emoções.  

---

## 🧠 Azure Language Studio

O **Language Studio** permite aplicar modelos de NLP em textos.

### 🧠 Funcionalidades principais

- **Análise de Sentimentos**: classifica sentimentos em positivo, negativo e neutro.  
- **Extração de Entidades Nomeadas (NER)**: identifica nomes, locais, organizações.  
- **Classificação de Texto**: categoriza textos com base em conteúdo.  
- **Frases-chave**: extrai conceitos principais de um texto.  
- **Perguntas e Respostas**: cria Q&A baseados em contexto.  
- **Customização**: treine com seus próprios exemplos.  

---

## 🛠️ Recursos e Funcionalidades

| Funcionalidade                 | Speech Studio ✅ | Language Studio ✅ |
|-------------------------------|------------------|--------------------|
| Reconhecimento de Fala        | ✅               | ❌                 |
| Tradução de Fala              | ✅               | ❌                 |
| Síntese de Fala (voz)         | ✅               | ❌                 |
| Análise de Sentimentos        | ❌               | ✅                 |
| Extração de Entidades         | ❌               | ✅                 |
| Classificação de Texto        | ❌               | ✅                 |
| Customização de Modelos       | ✅               | ✅                 |
| Testes Interativos            | ✅               | ✅                 |
| Suporte a APIs REST           | ✅               | ✅                 |

---

## 🚀 Casos de Uso

### 🏥 Saúde
- Transcrição de consultas médicas (Speech)  
- Análise de opiniões de pacientes (Language)  

### 📞 Call Centers
- Gravação e transcrição automática (Speech)  
- Detecção de intenções e entidades (Language)  

### 📚 Educação
- Leitura automatizada de conteúdos (Speech)  
- Análise de redações com extração de tópicos (Language)  

### 🧑‍💼 Atendimento ao Cliente
- Assistentes de voz (Speech)  
- Chatbots inteligentes (Language)  

---

## ⚙️ Como Usar

### 1. Criar os recursos no Azure

- Acesse o [portal Azure](https://portal.azure.com)
- Crie os recursos:
  - `Speech` (reconhecimento, TTS)
  - `Language` (serviços de NLP)

### 2. Acessar as ferramentas

- [Speech Studio](https://speech.microsoft.com)
- [Language Studio](https://language.cognitive.azure.com)

### 3. Testar via API

#### 🎧 Exemplo: Transcrição de Fala com Speech API (cURL)


curl -X POST "https://<região>.stt.speech.microsoft.com/speech/recognition/conversation/cognitiveservices/v1?language=pt-BR" \
  -H "Ocp-Apim-Subscription-Key: <sua-chave>" \
  -H "Content-Type: audio/wav" \
  --data-binary "@audio.wav"

## Exemplo: Análise de Sentimento com Language API (cURL) `


curl -X POST "https://<região>.api.cognitive.microsoft.com/language/:analyze-text?api-version=2023-04-01" \
  -H "Ocp-Apim-Subscription-Key: <sua-chave>" \
  -H "Content-Type: application/json" \
  -d '{
    "kind": "SentimentAnalysis",
    "parameters": {
      "text": "Este serviço é ótimo!",
      "language": "pt"
    }
  }'


## 📊 Comparativo

| Aspecto               | Speech Studio               | Language Studio               |
|-----------------------|----------------------------|-------------------------------|
| Entrada principal     | Áudio                      | Texto                         |
| Foco                  | Conversão e Geração de Fala | Análise de Texto e NLP        |
| Modelos disponíveis   | ASR, TTS, Tradução         | Sentimentos, Entidades, etc   |
| Domínios customizáveis| Sim                        | Sim                           |

## 💡 Boas Práticas

- **🔐 Segurança**: Use variáveis de ambiente para armazenar suas chaves.  
- **🗂️ Formato de áudio recomendado**: WAV, 16-bit mono PCM.  
- **🔁 Teste iterativo**: Valide com exemplos reais.  
- **🌎 Locale**: Sempre especifique o idioma correto (`pt-BR`, `en-US`, etc.).  
- **📚 Documentação**: Mantenha referência constante à documentação oficial.  

## 🔗 Referências

- [🔊 Azure Speech Services](https://azure.microsoft.com/pt-br/products/cognitive-services/speech-services/)  
- [🎤 Speech Studio](https://speech.microsoft.com/)  
- [🧠 Azure Language Service](https://azure.microsoft.com/pt-br/products/cognitive-services/language-service/)  
- [🧪 Language Studio](https://language.cognitive.azure.com/)  
- [💰 Preços Azure Cognitive Services](https://azure.microsoft.com/pt-br/pricing/details/cognitive-services/)  
