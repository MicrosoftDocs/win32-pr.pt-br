---
description: Chame o método IAzClientContext::AccessCheck para verificar se o cliente tem acesso a uma ou mais operações.
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Verificando o acesso do cliente aos recursos solicitados no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7393001c63f0a5b605870a8498e76231f0bf620a8c7e819a8c624eace565499a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906696"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Verificando o acesso do cliente aos recursos solicitados no script

Chame o [**método AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um [**objeto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para verificar se o cliente tem acesso a uma ou mais operações. Para obter informações sobre como criar **um objeto IAzClientContext,** consulte [Estabelecendo um contexto de cliente no script](establishing-a-client-context-in-script.md).

Um cliente pode ter associação em mais de uma função e uma operação pode ser atribuída a mais de uma tarefa, portanto, o Gerenciador de Autorização verifica todas as funções e tarefas. Se qualquer função à qual o cliente pertence contiver qualquer tarefa que contenha uma operação, o acesso a essa operação será concedido.

Para verificar o acesso de apenas uma única função à qual o cliente pertence, de definido a propriedade [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) do [**objeto IAzClientContext.**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)

Ao inicializar o repositório de políticas de autorização para verificação de acesso, você deve passar zero como o valor do parâmetro *lFlags* do método [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) do [**objeto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore)

Também é possível aplicar a lógica de negócios em tempo de operação para qualificar o acesso. Para obter informações sobre como qualificar o acesso com lógica de negócios, consulte [Qualificando o acesso com lógica de negócios no script](qualifying-access-with-business-logic-in-script.md).

O exemplo a seguir mostra como verificar o acesso de um cliente a uma operação. O exemplo presume que há um armazenamento de políticas XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse armazenamento contém um aplicativo chamado Expense e uma operação chamada UseFormControl.


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



 

 



