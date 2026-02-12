# Contador e Classificador de Moedas Brasileiras

## Descrição do Projeto

Este projeto visa identificar, contar e somar o valor monetário de moedas em uma imagem utilizando técnicas clássicas de Processamento de Imagens, sem o uso de Inteligência Artificial ou bibliotecas de alto nível como OpenCV.

O projeto foi desenvolvido como trabalho final da disciplina Processamento de Imagens do curso Ciência da Computação da Universidade Federal de Sergipe (UFS).

---

## Técnicas Utilizadas

A solução foi implementada em Python utilizando estritamente as bibliotecas vistas em sala de aula:
- **scikit-image:** leitura de imagens, conversão de cores e Transformada de Hough Circular
- **NumPy:** manipulação matricial e operações lógicas com máscaras
- **Matplotlib:** visualização dos resultados

### Pipeline de Processamento

1. **Pré-processamento:** conversão para escala de cinza e aplicação do Filtro da Mediana para remoção de ruído.
2. **Detecção:** uso da Transformada de Hough Circular (`hough_circle`) para localizar as moedas.
3. **Classificação:** análise do raio (tamanho em pixels) e da cor média (RGB) interna de cada círculo detectado.

---

## Base de Dados Utilizada
As imagens utilizadas para teste e validação foram obtidas a partir do dataset público **Brazilian Coins** no Roboflow.
- **Link do Dataset:** [Brazilian Coins - Roboflow Universe](https://app.roboflow.com/davislira/brazilian-coins-r2vwk-4llen/images/rACRDQmwFlJueYPycMMr?queryText=&pageSize=50&startingIndex=350&browseQuery=true)
- Foram selecionadas 19 imagens variadas contendo diferentes quantidades, iluminações e disposições de moedas das duas famílias do Real.

---

## Estrutura do Repositório
O projeto está organizado da seguinte forma:

- `/notebooks`: Contém o código principal (`coin_counter.ipynb`) e testes de carga.
- `/images`: Imagens originais utilizadas para os testes.
- `/results`: Imagens processadas com o valor total calculado e identificação visual.
- `/counts`: Imagens com a numeração (indexação) de cada moeda para conferência.
- `/data_coins`: Documentação técnica das moedas (tamanhos e cores esperados).

---

## Como Executar

### 1️⃣ Clonar o Repositório

```bash
git clone https://github.com/DavisLira/brazilian-coin-counter.git
cd brazilian-coin-counter
```

---

### 2️⃣ Instalar o uv

O **uv** é um gerenciador moderno de ambientes virtuais e dependências para Python.
Ele **não é instalado via pip**.

#### Linux / macOS

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Windows (PowerShell)

```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

Verifique a instalação:

```bash
uv --version
```

---

### 3️⃣ Criar o Ambiente Virtual (Python 3.12)

Na raiz do projeto, execute:

```bash
uv venv --python 3.12
```

Isso criará o ambiente virtual na pasta `.venv`, utilizando o **Python 3.12**.

---

### 4️⃣ Ativar o Ambiente Virtual

#### Linux / macOS

```bash
source .venv/bin/activate
```

#### Windows (PowerShell)

```powershell
.venv\Scripts\activate
```

---

### 5️⃣ Instalar as Dependências

Com o ambiente virtual ativado:

```bash
uv sync
```

---

### 6️⃣ Executar o Projeto

Em seguida, execute o arquivo:

```
/notebooks/coin_counter.ipynb
```

As imagens de teste estão disponíveis na pasta:

```
/images
```

---

## Autores – Matrícula UFS

- **Davi Lira Santana** – 202300083319
- **Paulo Henrique Melo Rugani de Sousa** – 202300027919

---

## Link da Apresentação

[Vídeo youtube](https://youtu.be/cOOuj-NyMws)