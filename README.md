## 🫀 **Machine Learning em Saúde: : Estudo com SVM no Reconhecimento de Doenças** 

Este repositório contém os códigos, experimentos e documentação relacionados ao estudo apresentado no 3º UMC SUMMIT de Pesquisa, Inovação e Extensão, que investigou o uso de Support Vector Machine (SVM) no diagnóstico de doenças cardíacas a partir do dataset Heart Disease Cleveland.

### 📌 **Objetivo**

Avaliar o desempenho de diferentes configurações do classificador SVM no apoio ao diagnóstico de doenças cardíacas, compararando o desempenho do classificador SVM em dois esquemas de validação: KFold-10 (baseline comum a todos os grupos) e StratifiedKFold-8.

### ⚙️ **Metodologia**

- Base de dados: Heart Disease Cleveland.

**1. Pré-processamento**
- Importação e visualização do Dataframe
- Tratamento de valores ausentes.
- Divisão dos dados em treino/teste (80/20)

**2. Modelagem**
- Pipeline com padronização StandardScaler + SVM (Support Vector Machine)
- Busca em grade (GridSearchCV) dos hiperparâmetros C, kernel e gamma
- Parâmetros a serem testados:
    - C = [0.01, 0.1, 1, 10, 100]
    - kernel = [linear, não-lineares]
    - gamma = [scale, 0.01, 0.001]

**3. Validação**
- Aplicado o KFold-10.
- Em seguida, foi aplicado o StratifiedKFold-8.
- Por fim, foi comparado o desempenho dos dois modelos entre si.

**4. Avaliação**
- Foram avaliadas diferentes configurações do classificador SVM utilizando validação cruzada com KFold=10 e StratifiedKFold=8.
- KFold=10: A melhor combinação de hiperparâmetros foi {'svm__C': 1, 'svm__gamma': 0.01, 'svm__kernel': 'rbf'}, resultando em um score de validação de 0.87 ± 0.06 e acurácia no teste de 73%.
- StratifiedKFold=8: A melhor combinação foi {'svm__C': 0.1, 'svm__gamma': 'scale', 'svm__kernel': 'sigmoid'}, com score de validação de 0.87 ± 0.05 e acurácia no teste também de 73%. Podemos observar que o desvio padrão foi ligeiramente menor em comparação ao KFold-10.

📂 **Estrutura do Repositório**
├── Summit2.ipynb        # Notebook principal com experimentos e análises
├── docs/                # Documentos relacionados ao artigo
│   └── Modelo RCUMC - Resumo simples.docx
├── data/                # Diretório sugerido para armazenamento do dataset
└── README.md            # Documentação do projeto

**🚀 Como Executar**
Clone este repositório:
- git clone [https://github.com/Eddie-Costa/SVM-HEART-CLEVELAND.git]
cd seu-repositorio
- Instale as dependências:
- pip install -r requirements.txt

**Abra o notebook:**
- jupyter notebook Summit2.ipynb

**📚 Tecnologias Utilizadas**
- Python 3.x
- Scikit-learn
- Pandas
- NumPy
- Matplotlib / Seaborn

**🔑 Palavras-chave**
machine learning · validação cruzada · SVM · diagnóstico médico · doenças cardíacas
