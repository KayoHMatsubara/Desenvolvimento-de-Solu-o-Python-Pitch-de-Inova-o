# Quebrador de Planilhas V2
> **Projeto de Atividade Final (A2)** | Automação de Processos com Python

Este script é uma ferramenta robusta para manipulação de grandes volumes de dados. Ele resolve o problema comum de arquivos CSV que excedem o limite de linhas do Excel ou que são pesados demais para sistemas legados, permitindo o particionamento inteligente e conversão de formato.

## Funcionalidades
* Divisão Dinâmica: Controle total sobre o número de registros por arquivo.
* Multi-formato: Exportação instantânea para .csv (rápido) ou .xlsx (pronto para uso administrativo).
* Integridade de Dados: Leitura em modo texto com utf-8-sig para garantir que CPFs, CNPJs e IDs com zeros à esquerda não sejam alterados.
* Parser Inteligente: Utiliza o motor do Pandas para detectar automaticamente se o separador original é , ou ;.

## Tecnologias Utilizadas
* Python 3.12+ - Linguagem base do projeto
* Pandas - Processamento de dados e conversão de formatos
* Openpyxl - Engine de suporte para criação de arquivos Excel
* Pathlib - Manipulação inteligente de caminhos de diretório

## Instalação e Dependências
Para rodar este projeto, você precisará ter o Python instalado e instalar as seguintes bibliotecas:

```bash
pip install pandas openpyxl
```

## Configuração de Caminhos
* O script está configurado para operar no Desktop.
* **Nota Importante:** No código, verifique a variável `diretorio_base` para o seu usuário.

### Estrutura esperada:

```text
BASE/
├── BASE.csv      # Seu arquivo original aqui
└── partição/     # Pasta criada automaticamente
```
## Como Executar
1. Coloque o seu arquivo `BASE.csv` na pasta indicada.
2. Abra o terminal ou CMD e execute:
```bash
python nome_do_arquivo.py
```
3. Siga as instruções no console:
   - **Linhas:** Informe o limite de registros por arquivo.
   - **Formato:** Digite `s` para CSV ou `n` para XLSX.
