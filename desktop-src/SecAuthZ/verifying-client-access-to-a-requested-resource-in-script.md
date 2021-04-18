---
description: 'Chame o método IAzClientContext:: AccessCheck para verificar se o cliente tem acesso a uma ou mais operações.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Verificando o acesso do cliente aos recursos solicitados no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755063"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="a37d8-103">Verificando o acesso do cliente aos recursos solicitados no script</span><span class="sxs-lookup"><span data-stu-id="a37d8-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="a37d8-104">Chame o método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para verificar se o cliente tem acesso a uma ou mais operações.</span><span class="sxs-lookup"><span data-stu-id="a37d8-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="a37d8-105">Para obter informações sobre como criar um objeto **IAzClientContext** , consulte [estabelecendo um contexto de cliente no script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="a37d8-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="a37d8-106">Um cliente pode ter associação em mais de uma função e uma operação pode ser atribuída a mais de uma tarefa, portanto, o Gerenciador de autorização verifica todas as funções e tarefas.</span><span class="sxs-lookup"><span data-stu-id="a37d8-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="a37d8-107">Se qualquer função à qual o cliente pertence contiver qualquer tarefa que contenha uma operação, o acesso a essa operação será concedido.</span><span class="sxs-lookup"><span data-stu-id="a37d8-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="a37d8-108">Para verificar o acesso apenas a uma única função à qual o cliente pertence, defina a propriedade [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) do objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="a37d8-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="a37d8-109">Ao inicializar o repositório de política de autorização para verificação de acesso, você deve passar zero como o valor do parâmetro *lFlags* do método [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) do objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="a37d8-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="a37d8-110">Também é possível aplicar a lógica de negócios em tempo de execução para qualificar o acesso.</span><span class="sxs-lookup"><span data-stu-id="a37d8-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="a37d8-111">Para obter informações sobre como qualificar o acesso com a lógica de negócios, consulte [qualificando o acesso com lógica de negócios no script](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="a37d8-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="a37d8-112">O exemplo a seguir mostra como verificar o acesso de um cliente a uma operação.</span><span class="sxs-lookup"><span data-stu-id="a37d8-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="a37d8-113">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse repositório contenha um aplicativo chamado despesas e uma operação chamada UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="a37d8-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



