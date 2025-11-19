# 📊 Projeto de Modelagem Dimensional – Star Schema: Professores

## 🎯 Objetivo

Este projeto tem como finalidade construir um modelo dimensional (esquema em estrela) com foco na análise de dados relacionados aos **professores** de uma instituição acadêmica. A estrutura foi baseada em um diagrama relacional previamente fornecido.

---

## 🧠 Escopo da Análise

O modelo permite responder perguntas como:
- Quais disciplinas cada professor ministra?
- Em quais cursos os professores atuam?
- A qual departamento cada professor pertence?
- Qual a carga horária total por professor?
- Como essas atividades se distribuem ao longo do tempo?

---

## 🏗️ Estrutura do Star Schema

### 🟦 Tabela Fato: `Fato_Professor_Atividade`
Contém os eventos relacionados à atuação dos professores.

**Campos principais:**
- `Idfato_Professor`
- `Fk_professor_dimensao`
- `Fk_departamento`
- `Fk_curso`
- `Fk_disciplina`
- `Fk_data`
- `Carga_Horaria_Total`
- `Qtd_Disciplinas`

### 📘 Tabelas Dimensão

#### `Dim_Professor`
- `Id_professor`
- `Nome`
- `Sobrenome`
- `Idade`

#### `Dim_Departamento`
- `Id_dept`
- `Nome_dept`
- `Localizacao_depto`

#### `Dim_Curso`
- `Id_curso`
- `Nome_curso`
- `Nivel_curso`
- `Area_curso`

#### `Dim_Disciplina`
- `Id_disciplina`
- `Nome_disciplina`
- `Tipo_disciplina`
- `Carga_horaria`

#### `Dim_Data`
- `Id_data`
- `Ano`
- `Mes`
- `Dia`
- `Dia_da_semana`

---

## 🛠️ Tecnologias Utilizadas

- **MySQL Workbench** – modelagem relacional
- **Power BI / Excel / SQL** – para visualização e análise
- **Markdown** – documentação do projeto

## 📌 Visual do Modelo Star Schema

![Modelo Star Schema](./star%20schema%20final.png)

## 📌 Observações

- O modelo **não inclui dados de alunos**, conforme especificado no desafio.
- A granularidade da dimensão de tempo pode ser ajustada conforme a necessidade da análise (dia, mês, semestre, etc).

---

## ✍️ Autor

**Victor Biscaia**  
Salvador, Bahia – Brasil  
Projeto acadêmico de modelagem dimensional

---

