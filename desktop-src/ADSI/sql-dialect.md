---
title: Dialeto SQL
description: O dialeto SQL, derivado da linguagem SQL, usa expressões legíveis para definir instruções de consulta.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- ADSI de dialeto SQL
- dialeto ADSI, dialeto SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754049"
---
# <a name="sql-dialect"></a>Dialeto SQL

O dialeto SQL, derivado da linguagem SQL, usa expressões legíveis para definir instruções de consulta. Use uma instrução de consulta SQL com as seguintes interfaces de pesquisa ADSI:

-   As interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , que são interfaces de automação que usam OLE DB.
-   [OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.

As instruções SQL exigem a sintaxe a seguir.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



A tabela a seguir lista as palavras-chave da instrução de consulta SQL.



| Palavra-chave  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Especifica uma lista separada por vírgulas de atributos a serem recuperados para cada objeto. Se você especificar \* , a consulta recuperará apenas o ADsPath de cada objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Especifica o ADsPath da base da pesquisa. Por exemplo, o ADsPath do contêiner usuários em um domínio Active Directory pode ser ' LDAP:Binding = Users, DC = Fabrikam, DC = COM '. Lembre-se de que o caminho está incluído em um par de aspas simples (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Uma palavra-chave opcional que especifica o filtro de consulta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Uma palavra-chave opcional que gera uma classificação do lado do servidor se o servidor oferecer suporte ao controle de classificação LDAP. O Active Directory dá suporte ao controle de classificação, mas pode afetar o desempenho do servidor, especialmente se o conjunto de resultados for grande. A lista de classificação é uma lista separada por vírgulas de atributos nos quais classificar. Lembre-se de que Active Directory dá suporte apenas a uma única chave de classificação. Você pode usar as palavras-chave ASC e DESC opcionais para especificar a ordem de classificação crescente ou decrescente; o padrão é Ascending. A palavra-chave ORDER BY substitui qualquer chave de classificação especificada com a propriedade "Sort on" do objeto de comando do ADO. |



 

> [!Note]  
> Nos casos em que um conjunto de caracteres MultiByte está sendo usado, se a pesquisa for executada pelo ADO com o dialeto SQL, uma barra invertida não poderá ser usada para escapar caracteres. Em vez disso, as sequências de escape listadas em [caracteres especiais](search-filter-syntax.md) devem ser usadas. Por exemplo, para uma instrução que usou a sintaxe "samAccountName = \( Test", que usa a barra invertida " \\ ", para escapar do parêntese de abertura, "(", em vez disso, você substituiria a barra invertida pelo caractere especial " \\ 28", da seguinte maneira: "sAMAccountName = \\ 28Test".

 

As instruções de consulta a seguir são exemplos de dialeto SQL no ADSI.

Para pesquisar todos os objetos de grupo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Para pesquisar todos os usuários cujo sobrenome começa com a letra H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



A gramática formal para consultas SQL é definida no exemplo de código a seguir. Todas as palavras-chave não diferenciam maiúsculas de minúsculas.


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



Não há suporte para junções internas do SQL pelo provedor de OLE DB Active Directory, mas você pode usar o SQL para unir dados SQL e Active Directory. Para obter mais informações, consulte [criando uma junção heterogênea entre SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe do filtro de pesquisa](search-filter-syntax.md)
</dt> <dt>

[Dialeto LDAP](ldap-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




