# MS671 - Introdução ao Aprendizado de Máquinas Profundo (UNICAMP)

[cite_start]Repositório dedicado aos projetos e estudos desenvolvidos na disciplina MS671 - Introdução ao Aprendizado de Máquinas Profundo, ministrada no Instituto de Matemática, Estatística e Computação Científica (IMECC) da Universidade Estadual de Campinas (UNICAMP)[cite: 1].

O foco do curso aborda desde os fundamentos teóricos até as aplicações práticas das arquiteturas de Deep Learning.

---

## Ementa da Disciplina

* **Fundamentos de Redes Neurais Profundas:** Arquiteturas lineares, funções de ativação e retropropagação.
* **Otimização de Hiperparâmetros, Regularização e Otimização:** Técnicas para mitigar overfitting, algoritmos de otimização e sintonia de parâmetros.
* **Tomadas de Decisão em Projetos de Machine Learning:** Análise de métricas de avaliação, diagnóstico de viés/variância e divisão de conjuntos de dados.
* **Redes Neurais Convolucionais e Visão Computacional:** Extração de características geométricas, convoluções, e tarefas de classificação, localização e detecção de objetos.
* **Modelos Sequenciais e Processamento de Linguagens Naturais:** Redes recorrentes e mecanismos de atenção.
* **Tópicos do Estado-da-Arte na Área:** Avanços recentes e evolução dos modelos profundos.

---

## Projeto 1: Reconhecimento de Objetos Usando YOLO

[cite_start]Este repositório contém o relatório completo e a implementação do Projeto 1, que consistiu na análise prática e matemática do algoritmo de detecção de objetos YOLOv3 (You Only Look Once)[cite: 3].

### Integrantes do Grupo
* [cite_start]Arthur Lourenço Narcizo da Silva [cite: 5]
* [cite_start]Danilo Antunes (RA269151) [cite: 6]
* [cite_start]Marcela Eduarda Marcelino Martins (RA236043) [cite: 7, 8]
* [cite_start]Vitor Macedo da Silva (RA204390) [cite: 10]

### Resumo do Trabalho
[cite_start]O projeto analisa o funcionamento do YOLOv3, focando em sua abordagem de regressão única para detecção em tempo real[cite: 24, 25, 38]. [cite_start]A rede utiliza o extrator de características Darknet-53 e realiza predições em múltiplas escalas para identificar objetos de diferentes tamanhos[cite: 38, 39, 42].

[cite_start]O modelo foi testado com imagens do cotidiano da UNICAMP (como o Restaurante Universitário, a Biblioteca Central e o ônibus circular 330), avaliando o comportamento empírico dos hiperparâmetros de limiar de confiança (Score Threshold) e supressão não-maximal (IoU Threshold) frente a desafios como oclusão e aglomeração[cite: 68, 97].

### Resultados Obtidos
[cite_start]A tabela abaixo resume o desempenho de detecção do modelo nas imagens do campus, utilizando os parâmetros de score em 0,5 e IoU em 0,4[cite: 69]:

| Imagem | Caixas Detectadas | Confiança Média | Falsos Positivos |
| :--- | :---: | :---: | :---: |
| Cachorro | 3 | 0,97 | 0 |
| Mesa | 10 | 0,75 | 0 |
| Livraria | 4 | 0,81 | 0 |
| IMECC | 10 | 0,76 | 1 |
| RU | 10 | 0,97 | 1 |
| Ônibus 330 | 2 | 1,00 | 0 |

[cite_start]*(Nota: Os dados e referências completas estão consolidados na Tabela 1 do relatório técnico)[cite: 88].*

---

## Como Executar no Google Colab

O desenvolvimento e a execução deste projeto foram realizados através do Google Colab, utilizando a integração nativa com o Google Drive para manipulação de arquivos pesados (pesos e datasets).

Para reproduzir os testes:

1. Baixe a pasta `deep_learning` contendo os scripts, notebooks e arquivos de pesos necessários.
2. Adicione essa pasta diretamente à raiz do seu Google Drive (`Meu Drive` / `MyDrive`).
3. Abra o notebook do projeto no Google Colab.
4. Execute a célula de montagem do drive para conceder permissão de acesso:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')

## Referências Principais

* [1] UNICAMP. Material de apoio da disciplina MS671 Aprendizado Profundo. IMECC, 2026.


* [2] REDMON, J.; FARHADI, A. YOLOv3: An Incremental Improvement. arXiv preprint arXiv:1804.02767, 2018.


* [3] LIN, T.-Y. et al. Microsoft COCO: Common Objects in Context. In: European conference on computer vision. Springer, Cham, 2014.

