---
title: Dialeto LDAP
description: O dialeto LDAP é um formato para instruções de consulta que usam a sintaxe de filtro de pesquisa LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI de dialeto LDAP
- dialeto ADSI, dialeto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822204"
---
# <a name="ldap-dialect"></a><span data-ttu-id="7d3b6-105">Dialeto LDAP</span><span class="sxs-lookup"><span data-stu-id="7d3b6-105">LDAP Dialect</span></span>

<span data-ttu-id="7d3b6-106">O dialeto LDAP é um formato para instruções de consulta que usam a [sintaxe de filtro de pesquisa LDAP](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b6-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="7d3b6-107">Use uma instrução de consulta LDAP com as seguintes interfaces de pesquisa ADSI:</span><span class="sxs-lookup"><span data-stu-id="7d3b6-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="7d3b6-108">As interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , que são interfaces de automação que usam OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="7d3b6-109">[OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="7d3b6-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), que é a interface C/C++ para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="7d3b6-111">Uma cadeia de caracteres de dialeto LDAP consiste em quatro partes separadas por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="7d3b6-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="7d3b6-112">Nome distinto base.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-112">Base distinguished name.</span></span> <span data-ttu-id="7d3b6-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7d3b6-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="7d3b6-114">Filtros de pesquisa LDAP.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-114">LDAP search filters.</span></span> <span data-ttu-id="7d3b6-115">Para obter mais informações sobre filtros de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b6-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="7d3b6-116">O nome de exibição LDAP dos atributos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="7d3b6-117">Vários atributos são separados por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="7d3b6-118">Especifica o escopo da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-118">Specifies the scope of the search.</span></span> <span data-ttu-id="7d3b6-119">Os valores válidos são "base", "OneLevel" e "Subtree".</span><span class="sxs-lookup"><span data-stu-id="7d3b6-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="7d3b6-120">O escopo especificado em uma cadeia de caracteres de consulta LDAP substitui qualquer escopo de pesquisa especificado pela propriedade "SearchScope" do objeto de comando ADO.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="7d3b6-121">Veja a seguir um exemplo de código do dialeto LDAP no ADSI que pesquisa todos os objetos na subárvore.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="7d3b6-122">Nem todas as opções de pesquisa (o tamanho da página de pesquisa, por exemplo) podem ser expressas no dialeto LDAP, portanto, você deve definir as opções antes que a execução real da consulta seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="7d3b6-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="7d3b6-123">Exemplo de código para executar uma consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="7d3b6-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="7d3b6-124">O exemplo de código a seguir mostra como usar uma consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="7d3b6-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="7d3b6-125">Para obter detalhes sobre a sintaxe de consulta, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b6-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d3b6-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d3b6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d3b6-127">Sintaxe do filtro de pesquisa</span><span class="sxs-lookup"><span data-stu-id="7d3b6-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="7d3b6-128">Dialeto SQL</span><span class="sxs-lookup"><span data-stu-id="7d3b6-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="7d3b6-129">Pesquisando com a interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="7d3b6-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="7d3b6-130">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="7d3b6-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="7d3b6-131">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="7d3b6-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




