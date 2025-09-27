🫀 Machine Learning em Saúde: Estudo com SVM no Reconhecimento de Doenças Cardíacas

Este repositório contém os códigos, experimentos e documentação relacionados ao estudo apresentado no 3º UMC SUMMIT de Pesquisa, Inovação e Extensão, que investigou o uso de Support Vector Machine (SVM) no diagnóstico de doenças cardíacas a partir do dataset Heart Disease Cleveland.

📌 Objetivo

Avaliar o desempenho de diferentes configurações do classificador SVM no apoio ao diagnóstico de doenças cardíacas, explorando desde modelos lineares até ajustes otimizados via busca em grade.

⚙️ Metodologia

Base de dados: Heart Disease Cleveland

Pré-processamento:

Padronização das variáveis contínuas

Divisão treino/teste (80/20)

Modelagem:

Pipeline com normalização + SVM

Busca em grade (GridSearchCV) dos hiperparâmetros C, kernel e gamma

Validação cruzada KFold (10 folds)

Avaliação:

Acurácia média

Métricas da matriz de confusão (sensibilidade, especificidade, precisão, F1-score)

📊 Resultados

O modelo SVM linear obteve acurácia de ~85%.

O SVM com kernel radial apresentou melhor equilíbrio entre sensibilidade e especificidade.

O modelo otimizado atingiu acurácia média > 88%, com redução de falsos negativos, fator crítico em diagnósticos clínicos.

📂 Estrutura do Repositório
├── Summit2.ipynb        # Notebook principal com experimentos e análises
├── docs/                # Documentos relacionados ao artigo
│   └── Modelo RCUMC - Resumo simples.docx
├── data/                # Diretório sugerido para armazenamento do dataset
└── README.md            # Documentação do projeto

🚀 Como Executar

Clone este repositório:

git clone https://github.com/seuusuario/seu-repositorio.git
cd seu-repositorio


Instale as dependências:

pip install -r requirements.txt


Abra o notebook:

jupyter notebook Summit2.ipynb

📚 Tecnologias Utilizadas

Python 3.x

Scikit-learn

Pandas

NumPy

Matplotlib / Seaborn

🔑 Palavras-chave

machine learning · validação cruzada · SVM · diagnóstico médico · doenças cardíacas
