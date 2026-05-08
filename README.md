# 🗂️ Classificador CNAE

Extensão para Google Chrome que classifica CNAEs automaticamente em **Serviço**, **Comércio** ou **Indústria**, indicando o **Anexo do Simples Nacional** correspondente.

Busca por lista de códigos colados manualmente ou diretamente pelo **CNPJ** da empresa via Receita Federal.

---

## ✨ Funcionalidades

- **Classificação por lista** — cole um ou vários CNAEs (com ou sem descrição) e gere a tabela instantaneamente
- **Busca por CNPJ** — informe o CNPJ e todos os CNAEs da empresa (principal e secundários) são buscados e classificados automaticamente
- **Banco de dados completo** — 1.338 subclasses da tabela CNAE 2.3 oficial do IBGE mapeadas
- **Anexo do Simples Nacional** — identifica Anexo I, II, III, IV, V ou VI para cada CNAE
- **Copiar tabela** — exporta o resultado em formato Markdown com um clique
- **Destaque do CNAE principal** — diferencia visualmente o CNAE principal dos secundários

---

## 📋 Categorias identificadas

| Categoria  | Exemplos de divisões CNAE         | Anexo Simples |
|------------|-----------------------------------|---------------|
| Comércio   | 45.xx, 46.xx, 47.xx               | Anexo I       |
| Indústria  | 10.xx a 33.xx                     | Anexo II      |
| Serviço    | 41.xx – 43.xx, 49.xx – 99.xx     | Anexo III–VI  |

---

## 🚀 Instalação

### Via Chrome Web Store
Disponível em breve na [Chrome Web Store](#).

### Manualmente (modo desenvolvedor)
1. Baixe o [release](https://github.com/Marcinho-3-bola/CNAEs-extension/releases) mais recente.
2. Acesse `chrome://extensions` no Chrome.
3. Ative o **Modo do desenvolvedor** (canto superior direito).
4. Clique em **"Carregar sem compactação"**.
5. Selecione a pasta `cnae-extension`.

---

## 🔍 Como usar

### Aba CNAEs (manual)
1. Abra a extensão clicando no ícone na barra do Chrome
2. Cole os CNAEs na caixa de texto (aceita com ou sem descrição)
3. Clique em **⚡ Classificar**
4. Use **📋 Copiar tabela** para exportar em Markdown

**Formatos aceitos:**
```
47.81-4-00
47.81-4-00 - Comércio varejista de artigos do vestuário
CÓDIGO E DESCRIÇÃO DA ATIVIDADE ECONÔMICA PRINCIPAL 56.11-2-01 - Restaurantes e similares
```

### Aba CNPJ
1. Clique na aba **🏢 CNPJ**
2. Digite o CNPJ (com ou sem pontuação)
3. Clique em **🔍 Buscar**
4. A extensão consulta a Receita Federal e classifica todos os CNAEs automaticamente

---

## 🛠️ Tecnologias

- HTML, CSS, JavaScript puro (sem dependências externas)
- [BrasilAPI](https://brasilapi.com.br) — consulta de CNPJ (principal)
- [ReceitaWS](https://receitaws.com.br) — fallback para consulta de CNPJ
- Tabela CNAE 2.3 — [IBGE/CONCLA](https://concla.ibge.gov.br)

---

## 📁 Estrutura do projeto

```
cnae-extension/
├── manifest.json       # Configuração da extensão (Manifest V3)
├── popup.html          # Interface da extensão
├── popup.js            # Lógica de classificação e busca por CNPJ
└── icon.png            # Ícone da extensão
```

---

## 📄 Licença

GNU GENERAL PUBLIC LICENSE

---

## 🤝 Contribuições

Pull requests são bem-vindos! Para mudanças maiores, abra uma issue primeiro para discutir o que você gostaria de alterar.

---

*Base de dados: CNAE 2.3 — IBGE/CONCLA — 1.338 subclasses*
