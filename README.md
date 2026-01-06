# 🏠 B&D Real Estate - Management System

Um sistema web para gerenciamento de imóveis, desenvolvido em dupla como parte de um trabalho acadêmico com finalidade de avaliação para nota semestral. O projeto permite realizar operações CRUD (Criar, Deletar, Atualizar, Consultar por ID e Consultar todos) sobre imóveis, utilizando **Java** com Spring Boot no backend; e **HTML, CSS e JavaScript** no frontend além do Banco de Dados MySQL.

---

## **Funcionalidades**
- **Criar Imóvel**: Adicionar um novo imóvel ao sistema.
- **Consultar Imóveis**: Listar todos os imóveis registrados no banco de dados.
- **Consultar por ID**: Exibir os detalhes de um imóvel específico utilizando seu ID.
- **Atualizar Imóvel**: Modificar as informações de um imóvel existente.
- **Deletar Imóvel**: Remover um imóvel do sistema.

---

## **Tecnologias Utilizadas**
- **Backend**: Java, Spring Boot e Maven
- **Frontend**: HTML, CSS e JavaScript
- **Ferramenta de Desenvolvimento**: IntelliJ IDEA
- **Ferramenta de Testes**: Postman
- **Banco de Dados**: MYSQL

---

## **Pré-requisitos**
Certifique-se de ter as seguintes ferramentas instaladas:
- Java 17+ 
- Maven
- Navegador Web (Google Chrome, Edge, etc.)
- Editor de texto (recomenda-se o IntelliJ IDEA)
- Banco de Dados MYSQL configurado com o código SQL disponivel no arquivo banco de dados.txt desse repositório.

---

## **Como Executar o Projeto**
### **Passo 1: Clone o Repositório**
Acesse o GitHub e clique em "Code > Download ZIP" ou use o comando:
```bash
git clone https://github.com/Diego251Fagundes/crud-imoveis.git
```

### **Passo 2: Criação do Banco de Dados MySQL**
1. No MySQL, crie um banco de dados com o nome imoveis. Execute o seguinte comando no seu painel SQL:
   ```sql
   CREATE DATABASE imoveis;
   ```
2. Importe o código SQL que está disponível no repositório para criar a tabela necessária. O arquivo SQL pode ser encontrado no arquivo `MySQL/imoveis.sql`.


### **Passo 3: Configure o Backend**
1. Abra o projeto backend no IntelliJ IDEA.
2. Configure o arquivo `application.properties` para apontar para o seu banco de dados:
   ```properties
    spring.application.name=imoveis_crud
    spring.datasource.url=jdbc:mysql://localhost:3306/imoveis
    spring.datasource.username= seu usuario, normalmente é "root"
    spring.datasource.password= sua senha 
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
   ```
3. Execute o backend utilizando o IntelliJ IDEA:
   - Clique com o botão direito na classe principal do Spring Boot (localizada em `imoveis_crud/src/main/java/imoveis_crud` com o nome `CrudImoveisApplication.java`) e selecione **"Run"**.
   - O servidor será iniciado e estará disponível em `http://localhost:8080`.

### **Passo 4: Configure o Frontend**
1. Abra a pasta do frontend no seu editor de texto ou IDE do Intellij.
2. Utilize um servidor local para rodar o frontend:
   - Caso use o **Live Server** no Visual Studio Code:
     - Clique com o botão direito no arquivo `index.html` e selecione **"Open with Live Server"**.
     - Acesse o projeto em `http://localhost:63342/m2/front-end-imovel/front-end/index.html`.
---

## **Estrutura do Projeto**
```plaintext
crud-imoveis/
├── imoveis_crud/           # Código do backend (Java e Spring Boot)
│   ├── .mvn/               # Arquivos de configuração do Maven Wrapper
│   ├── src/                # Código-fonte
│   └── pom.xml             # Configuração do Maven
│ 
├── frontend/                 # Código do frontend (HTML, CSS, JS)
│   ├── index.html            # Página inicial
│   ├── catalog.html          # Página de exibição do catálogo de imóveis
│   ├── consultar_imovel.html # Página para consultar um imóvel por ID
│   ├── createimovel.html     # Página para criar um novo imóvel
│   ├── edit.html             # Página para editar um imóvel existente
│   ├
│   ├── scripts/                       # Arquivos JavaScript
│   │   ├── alert.js                   # Lógica de alertas personalizados
│   │   ├── script_addimovel.js        # Lógica para adicionar imóvel
│   │   ├── script_catalog.js          # Lógica para catálogo de imóveis
│   │   ├── script_consultar_imovel.js # Lógica para consultar imóvel
│   │   └── script_edit.js             # Lógica para editar imóvel
│   ├
│   ├── styles/             # Arquivos de estilo CSS
│   │   ├── style.css       # Estilo principal da aplicação
│   │   └── images/         # Pasta para armazenar imagens do projeto
│   ├
├── MySQL/                  # Script SQL para configurar o banco de dados
│   └── imoveis.sql         # Código SQL para criação do banco de dados
│  
└── README.md               # Documentação do projeto

```

---

## **Colaboradores**
- **Bruno Shiraishi** *(https://github.com/BrunoShiraishi)*
- **Diego Fagundes** *(https://github.com/Diego251Fagundes)* 

---

## **Screenshots**

- **Tela Inicial:**
<img src="Screenshots/Inicio.png">

- **Tela de cadastro do imóvel:**
<img src="Screenshots/Cadastrar.png">


- **Lista de Imoveis Cadastrados:**
<img src="Screenshots/ConsultarTodos.png">
