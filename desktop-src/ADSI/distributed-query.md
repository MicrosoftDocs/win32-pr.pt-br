---
title: Consulta Distribuída
description: Como o ADSI é um provedor de OLE DB, ele pode participar da consulta distribuída introduzida no Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- ADSI de consultas, consulta distribuída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105755903"
---
# <a name="distributed-query"></a><span data-ttu-id="c3487-104">Consulta Distribuída</span><span class="sxs-lookup"><span data-stu-id="c3487-104">Distributed Query</span></span>

<span data-ttu-id="c3487-105">Como o ADSI é um provedor de OLE DB, ele pode participar da consulta distribuída introduzida no Microsoft SQL Server 7,0.</span><span class="sxs-lookup"><span data-stu-id="c3487-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="c3487-106">Estes são os possíveis cenários:</span><span class="sxs-lookup"><span data-stu-id="c3487-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="c3487-107">Unindo objetos de Active Directory com dados de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3487-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="c3487-108">Atualizando dados SQL de objetos Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c3487-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="c3487-109">Criando junções de três vias ou quatro vias com outros provedores de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c3487-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="c3487-110">Por exemplo, servidor de índice, SQL Server e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c3487-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="c3487-111">O provedor de OLE DB dá suporte a dois dialetos de comando, LDAP e SQL, para acessar o serviço de diretório e retornar resultados em um formulário de tabela que pode ser consultado com SQL Server consultas distribuídas.</span><span class="sxs-lookup"><span data-stu-id="c3487-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="c3487-112">**Para iniciar o analisador de consultas SQL**</span><span class="sxs-lookup"><span data-stu-id="c3487-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="c3487-113">Primeiro, abra o [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) no SQL Server que está vinculado ao serviço de diretório (consulte Criando um servidor vinculado).</span><span class="sxs-lookup"><span data-stu-id="c3487-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="c3487-114">Execute o **SQL Query Analyzer** (iniciar \| programas \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="c3487-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="c3487-115">Faça logon no computador SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3487-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="c3487-116">Insira a consulta SQL no painel do editor da janela de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3487-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="c3487-117">Execute a consulta pressionando F5.</span><span class="sxs-lookup"><span data-stu-id="c3487-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="c3487-118">As seções a seguir fornecem mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="c3487-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="c3487-119">Criando um servidor vinculado</span><span class="sxs-lookup"><span data-stu-id="c3487-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="c3487-120">Criando um logon SQL Server autenticado</span><span class="sxs-lookup"><span data-stu-id="c3487-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="c3487-121">Consultando o serviço de diretório</span><span class="sxs-lookup"><span data-stu-id="c3487-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="c3487-122">Criando um servidor vinculado</span><span class="sxs-lookup"><span data-stu-id="c3487-122">Creating a Linked Server</span></span>

