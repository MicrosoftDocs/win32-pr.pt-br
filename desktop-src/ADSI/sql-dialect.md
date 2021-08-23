---
title: SQL Dialeto
description: O SQL dialeto, derivado do linguagem SQL, usa expressões que podem ser lidas por humanos para definir instruções de consulta.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL ADSI de dialeto
- dialeto ADSI, SQL dialeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7483a5e3785f410e6c2fd875122ba24618a82b70d1ed6dc9a85105ae4e8dcfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262046"
---
# <a name="sql-dialect"></a>SQL Dialeto

O SQL dialeto, derivado do linguagem SQL, usa expressões que podem ser lidas por humanos para definir instruções de consulta. Use uma SQL de consulta com as seguintes interfaces de pesquisa ADSI:

-   As [interfaces ActiveX ADO (Objeto](searching-with-activex-data-objects-ado.md) de Dados), que são interfaces de Automação que usam OLE DB.
-   [OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.

SQL instruções exigem a sintaxe a seguir.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



A tabela a seguir lista SQL de instrução de consulta.



| Palavra-chave  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Especifica uma lista separada por vírgulas de atributos a recuperar para cada objeto. Se você especificar \* , a consulta recuperará apenas o ADsPath de cada objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Especifica o ADsPath da base da pesquisa. Por exemplo, o ADsPath do contêiner Usuários em um domínio do Active Directory pode ser 'LDAP://CN=Users,DC=Fabrikam,DC=COM'. Esteja ciente de que o caminho está entre um par de aspas simples (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Uma palavra-chave opcional que especifica o filtro de consulta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Uma palavra-chave opcional que gera uma classificação do lado do servidor se o servidor dá suporte ao controle de classificação LDAP. O Active Directory dá suporte ao controle de classificação, mas pode afetar o desempenho do servidor, especialmente se o conjunto de resultados for grande. A lista de classificação é uma lista separada por vírgulas de atributos nos quais classificar. Esteja ciente de que o Active Directory dá suporte apenas a uma única chave de classificação. Você pode usar as palavras-chave OPC e DESC opcionais para especificar a ordem de classificação crescente ou decrescente; o padrão é crescente. A palavra-chave ORDER BY substitui qualquer chave de classificação especificada pela propriedade "Classificar" do objeto Comando ADO. |



 

> [!Note]  
> Nos casos em que um Conjunto de Caracteres MultiByte está sendo usado, se a pesquisa for executada pelo ADO com o dialeto SQL, uma faixa invertida não poderá ser usada para escapar caracteres. Em vez disso, as sequências de escape listadas [em Caracteres Especiais](search-filter-syntax.md) devem ser usadas. Por exemplo, para uma instrução que usou a sintaxe "samAccountName= Test", que usa a faixa invertida, " ", para escapar o parêntese aberto, "(", em vez disso, você substituiria a faixa invertida pelo caractere especial \( \\ " 28", da seguinte \\ forma: "samAccountName= \\ 28Test".

 

As instruções de consulta a seguir são exemplos de SQL dialeto no ADSI.

Para pesquisar todos os objetos de grupo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Para pesquisar todos os usuários cujo Sobrenome começa com a letra H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



A gramática formal para SQL consultas é definida no exemplo de código a seguir. Todas as palavras-chave não são sensíveis a maiúsculas e minúsculas.


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



SQL junções internas não são suportadas pelo provedor de OLE DB Active Directory, mas você pode usar o SQL para unir SQL dados do Active Directory. Para obter mais informações, consulte [Criando uma junção heterogênea entre o SQL Server e o Active Directory.](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de filtro de pesquisa](search-filter-syntax.md)
</dt> <dt>

[Dialeto LDAP](ldap-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




