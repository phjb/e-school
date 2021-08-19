# 📖 Dicionário de dados

Dicionário de dados utilizado no sistema **E-School**.

## Sumário

1. [**Introdução**](#1-introducao)

2. [**Modelo Proposto**](#2-modelo-proposto)
3. [**E-school**](#3-e-school)

   3.1. [Período](#31---período)

   3.2. [Semestre](#32---semestre)

   3.3. [Turma](#33---turma)

   3.4. [Curso](#34---curso)

   3.5. [Relação entre Curso e Turma](#35---relação-entre-curso-e-turma)
   
   3.6. [Disciplina](#36---disciplina)

   3.7. [Relação entre Disciplina e Curso](#37---relação-entre-disciplina-e-curso)

   3.8. [Função](#38---função)

   3.9. [Funcionário](#39---funcionário)

   3.10. [Relação entre Funcionário e Função](#310---relação-entre-funcionário-e-função)

   3.11. [Relação entre Funcionário e Disciplina](#311---relação-entre-funcionário-e-disciplina)

   3.12. [Relação entre Funcionário e Curso](#312---relação-entre-funcionário-e-curso)

## 1. Introdução

O Dicionário de Dados é uma listagem organizada de todos os elementos de dados que são pertinentes ao sistema, com definições precisas e rigorosas.  
 Tem como objetivo, transcrever de forma clara e consistente as informações sobre todos os objetos do modelo, para que tanto os usuários como o analista de sistemas tenham uma compreensão comum. Sendo assim, o dicionário de dados é feito de forma textual, contendo explicações por vezes difíceis de incluir no diagrama.

## 2. Modelo Proposto

Segue abaixo, o modelo proposto para criação do dicionário de dados: <br /> **Exemplo da entidade**: Descrição da entidade do Banco de Dados.

<table>
  <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">Exemplo da entidade</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>Nome do Campo da entidade.</td>
    <td>Descrição do Campo.</td>
    <td>Tipo de Dados</td>
    <td>Quantidade de caracteres</td>
    <td>É chave primária</td>
    <td>É Chave estrangeira</td>
    <td>Aceita nulo</td>
  </tr>
</table>
<br>

No próximo tópico, estamos explicando todas as entidades do modelo de entidade relacionamento e seus atributos, onde:

- **Entidade**: Nome da entidade que foi definida no Modelo entidade relacionamento (MER).
- **Atributo**: Nome dos atributos das entidades.
- **Descrição**: Descrição dos atributos das entidades.
- **Tipo dados**: Nome do tipo de dados do atributo.
- **Tamanho**: Quantidade de caracteres que serão necessários para armazenar o seu conteúdo.
- **PK**: Chave primária da entidade.
- **FK**: Chave secundária da entidade.
- **Null**: Indica os campos que podem ser nulos.

## 3. E-School

> _O esquema a ser utilizado na base de dados será `schoolar`_.

### 3.1 - Período

Entidade responsável por armazenar os dados do período da turma.

  <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">periodo</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código que definirá o período</td>
    <td>varchar</td>
    <td>20</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>descricao</td>
    <td>Descrição do código que definirá o período</td>
    <td>varchar</td>
    <td>100</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

### 3.2 - Semestre

Entidade responsável por armazenar os dados do semestre da turma.

> _Espera-se que a turma tenha até 10 semestres._

  <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">semestre</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código que definirá o semestre</td>
    <td>varchar</td>
    <td>20</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>descricao</td>
    <td>Descrição do código que definirá o semestre</td>
    <td>varchar</td>
    <td>100</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

### 3.3 - Turma

Entidade responsável por armazenar os dados da turma.

 <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">turma</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>id</td>
    <td>Identificador único da entidade</td>
    <td>serial</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
   <tr>
    <td>nome</td>
    <td>Nome da turma</td>
    <td>varchar</td>
    <td>30</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código da turma</td>
    <td>varchar</td>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>data_inicio</td>
    <td>Data de início da turma</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>data_fim</td>
    <td>Data de encerramento da turma</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>x</td>
  </tr>
   <tr>
    <td>numero_vaga</td>
    <td>Número de vagas da turma</td>
    <td>integer</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>semestre</td>
    <td>Identificador da entidade semestre a qual a turma pertence</td>
    <td>varchar</td>
    <td>20</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>periodo</td>
    <td>Identificador da entidade período a qual a turma pertence</td>
    <td>varchar</td>
    <td>20</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </tr>
    <tr>
    <td>ativa</td>
    <td>Flag para identificar se a turma está ativo</td>
    <td>boolean</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
    <tr>
    <td>data_cadastro</td>
    <td>Data de cadastro da turma</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>data_alteracao</td>
    <td>Data de alteração da turma</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>x</td>
  </tr>
  </table>


### 3.4 - Curso

Entidade responsável por armazenar os dados do curso.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">curso</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
    <tr>
    <td>id</td>
    <td>Identificador único da entidade</td>
    <td>serial</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>nome</td>
    <td>Nome do curso</td>
    <td>varchar</td>
    <td>30</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código do curso</td>
    <td>varchar</td>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>carga_horaria</td>
    <td>Carga horária do curso</td>
    <td>integer</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
    <tr>
    <td>ativo</td>
    <td>Flag para identificar se o curso está ativo</td>
    <td>boolean</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>data_cadastro</td>
    <td>Data de cadastro do curso</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>data_alteracao</td>
    <td>Data de alteração do curso</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>x</td>
  </tr>
   <tr>
    <td>data_exclusao</td>
    <td>Data de exclusão do curso</td>
    <td>timestamp</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>x</td>
  </tr>
</table>

### 3.5 - Relação entre Curso e Turma

Entidade responsável por armazenar a relação entre curso e turma.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">rel_curso_turma</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>id_curso</td>
    <td>Identificador único da entidade curso</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>id_turma</td>
    <td>Identificador único da entidade turma</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </table>

### 3.6 - Disciplina

Entidade responsável por armazenar os dados da disciplina.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">disciplina</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>id</td>
    <td>Identificador único da entidade</td>
    <td>serial</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código da disciplina</td>
    <td>varchar</td>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>carga_horaria</td>
    <td>Carga horária da disciplina</td>
    <td>integer</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  </table>


### 3.7 - Relação entre Disciplina e Curso

Entidade responsável por armazenar a relação entre disciplina e curso.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">rel_disciplina_curso</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
    <tr>
    <td>id_disciplina</td>
    <td>Identificador único da entidade disciplina</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  <tr>
    <td>id_curso</td>
    <td>Identificador único da entidade curso</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </table>

### 3.8 - Função

Entidade responsável por armazenar os dados da função do funcionário.

  <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">funcao</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>codigo</td>
    <td>Código que definirá a função</td>
    <td>varchar</td>
    <td>20</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>descricao</td>
    <td>Descrição do código que definirá a função</td>
    <td>varchar</td>
    <td>100</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

### 3.9 - Funcionário

Entidade responsável por armazenar os dados do funcionário.

  <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">funcionario</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>id</td>
    <td>Identificador único da entidade</td>
    <td>serial</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
    <td>-</td>
  </tr>
    <tr>
    <td>pessoa</td>
    <td>Identificador único da entidade pessoa</td>
    <td>varchar</td>
    <td>40</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
  </tr>
   <tr>
    <td>funcao</td>
    <td>Identificador único da entidade função</td>
    <td>varchar</td>
    <td>20</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
  </tr>
  <tr>
    <td>contrato</td>
    <td>Código/Número do contrato do funcionário</td>
    <td>varchar</td>
    <td>20</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>


### 3.10 - Relação entre Funcionário e Função

Entidade responsável por armazenar a relação entre funcionário e função.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">rel_funcionario_funcao</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>funcionario</td>
    <td>Identificador único da entidade funcionário</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>funcao</td>
    <td>Identificador único da entidade função</td>
    <td>varchar</td>
    <td>20</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </table>

### 3.11 - Relação entre Funcionário e Disciplina

Entidade responsável por armazenar a relação entre funcionário e disciplina.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">rel_funcionario_disciplina</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>funcionario</td>
    <td>Identificador único da entidade funcionário</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>disciplina</td>
    <td>Identificador único da entidade disciplina</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </table>

### 3.12 - Relação entre Funcionário e Curso

Entidade responsável por armazenar a relação entre funcionário e curso.

<table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">rel_funcionario_curso</span>
    </th>
  </tr>
  <tr align="left">
    <th>Atributo</th>
    <th>Descrição</th>
    <th>Tipo dados</th>
    <th>Tamanho</th>
    <th>PK</th>
    <th>FK</th>
    <th>Null</th>
  </tr>
  <tr>
    <td>funcionario</td>
    <td>Identificador único da entidade funcionário</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>curso</td>
    <td>Identificador único da entidade curso</td>
    <td>varchar</td>
    <td>40</td>
    <td>x</td>
    <td>x</td>
    <td>-</td>
  </tr>
  </table>

  