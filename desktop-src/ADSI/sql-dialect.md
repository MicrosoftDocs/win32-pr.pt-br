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
# <a name="sql-dialect"></a><span data-ttu-id="0d719-105">Dialeto SQL</span><span class="sxs-lookup"><span data-stu-id="0d719-105">SQL Dialect</span></span>

<span data-ttu-id="0d719-106">O dialeto SQL, derivado da linguagem SQL, usa expressões legíveis para definir instruções de consulta.</span><span class="sxs-lookup"><span data-stu-id="0d719-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="0d719-107">Use uma instrução de consulta SQL com as seguintes interfaces de pesquisa ADSI:</span><span class="sxs-lookup"><span data-stu-id="0d719-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="0d719-108">As interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , que são interfaces de automação que usam OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0d719-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="0d719-109">[OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="0d719-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="0d719-110">As instruções SQL exigem a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d719-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="0d719-111">A tabela a seguir lista as palavras-chave da instrução de consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="0d719-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="0d719-112">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="0d719-112">Keyword</span></span>  | <span data-ttu-id="0d719-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d719-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d719-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="0d719-114">SELECT</span></span>   | <span data-ttu-id="0d719-115">Especifica uma lista separada por vírgulas de atributos a serem recuperados para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="0d719-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="0d719-116">Se você especificar \* , a consulta recuperará apenas o ADsPath de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="0d719-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0d719-117">FROM</span><span class="sxs-lookup"><span data-stu-id="0d719-117">FROM</span></span>     | <span data-ttu-id="0d719-118">Especifica o ADsPath da base da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0d719-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="0d719-119">Por exemplo, o ADsPath do contêiner usuários em um domínio Active Directory pode ser ' LDAP:Binding = Users, DC = Fabrikam, DC = COM '.</span><span class="sxs-lookup"><span data-stu-id="0d719-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="0d719-120">Lembre-se de que o caminho está incluído em um par de aspas simples (').</span><span class="sxs-lookup"><span data-stu-id="0d719-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0d719-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="0d719-121">WHERE</span></span>    | <span data-ttu-id="0d719-122">Uma palavra-chave opcional que especifica o filtro de consulta.</span><span class="sxs-lookup"><span data-stu-id="0d719-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0d719-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="0d719-123">ORDER BY</span></span> | <span data-ttu-id="0d719-124">Uma palavra-chave opcional que gera uma classificação do lado do servidor se o servidor oferecer suporte ao controle de classificação LDAP.</span><span class="sxs-lookup"><span data-stu-id="0d719-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="0d719-125">O Active Directory dá suporte ao controle de classificação, mas pode afetar o desempenho do servidor, especialmente se o conjunto de resultados for grande.</span><span class="sxs-lookup"><span data-stu-id="0d719-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="0d719-126">A lista de classificação é uma lista separada por vírgulas de atributos nos quais classificar.</span><span class="sxs-lookup"><span data-stu-id="0d719-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="0d719-127">Lembre-se de que Active Directory dá suporte apenas a uma única chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="0d719-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="0d719-128">Você pode usar as palavras-chave ASC e DESC opcionais para especificar a ordem de classificação crescente ou decrescente; o padrão é Ascending.</span><span class="sxs-lookup"><span data-stu-id="0d719-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="0d719-129">A palavra-chave ORDER BY substitui qualquer chave de classificação especificada com a propriedade "Sort on" do objeto de comando do ADO.</span><span class="sxs-lookup"><span data-stu-id="0d719-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="0d719-130">Nos casos em que um conjunto de caracteres MultiByte está sendo usado, se a pesquisa for executada pelo ADO com o dialeto SQL, uma barra invertida não poderá ser usada para escapar caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d719-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="0d719-131">Em vez disso, as sequências de escape listadas em [caracteres especiais](search-filter-syntax.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="0d719-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="0d719-132">Por exemplo, para uma instrução que usou a sintaxe "samAccountName = \( Test", que usa a barra invertida " \\ ", para escapar do parêntese de abertura, "(", em vez disso, você substituiria a barra invertida pelo caractere especial " \\ 28", da seguinte maneira: "sAMAccountName = \\ 28Test".</span><span class="sxs-lookup"><span data-stu-id="0d719-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="0d719-133">As instruções de consulta a seguir são exemplos de dialeto SQL no ADSI.</span><span class="sxs-lookup"><span data-stu-id="0d719-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="0d719-134">Para pesquisar todos os objetos de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d719-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="0d719-135">Para pesquisar todos os usuários cujo sobrenome começa com a letra H.</span><span class="sxs-lookup"><span data-stu-id="0d719-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="0d719-136">A gramática formal para consultas SQL é definida no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d719-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="0d719-137">Todas as palavras-chave não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0d719-137">All keywords are case-insensitive.</span></span>


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



<span data-ttu-id="0d719-138">Não há suporte para junções internas do SQL pelo provedor de OLE DB Active Directory, mas você pode usar o SQL para unir dados SQL e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d719-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="0d719-139">Para obter mais informações, consulte [criando uma junção heterogênea entre SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="0d719-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d719-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d719-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d719-141">Sintaxe do filtro de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0d719-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="0d719-142">Dialeto LDAP</span><span class="sxs-lookup"><span data-stu-id="0d719-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="0d719-143">Pesquisando com a interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0d719-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="0d719-144">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="0d719-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="0d719-145">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="0d719-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




