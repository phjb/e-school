<h1 align="center">
 📖 Dicionário de dados
</h1>

Dicionário de dados utilizado no sistema **E-School**.

## Sumário

1. [**Introdução**](#1-introducao)

2. [**Modelo Proposto**](2-modelo-proposto)
   
3. [**E-school**](3-e-school)   
   
    3.1. [Período](31---período)
    
    3.2. [Semestre](32---semestre)
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
  <tr>
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
  <tr>
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

  <table>
 <tr align="left">
    <th colspan="7">
      Entidade: <span style="font-weight: normal">semestre</span>
    </th>
  </tr>
  <tr>
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