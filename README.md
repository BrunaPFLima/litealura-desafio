<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:3C1361,50:6A0DAD,100:C77DFF&height=180&section=header&text=LiterAlura&fontSize=52&fontColor=ffffff&fontAlignY=36&desc=Cat%C3%A1logo%20de%20livros%20com%20Java%2C%20Spring%20e%20API%20Gutendex&descSize=17&descAlignY=58&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-21-6A0DAD?style=for-the-badge&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring%20Boot-3.2-9D4EDD?style=for-the-badge&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring%20Data%20JPA-9D4EDD?style=for-the-badge&logo=spring&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-C77DFF?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/API-Gutendex-C77DFF?style=for-the-badge&logo=bookstack&logoColor=white" />
</p>

---

## 💜 Sobre

O **LiterAlura** é um catálogo de livros interativo que roda no terminal. Ele busca livros na [API Gutendex](https://gutendex.com/) (acervo do Projeto Gutenberg), converte o JSON em objetos Java e salva livros e autores num banco **PostgreSQL**, permitindo consultas e estatísticas sobre o que foi registrado.

Projeto desenvolvido como **challenge da formação Back-end do programa Oracle Next Education (ONE)**, da Alura com a Oracle.

## ✨ Funcionalidades

```
1 - Buscar livro pelo título          → consulta a API e salva no banco
2 - Listar livros registrados
3 - Listar autores registrados
4 - Listar autores vivos em um determinado ano
5 - Listar livros em um determinado idioma
6 - Estatísticas de downloads de todos os livros
7 - Top 10 livros mais baixados
8 - Buscar autor por nome
0 - Sair
```

## 🧠 O que pratiquei aqui

- Consumo de API REST com **`HttpClient`** nativo do Java
- Conversão de JSON para **records** com **Jackson**
- Persistência com **Spring Data JPA** e relacionamento livro ↔ autor
- Consultas com **JPQL** (`@Query`) no repository
- Uso de `CommandLineRunner` pra rodar uma aplicação de console com Spring
- Configuração do banco via **variáveis de ambiente**

## 🚀 Como rodar

**Pré-requisitos:** Java 21 e PostgreSQL.

```bash
# 1. Clone o repositório
git clone https://github.com/BrunaPFLima/litealura-desafio.git
cd litealura-desafio/Challenge-Challenge-LiterAlura-master

# 2. Crie o banco
psql -U postgres -c "CREATE DATABASE liter_alura;"

# 3. Configure as variáveis de ambiente
export DB_HOST=localhost:5432
export DB_USER=postgres
export DB_PASSWORD=sua_senha

# 4. Rode — o menu aparece no terminal
./mvnw spring-boot:run
```

> No IntelliJ, também dá pra rodar direto a classe `LiterAluraApplication` (lembrando de configurar as variáveis de ambiente na configuração de execução).

## 🗂️ Estrutura

```
src/main/java/br/com/alura/literAlura
├── main/          # Menu interativo (Main.java)
├── model/         # Entidades Book e Author + records da API
├── repositoy/     # BookRepository (Spring Data JPA)
└── service/       # Consumo da API, conversão de JSON e regras de negócio
```

---

<p align="center">
  Feito com 💜 por <a href="https://github.com/BrunaPFLima">Bruna Lima</a> ·
  <a href="https://www.linkedin.com/in/bruna-lima-205360144/">LinkedIn</a>
</p>

<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:C77DFF,50:6A0DAD,100:3C1361&height=90&section=footer" />
</p>
