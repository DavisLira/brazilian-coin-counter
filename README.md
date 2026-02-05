# Contador e Classificador de Moedas Brasileiras

## Descrição do Projeto
Este projeto visa identificar, contar e somar o valor monetário de moedas em uma imagem utilizando técnicas clássicas de Processamento de Imagens, sem o uso de Inteligência Artificial ou bibliotecas de alto nível como OpenCV.

O projeto foi desenvolvido como trabalho final da disciplina Procressamento de Imagens do curso Ciência da Computação na UFS.

## Técnicas Utilizadas
A solução foi implementada em Python utilizando estritamente as bibliotecas vistas em sala de aula:
- **scikit-image:** Para leitura, conversão de cores e Transformada de Hough.
- **NumPy:** Para manipulação matricial e lógica de máscaras.
- **Matplotlib:** Para visualização dos resultados.

### Pipeline de Processamento:
1.  **Pré-processamento:** Conversão para escala de cinza e aplicação de Filtro da Mediana para remoção de ruído.
2.  **Detecção:** Uso da Transformada de Hough Circular (`hough_circle`) para encontrar as moedas.
3.  **Classificação:** Análise do raio (tamanho em pixels) e da cor média (RGB) interna de cada círculo detectado.

## Como Executar
1.  Clone este repositório.
2.  Abra o arquivo `/notebooks/projeto_moedas.ipynb` no Jupyter Notebook ou Google Colab.
3.  As imagens de teste estão na pasta `/images`.

## Autores - Matrícula UFS
Davi Lira Santana - 202300083319
Paulo Henrique Melo Rugani de Sousa - 202300027919

## Link da Apresentação
...