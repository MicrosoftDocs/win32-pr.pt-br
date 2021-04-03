---
title: Pesquisando objetos
description: Julie Bankert deve encontrar números de telefone para todos os gerentes de programa que trabalham no departamento 101. Ela pode criar um script que usa ADO e ADSI para fazer isso.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Pesquisando objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103823581"
---
# <a name="searching-for-objects"></a><span data-ttu-id="f680d-105">Pesquisando objetos</span><span class="sxs-lookup"><span data-stu-id="f680d-105">Searching for Objects</span></span>

<span data-ttu-id="f680d-106">Julie Bankert deve encontrar números de telefone para todos os gerentes de programa que trabalham no departamento 101.</span><span class="sxs-lookup"><span data-stu-id="f680d-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="f680d-107">Ela pode criar um script que usa ADO e ADSI para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f680d-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="f680d-108">Ao usar o provedor ADO para executar uma consulta, o conjunto de resultados retornará apenas os primeiros 1000 objetos.</span><span class="sxs-lookup"><span data-stu-id="f680d-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="f680d-109">Por esse motivo, é importante usar uma consulta paginada para que você possa recuperar todos os objetos no conjunto de resultados, desde que o serviço de diretório não tenha sido definido para limitar o número de itens em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f680d-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="f680d-110">Os conjuntos de retorno conterão o número de itens que você especificar no tamanho da página e os conjuntos paginados continuarão a ser retornados até que todos os itens no conjunto de resultados tenham sido retornados.</span><span class="sxs-lookup"><span data-stu-id="f680d-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



<span data-ttu-id="f680d-111">Para executar uma pesquisa de ADSI no Visual Basic ou em um ambiente de script, três componentes do ADO são necessários: **conexão**, **comando** e **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="f680d-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="f680d-112">O objeto **Connection** permite que você especifique o nome do provedor, credenciais alternativas, se aplicável e outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="f680d-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="f680d-113">O objeto **Command** permite que você especifique as preferências de pesquisa e a cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="f680d-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="f680d-114">Você deve associar o objeto de **conexão** a um objeto de **comando** antes da execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="f680d-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="f680d-115">Por fim, o objeto **Recordset** é usado para iterar o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f680d-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="f680d-116">A ADSI dá suporte a dois tipos de cadeias de caracteres de consulta ou dialetos.</span><span class="sxs-lookup"><span data-stu-id="f680d-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="f680d-117">O exemplo de código anterior usa o dialeto SQL.</span><span class="sxs-lookup"><span data-stu-id="f680d-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="f680d-118">Você também pode usar o dialeto LDAP.</span><span class="sxs-lookup"><span data-stu-id="f680d-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="f680d-119">A cadeia de caracteres de consulta de dialeto LDAP é baseada em [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (um RFC é um documento de solicitação de comentários, que é a base para o desenvolvimento de padrões LDAP).</span><span class="sxs-lookup"><span data-stu-id="f680d-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="f680d-120">O exemplo anterior pode ser traduzido para o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f680d-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="f680d-121">Por que a palavra "subárvore" no final da cadeia de caracteres?</span><span class="sxs-lookup"><span data-stu-id="f680d-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="f680d-122">No mundo do diretório, você pode especificar o escopo da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f680d-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="f680d-123">As opções são: "base", "OneLevel" e "Subtree".</span><span class="sxs-lookup"><span data-stu-id="f680d-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="f680d-124">"base" é usado para ler o objeto em si; "OneLevel" refere-se aos filhos imediatos, semelhante ao comando **dir** ; "Subtree" é usado para pesquisar vários níveis de profundidade ou para baixo (semelhante a **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="f680d-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="f680d-125">Com o dialeto SQL, você pode especificar o escopo na Propriedade Command, como no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f680d-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="f680d-126">Se o escopo não for especificado, por padrão ele usará uma pesquisa de subárvore.</span><span class="sxs-lookup"><span data-stu-id="f680d-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="f680d-127">Se você usar o C++, poderá usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) do ADSI.</span><span class="sxs-lookup"><span data-stu-id="f680d-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f680d-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f680d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f680d-129">Reorganização</span><span class="sxs-lookup"><span data-stu-id="f680d-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




