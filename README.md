# Google + Alura Imersão

Este projeto utiliza a API Google Generative AI para explorar e gerar conteúdo usando modelos de inteligência artificial avançados.

## Instalação

Para instalar as dependências necessárias para executar este projeto, execute o seguinte comando:

```bash
pip install -q -U google-generativeai
```

## Configuração

Antes de executar o projeto, é necessário configurar a chave da API fornecida pela Google:

```python
import google.generativeai as genai

GOOGLE_API_KEY = 'YOUR_API_KEY'
genai.configure(api_key=GOOGLE_API_KEY)
```

Substitua `'YOUR_API_KEY'` pela sua chave de API real.

## Uso

O projeto inclui scripts para listar modelos disponíveis e gerar conteúdo com configurações específicas de geração e segurança:

### Listar Modelos Disponíveis

Para listar modelos que suportam a geração de conteúdo:

```python
for model in genai.list_models():
    if 'generateContent' in model.supported_generation_methods:
        print(model.name)
```

### Configurações de Geração

Configurações de geração e segurança podem ser ajustadas conforme necessário:

```python
generation_config = {
    'candidate_count': 1,
    'temperature': 0.5,
}

safety_settings = {
    'HARASSMENT': 'BLOCK_NONE',
    'HATE': 'BLOCK_NONE',
    'SEXUAL': 'BLOCK_NONE',
    'DANGEROUS': 'BLOCK_NONE'
}
```

## Autor

Lucas Knust

---
