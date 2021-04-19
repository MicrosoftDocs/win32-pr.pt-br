---
title: Unindo dados heterogêneos
description: As organizações típicas armazenam dados em vários bancos de dados heterogêneos. Os dados de recursos humanos podem ser armazenados em SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório. Outros dados podem ser armazenados em formatos proprietários.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314609"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="42e1d-105">Unindo dados heterogêneos</span><span class="sxs-lookup"><span data-stu-id="42e1d-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="42e1d-106">As organizações típicas armazenam dados em vários bancos de dados heterogêneos.</span><span class="sxs-lookup"><span data-stu-id="42e1d-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="42e1d-107">Os dados de recursos humanos podem ser armazenados em SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório.</span><span class="sxs-lookup"><span data-stu-id="42e1d-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="42e1d-108">Outros dados podem ser armazenados em formatos proprietários.</span><span class="sxs-lookup"><span data-stu-id="42e1d-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="42e1d-109">Com o, SQL Server 7,0, ADSI e o provedor de OLE DB, é possível unir dados de Active Directory aos dados no SQL Server e criar uma exibição dos dados associados.</span><span class="sxs-lookup"><span data-stu-id="42e1d-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="42e1d-110">**Para unir dados de Active Directory com dados de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="42e1d-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="42e1d-111">Execute o **SQL Query Analyzer** (iniciar \| programas \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="42e1d-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="42e1d-112">Faça logon no computador SQL Server.</span><span class="sxs-lookup"><span data-stu-id="42e1d-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="42e1d-113">Execute a seguinte linha (realçando-a e pressionando CTRL + E):</span><span class="sxs-lookup"><span data-stu-id="42e1d-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="42e1d-114">Nessa linha, os argumentos para o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="42e1d-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="42e1d-115">"ADSI" é o argumento de **servidor** , que será o nome desse servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="42e1d-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="42e1d-116">"Serviços Active Directorys" é o argumento **srvproduct** , que é o nome da fonte de dados OLE DB que você está adicionando como um servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="42e1d-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="42e1d-117">"ADSDSOObject" é o argumento de **\_ nome do provedor** e indica que você está usando o provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="42e1d-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="42e1d-118">"adsdatasource" é o **\_ argumento de fonte de dados**, que é o nome da fonte de dados conforme interpretado pelo provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="42e1d-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="42e1d-119">Agora você pode usar o servidor vinculado para acessar Active Directory do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="42e1d-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="42e1d-120">O exemplo a seguir executa uma consulta usando a instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="42e1d-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="42e1d-121">Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você acabou de criar e uma instrução de consulta.</span><span class="sxs-lookup"><span data-stu-id="42e1d-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="42e1d-122">A instrução de consulta contém os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="42e1d-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="42e1d-123">A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="42e1d-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="42e1d-124">Será necessário usar o nome de exibição LDAP para indicar quais dados você está procurando.</span><span class="sxs-lookup"><span data-stu-id="42e1d-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="42e1d-125">A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="42e1d-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="42e1d-126">A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="42e1d-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="42e1d-127">Neste exemplo, ele está procurando por usuários.</span><span class="sxs-lookup"><span data-stu-id="42e1d-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="42e1d-128">Digite e execute:</span><span class="sxs-lookup"><span data-stu-id="42e1d-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="42e1d-129">Você também pode usar o [DIALETO ADSI LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="42e1d-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="42e1d-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="42e1d-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="42e1d-131">No exemplo anterior, a consulta LDAP tem quatro partes:</span><span class="sxs-lookup"><span data-stu-id="42e1d-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="42e1d-132">" \<LDAP://DC=Fabrikam,DC=COM> " é o nome distinto do servidor de diretório a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="42e1d-132">"\<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="42e1d-133">"(& (objectCategory = Person) (objectClass = user))" é o filtro de pesquisa LDAP (consulte a [sintaxe do filtro de pesquisa](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="42e1d-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="42e1d-134">"Name, ADsPath" são os nomes (usando o formato de nome de exibição LDAP) dos atributos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="42e1d-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="42e1d-135">"Subtree" indica o [escopo](scope-of-query.md) da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="42e1d-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42e1d-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42e1d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42e1d-137">Criando e executando uma exibição</span><span class="sxs-lookup"><span data-stu-id="42e1d-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