<span data-ttu-id="c3487-123">Para configurar uma junção distribuída em um serviço de diretório do Windows 2000 Server, crie um servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="c3487-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="c3487-124">Para fazer isso, configure o mapeamento ADSI usando o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3487-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="c3487-125">Este procedimento vincula um nome a um nome de provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c3487-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="c3487-126">No exemplo a seguir, observe que há vários argumentos usados com o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :</span><span class="sxs-lookup"><span data-stu-id="c3487-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="c3487-127">"ADSI" é o argumento de **servidor** e será o nome desse servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="c3487-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="c3487-128">"Active Directory Services 2,5" é o argumento **srvproduct** , que é o nome da fonte de dados OLE DB que você está adicionando como um servidor vinculado.</span><span class="sxs-lookup"><span data-stu-id="c3487-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="c3487-129">"ADSDSOObject" é o argumento de **\_ nome do provedor** .</span><span class="sxs-lookup"><span data-stu-id="c3487-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="c3487-130">"adsdatasource" é o argumento de **\_ fonte de dados** , que é o nome da fonte de dados conforme interpretado pelo provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c3487-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="c3487-131">O comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3487-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="c3487-132">Para logons autenticados pelo Windows, o mapeamento automático é suficiente para acessar o diretório com SQL Server delegação de segurança.</span><span class="sxs-lookup"><span data-stu-id="c3487-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="c3487-133">Como o mapeamento automático é criado por padrão para servidores vinculados criados por meio do [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), nenhum outro mapeamento de logon é necessário.</span><span class="sxs-lookup"><span data-stu-id="c3487-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="c3487-134">Para os logons SQL Server autenticados, você pode configurar logons e senhas adequados para se conectar ao serviço de diretório usando o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3487-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="c3487-135">Quando possível, use a Autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3487-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="c3487-136">Criando um logon SQL Server autenticado</span><span class="sxs-lookup"><span data-stu-id="c3487-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="c3487-137">Se você preferir usar um logon SQL Server autenticado em vez da autenticação do Windows, adicione um logon ao servidor vinculado (consulte a seção anterior).</span><span class="sxs-lookup"><span data-stu-id="c3487-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="c3487-138">Para fazer isso, use o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3487-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="c3487-139">No exemplo a seguir, há vários argumentos que são usados com o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :</span><span class="sxs-lookup"><span data-stu-id="c3487-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="c3487-140">"ADSI" é o argumento **rmtsvrname** , que é o nome do servidor vinculado criado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="c3487-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="c3487-141">"Fabrikam \\ administrador" é o argumento **locallogin** , que é o logon no servidor local e pode ser o logon SQL Server ou um usuário do Windows NT.</span><span class="sxs-lookup"><span data-stu-id="c3487-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="c3487-142">"CN = Administrator, OU = Sales, DC = activeds, DC = Fabrikam, DC = com" é o argumento **rmtuser** , que é o nome de usuário que você usa para se conectar porque **useself** é **false**.</span><span class="sxs-lookup"><span data-stu-id="c3487-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="c3487-143">"Secret \* \* 2000" é o **rmtpassword**, que é a senha associada a **rmtuser**</span><span class="sxs-lookup"><span data-stu-id="c3487-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="c3487-144">O comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3487-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="c3487-145">Consultando o serviço de diretório</span><span class="sxs-lookup"><span data-stu-id="c3487-145">Querying the Directory Service</span></span>

<span data-ttu-id="c3487-146">Depois de criar um servidor vinculado, use uma instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar uma consulta ao serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="c3487-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="c3487-147">A consulta SQL a seguir cria uma tabela virtual para manter os resultados da consulta usando a instrução [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3487-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="c3487-148">A exibição que é criada é denominada "viewADContacts".</span><span class="sxs-lookup"><span data-stu-id="c3487-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="c3487-149">A primeira instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) define as informações que estão sendo consultadas do serviço de diretório e as mapeia para uma coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="c3487-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="c3487-150">As informações entre colchetes indicam os dados que são colocados na tabela virtual.</span><span class="sxs-lookup"><span data-stu-id="c3487-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="c3487-151">As informações que não estão entre colchetes indicam os dados recuperados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="c3487-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="c3487-152">Observe que as informações que estão sendo recuperadas do serviço de diretório devem ser referenciadas pelo seu nome de exibição LDAP.</span><span class="sxs-lookup"><span data-stu-id="c3487-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="c3487-153">A próxima instrução é a instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3487-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="c3487-154">Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você criou e uma instrução de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3487-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="c3487-155">A instrução de consulta contém os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="c3487-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="c3487-156">A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="c3487-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="c3487-157">Será necessário usar o nome de exibição LDAP para indicar quais dados você está procurando.</span><span class="sxs-lookup"><span data-stu-id="c3487-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="c3487-158">A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="c3487-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="c3487-159">A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3487-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="c3487-160">Neste exemplo, ele está procurando contatos.</span><span class="sxs-lookup"><span data-stu-id="c3487-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="c3487-161">A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) final é usada para escolher os resultados da exibição a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="c3487-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




