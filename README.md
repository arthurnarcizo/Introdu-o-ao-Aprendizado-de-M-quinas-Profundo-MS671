# MS671 - Introdução ao Aprendizado de Máquinas Profundo (UNICAMP)

Repositório dedicado aos projetos e estudos desenvolvidos na disciplina MS671 - Introdução ao Aprendizado de Máquinas Profundo, ministrada no Instituto de Matemática, Estatística e Computação Científica (IMECC) da Universidade Estadual de Campinas (UNICAMP).

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

Este repositório contém o relatório completo e a implementação do Projeto 1, que consistiu na análise prática e matemática do algoritmo de detecção de objetos YOLOv3 (You Only Look Once).

### Integrantes do Grupo
* Arthur Lourenço Narcizo da Silva
* Danilo Antunes (RA269151)
* Marcela Eduarda Marcelino Martins (RA236043)
* Vitor Macedo da Silva (RA204390)

### Resumo do Trabalho
O projeto analisa o funcionamento do YOLOv3, focando em sua abordagem de regressão única para detecção em tempo real. A rede utiliza o extrator de características Darknet-53 e realiza predições em múltiplas escalas para identificar objetos de diferentes tamanhos.

O modelo foi testado com imagens do cotidiano da UNICAMP (como o Restaurante Universitário, a Biblioteca Central e o ônibus circular 330), avaliando o comportamento empírico dos hiperparâmetros de limiar de confiança (Score Threshold) e supressão não-maximal (IoU Threshold) frente a desafios como oclusão e aglomeração.

### Resultados Obtidos
A tabela abaixo resume o desempenho de detecção do modelo nas imagens do campus, utilizando os parâmetros de score em 0,5 e IoU em 0,4:

| Imagem | Caixas Detectadas | Confiança Média | Falsos Positivos |
| :--- | :---: | :---: | :---: |
| Cachorro | 3 | 0,97 | 0 |
| Mesa | 10 | 0,75 | 0 |
| Livraria | 4 | 0,81 | 0 |
| IMECC | 10 | 0,76 | 1 |
| RU | 10 | 0,97 | 1 |
| Ônibus 330 | 2 | 1,00 | 0 |

*(Nota: Os dados e referências completas estão consolidados na Tabela 1 do relatório técnico).*

---

## Como Executar o Projeto

Por motivos de desempenho e limitações de armazenamento do Git, os arquivos de pesos pré-treinados e datasets grandes não foram adicionados a este repositório.

1. Clone este repositório para a sua máquina local.
2. Faça o download do arquivo de pesos pré-treinados do YOLOv3 (`yolov3.weights`) através do [site oficial do autor do modelo](https://pjreddie.com/media/files/yolov3.weights).
3. Salve o arquivo baixado na pasta raiz do projeto (ou dentro do diretório indicado nos scripts de execução).
4. Certifique-se de ter as dependências do projeto instaladas antes de rodar os scripts de inferência.

---

## Estrutura do Repositório

```bash
├── .gitignore               # Ignora arquivos auxiliares do LaTeX e arquivos pesados de dados/pesos
├── README.md                # Descrição geral do repositório
└── Projeto_1_YOLO/
    ├── Trabalho_MS671.pdf   # Relatório final entregue em PDF
    ├── src/                 # Código-fonte da implementação do algoritmo
    └── document/            # Arquivos fonte .tex e imagens do relatório
