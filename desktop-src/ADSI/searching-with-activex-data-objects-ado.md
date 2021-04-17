---
title: Pesquisando com ActiveX Data Objects (ADO)
description: O modelo ADO (ActiveX Data Object) consiste em objetos listados na tabela a seguir.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, pesquisando com ADO
- Pesquisando com ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755452"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="e2623-105">Pesquisando com ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="e2623-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="e2623-106">O modelo ADO (ActiveX Data Object) consiste em objetos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2623-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="e2623-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="e2623-107">Object</span></span>         | <span data-ttu-id="e2623-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2623-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2623-109">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="e2623-109">**Connection**</span></span> | <span data-ttu-id="e2623-110">Uma conexão aberta com uma fonte de dados OLE DB como ADSI.</span><span class="sxs-lookup"><span data-stu-id="e2623-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="e2623-111">**Comando**</span><span class="sxs-lookup"><span data-stu-id="e2623-111">**Command**</span></span>    | <span data-ttu-id="e2623-112">Define um comando específico a ser executado na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e2623-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="e2623-113">**Parâmetro**</span><span class="sxs-lookup"><span data-stu-id="e2623-113">**Parameter**</span></span>  | <span data-ttu-id="e2623-114">Uma coleção opcional para quaisquer parâmetros a serem fornecidos ao objeto de comando.</span><span class="sxs-lookup"><span data-stu-id="e2623-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="e2623-115">**Registros**</span><span class="sxs-lookup"><span data-stu-id="e2623-115">**RecordSet**</span></span>  | <span data-ttu-id="e2623-116">Um conjunto de registros de uma tabela, objeto de comando ou sintaxe SQL.</span><span class="sxs-lookup"><span data-stu-id="e2623-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="e2623-117">Um conjunto de registros pode ser criado sem nenhum objeto de conexão subjacente.</span><span class="sxs-lookup"><span data-stu-id="e2623-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="e2623-118">**Campo**</span><span class="sxs-lookup"><span data-stu-id="e2623-118">**Field**</span></span>      | <span data-ttu-id="e2623-119">Uma única coluna de dados em um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="e2623-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="e2623-120">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="e2623-120">**Property**</span></span>   | <span data-ttu-id="e2623-121">Uma coleção de valores fornecidos pelo provedor para ADO.</span><span class="sxs-lookup"><span data-stu-id="e2623-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="e2623-122">**Erro**</span><span class="sxs-lookup"><span data-stu-id="e2623-122">**Error**</span></span>      | <span data-ttu-id="e2623-123">Contém dados sobre erros de acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="e2623-123">Contains data about data access errors.</span></span> <span data-ttu-id="e2623-124">Atualizado quando ocorre um erro em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="e2623-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="e2623-125">Para que o ADO se comunique com a ADSI, deve haver, pelo menos, dois objetos ADO: **Connection** e **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e2623-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="e2623-126">Esses objetos ADO servem para autenticar usuários e enumerar resultados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2623-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="e2623-127">Normalmente, você também usará um objeto de **comando** para manter uma conexão ativa, especificar parâmetros de consulta, como o tamanho da página e o escopo da pesquisa, e executar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="e2623-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="e2623-128">Para obter mais informações sobre a sintaxe do filtro de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e2623-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="e2623-129">O objeto de **conexão** carrega o provedor de OLE DB e valida as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2623-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="e2623-130">Em Visual Basic, chame a função **CreateObject** com "ADODB. Conexão "para criar uma instância de um objeto de **conexão** e, em seguida, defina a propriedade do **provedor** do objeto de **conexão** como" ADsDSOObject ".</span><span class="sxs-lookup"><span data-stu-id="e2623-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="e2623-131">ActiveX. Conexão "é o ProgID do objeto de **conexão** e" ADsDSOObject "é o nome do provedor de OLE DB no ADSI.</span><span class="sxs-lookup"><span data-stu-id="e2623-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="e2623-132">Se nenhuma credencial for especificada, as credenciais do usuário conectado no momento serão usadas.</span><span class="sxs-lookup"><span data-stu-id="e2623-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="e2623-133">O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** .</span><span class="sxs-lookup"><span data-stu-id="e2623-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="e2623-134">O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** .</span><span class="sxs-lookup"><span data-stu-id="e2623-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="e2623-135">O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** .</span><span class="sxs-lookup"><span data-stu-id="e2623-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="e2623-136">Lembre-se de que você deve incluir a biblioteca de tipos do ADO (msadoXX.dll) como uma das referências no projeto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e2623-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="e2623-137">Especifique os dados de autenticação de usuário definindo as propriedades do objeto de **conexão** .</span><span class="sxs-lookup"><span data-stu-id="e2623-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="e2623-138">A tabela a seguir lista as propriedades de autenticação de usuário com suporte ADSI.</span><span class="sxs-lookup"><span data-stu-id="e2623-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="e2623-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e2623-139">Property</span></span>           | <span data-ttu-id="e2623-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2623-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2623-141">"ID de usuário"</span><span class="sxs-lookup"><span data-stu-id="e2623-141">"User ID"</span></span>          | <span data-ttu-id="e2623-142">Uma cadeia de caracteres que identifica o usuário cujo contexto de segurança é usado ao executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="e2623-143">Para obter mais informações sobre o formato da cadeia de caracteres de nome de usuário, consulte [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="e2623-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="e2623-144">Se não for especificado, o padrão será o usuário conectado ou o usuário representado pelo processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="e2623-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="e2623-145">"Password"</span><span class="sxs-lookup"><span data-stu-id="e2623-145">"Password"</span></span>         | <span data-ttu-id="e2623-146">Uma cadeia de caracteres que especifica a senha do usuário identificada por "ID de usuário".</span><span class="sxs-lookup"><span data-stu-id="e2623-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e2623-147">"Criptografar senha"</span><span class="sxs-lookup"><span data-stu-id="e2623-147">"Encrypt Password"</span></span> | <span data-ttu-id="e2623-148">Um valor booliano que especifica se a senha é criptografada.</span><span class="sxs-lookup"><span data-stu-id="e2623-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="e2623-149">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="e2623-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e2623-150">"Sinalizador ADSI"</span><span class="sxs-lookup"><span data-stu-id="e2623-150">"ADSI Flag"</span></span>        | <span data-ttu-id="e2623-151">Um conjunto de sinalizadores da enumeração de enumeração de [**\_ \_ autenticação do ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) que especificam as opções de autenticação de associação.</span><span class="sxs-lookup"><span data-stu-id="e2623-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="e2623-152">O padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="e2623-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="e2623-153">O exemplo de código a seguir mostra como as propriedades são definidas antes da criação do objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="e2623-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="e2623-154">O segundo objeto ADO é o objeto **Command** .</span><span class="sxs-lookup"><span data-stu-id="e2623-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="e2623-155">O ProgID do objeto de **comando** é "ADODB. Command".</span><span class="sxs-lookup"><span data-stu-id="e2623-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="e2623-156">Esse objeto permite que você emita instruções de consulta e outros comandos para a ADSI usando a conexão ativa.</span><span class="sxs-lookup"><span data-stu-id="e2623-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="e2623-157">O objeto **Command** usa sua propriedade **ActiveConnection** para manter uma conexão ativa.</span><span class="sxs-lookup"><span data-stu-id="e2623-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="e2623-158">Ele também mantém a propriedade **CommandText** para manter instruções de consulta emitidas por um usuário.</span><span class="sxs-lookup"><span data-stu-id="e2623-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="e2623-159">As instruções de consulta são expressas no [dialeto SQL](sql-dialect.md) ou no [dialeto LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="e2623-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="e2623-160">Os exemplos de código a seguir mostram como criar um objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="e2623-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="e2623-161">No exemplo de código a seguir, inclua a biblioteca de tipos do ADO (msadoXX.dll) como uma das referências.</span><span class="sxs-lookup"><span data-stu-id="e2623-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="e2623-162">As opções de pesquisa para o objeto de **comando** são especificadas definindo a propriedade **Properties** .</span><span class="sxs-lookup"><span data-stu-id="e2623-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="e2623-163">A tabela a seguir lista as propriedades nomeadas aceitáveis para **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="e2623-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="e2623-164">Propriedade nomeada</span><span class="sxs-lookup"><span data-stu-id="e2623-164">Named property</span></span>      | <span data-ttu-id="e2623-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2623-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2623-166">Manipulador</span><span class="sxs-lookup"><span data-stu-id="e2623-166">"Asynchronous"</span></span>      | <span data-ttu-id="e2623-167">Um valor booliano que especifica se a pesquisa é síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e2623-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="e2623-168">O padrão é false (síncrono).</span><span class="sxs-lookup"><span data-stu-id="e2623-168">The default is False (synchronous).</span></span> <span data-ttu-id="e2623-169">Um bloco de pesquisa síncrono até que o servidor retorne todo o resultado, ou para uma pesquisa paginada, a página inteira.</span><span class="sxs-lookup"><span data-stu-id="e2623-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="e2623-170">Um bloco de pesquisa assíncrono até que uma linha dos resultados da pesquisa esteja disponível ou até que o tempo especificado pela propriedade "Timeout" decorra.</span><span class="sxs-lookup"><span data-stu-id="e2623-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="e2623-171">"Resultados do cache"</span><span class="sxs-lookup"><span data-stu-id="e2623-171">"Cache results"</span></span>     | <span data-ttu-id="e2623-172">Um valor booliano que especifica se o resultado deve ser armazenado em cache no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e2623-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="e2623-173">O padrão é **true**; O ADSI armazena em cache o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e2623-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="e2623-174">Desativar essa opção pode ser desejável para grandes conjuntos de resultados.</span><span class="sxs-lookup"><span data-stu-id="e2623-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="e2623-175">"Perseguir referências"</span><span class="sxs-lookup"><span data-stu-id="e2623-175">"Chase referrals"</span></span>   | <span data-ttu-id="e2623-176">Um valor dos anúncios buscam [**\_ \_ \_ enums de referências**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) que especifica como a pesquisa procura referências.</span><span class="sxs-lookup"><span data-stu-id="e2623-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="e2623-177">O padrão é **ADS \_ Chase \_ referências \_ nunca**. Para obter mais informações sobre essa propriedade, consulte [referências](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="e2623-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="e2623-178">"Somente nomes de coluna"</span><span class="sxs-lookup"><span data-stu-id="e2623-178">"Column Names Only"</span></span> | <span data-ttu-id="e2623-179">Um valor booliano que indica que a pesquisa deve recuperar somente o nome dos atributos aos quais os valores foram atribuídos.</span><span class="sxs-lookup"><span data-stu-id="e2623-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="e2623-180">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="e2623-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e2623-181">"Aliases Deref"</span><span class="sxs-lookup"><span data-stu-id="e2623-181">"Deref Aliases"</span></span>     | <span data-ttu-id="e2623-182">Um valor booliano que especifica se os aliases de objetos encontrados são resolvidos.</span><span class="sxs-lookup"><span data-stu-id="e2623-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="e2623-183">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="e2623-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e2623-184">"Tamanho da página"</span><span class="sxs-lookup"><span data-stu-id="e2623-184">"Page size"</span></span>         | <span data-ttu-id="e2623-185">Um valor inteiro que ativa a paginação e especifica o número máximo de objetos a serem retornados em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e2623-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="e2623-186">O padrão é nenhum tamanho de página.</span><span class="sxs-lookup"><span data-stu-id="e2623-186">The default is no page size.</span></span> <span data-ttu-id="e2623-187">Para obter mais informações, consulte [recuperando conjuntos de resultados grandes](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="e2623-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="e2623-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="e2623-188">"SearchScope"</span></span>       | <span data-ttu-id="e2623-189">Um valor da enumeração [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) que especifica o escopo da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="e2623-190">O padrão é **a \_ \_ subárvore de escopo ADS**.</span><span class="sxs-lookup"><span data-stu-id="e2623-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e2623-191">"Limite de tamanho"</span><span class="sxs-lookup"><span data-stu-id="e2623-191">"Size Limit"</span></span>        | <span data-ttu-id="e2623-192">Um valor inteiro que especifica o limite de tamanho para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="e2623-193">Por Active Directory, o limite de tamanho especifica o número máximo de objetos retornados.</span><span class="sxs-lookup"><span data-stu-id="e2623-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="e2623-194">O servidor para de Pesquisar quando o limite de tamanho é atingido e retorna os resultados acumulados.</span><span class="sxs-lookup"><span data-stu-id="e2623-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="e2623-195">O padrão é sem limite.</span><span class="sxs-lookup"><span data-stu-id="e2623-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="e2623-196">"Classificar em"</span><span class="sxs-lookup"><span data-stu-id="e2623-196">"Sort on"</span></span>           | <span data-ttu-id="e2623-197">Uma cadeia de caracteres que especifica uma lista separada por vírgulas de atributos a serem usados como chaves de classificação.</span><span class="sxs-lookup"><span data-stu-id="e2623-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="e2623-198">Essa propriedade funciona somente para servidores de diretório que dão suporte ao controle LDAP para classificação no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="e2623-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="e2623-199">O Active Directory dá suporte ao controle de classificação, mas pode afetar o desempenho do servidor, especialmente se o conjunto de resultados for grande.</span><span class="sxs-lookup"><span data-stu-id="e2623-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="e2623-200">Lembre-se de que Active Directory dá suporte apenas a uma única chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="e2623-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="e2623-201">O padrão é sem classificação.</span><span class="sxs-lookup"><span data-stu-id="e2623-201">The default is no sorting.</span></span> |
| <span data-ttu-id="e2623-202">"Limite de tempo"</span><span class="sxs-lookup"><span data-stu-id="e2623-202">"Time Limit"</span></span>        | <span data-ttu-id="e2623-203">Um valor inteiro que especifica o limite de tempo, em segundos, para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="e2623-204">Quando o limite de tempo é atingido, o servidor para de Pesquisar e retorna os resultados acumulados.</span><span class="sxs-lookup"><span data-stu-id="e2623-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="e2623-205">O padrão é sem limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="e2623-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="e2623-206">Cedido</span><span class="sxs-lookup"><span data-stu-id="e2623-206">"Timeout"</span></span>           | <span data-ttu-id="e2623-207">Um valor inteiro que especifica o valor de tempo limite do lado do cliente, em segundos.</span><span class="sxs-lookup"><span data-stu-id="e2623-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="e2623-208">Esse valor indica a hora em que o cliente aguarda os resultados do servidor antes de parar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="e2623-209">O padrão não é tempo limite.</span><span class="sxs-lookup"><span data-stu-id="e2623-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="e2623-210">O exemplo de código a seguir mostra como definir opções de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e2623-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="e2623-211">O terceiro objeto ADO é **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e2623-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="e2623-212">Você obtém esse objeto ao invocar o método **Execute** em um objeto **Command** .</span><span class="sxs-lookup"><span data-stu-id="e2623-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="e2623-213">A função principal do objeto **Recordset** é enumerar o conjunto de resultados e obter os dados.</span><span class="sxs-lookup"><span data-stu-id="e2623-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="e2623-214">O conjunto de resultados pode conter valores para atributos que têm valores únicos ou múltiplos.</span><span class="sxs-lookup"><span data-stu-id="e2623-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="e2623-215">Obter um atributo de valor único é simples, semelhante a obter o valor da coluna no banco de dados relacional, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2623-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="e2623-216">No entanto, obter um atributo com vários valores é mais desafiador.</span><span class="sxs-lookup"><span data-stu-id="e2623-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="e2623-217">Nesse caso, o **campo. Value** é uma matriz e você deve verificar o limite inferior e superior da matriz, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2623-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="e2623-218">O exemplo de código a seguir desabilita as contas de usuário em um servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="e2623-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="e2623-219">Para obter mais informações sobre o modelo de objeto ADO, consulte [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="e2623-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

