# 📖 Dicionário de dados

Dicionário de dados utilizado no sistema **E-School**.

## Sumário

1. [**Introdução**](#1-introducao)

2. [**Modelo Proposto**](#2-modelo-proposto)
   
3. [**E-school**](#3-e-school)   
   
    3.1. [Período](#31---período)
    
    3.2. [Semestre](#32---semestre)
    
    3.3. [Turma](#33---turma)

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
    <td>id_semestre</td>
    <td>Identificar da entidade semestre a qual a turma pertence</td>
    <td>integer</td>
    <td>-</td>
    <td>-</td>
    <td>x</td>
    <td>-</td>
  </tr>
    <tr>
    <td>id_periodo</td>
    <td>Identificar da entidade período a qual a turma pertence</td>
    <td>integer</td>
    <td>-</td>
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
