---
description: Usando scripts de regra de negócio no script para fornecer lógica de tempo de execução para verificar o acesso.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Qualificando o acesso com a lógica de negócios no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756383"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Qualificando o acesso com a lógica de negócios no script

Use scripts de regra de negócio para fornecer lógica de tempo de execução para verificar o acesso. Para obter mais informações sobre regras de negócio, consulte [regras de negócio](business-rules.md).

Para atribuir uma regra de negócio a uma tarefa, primeiro defina a propriedade [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) do objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa a tarefa. O script deve ser escrito usando a linguagem de programação Visual Basic Scripting Edition (VBScript) ou o software de desenvolvimento JScript. Depois de especificar a linguagem de script, defina a propriedade [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) do objeto **IAzTask** com uma representação de cadeia de caracteres do script.

Ao verificar o acesso de uma operação contida em uma tarefa que tem uma regra de negócio associada, o aplicativo deve criar duas matrizes do mesmo tamanho a serem passadas como os parâmetros *varParameterNames* e *VarParameterValues* do método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) . Para obter informações sobre como criar um contexto de cliente, consulte [estabelecendo um contexto de cliente no script](establishing-a-client-context-in-script.md).

O método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) cria um objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que é passado para o script de regra de negócio. Em seguida, o script define a propriedade [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) do objeto **AzBizRuleContext** . Um valor **true** indica que o acesso é concedido e um valor **false** indica que o acesso foi negado.

Um script de regra de negócio não pode ser atribuído a um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contido por um objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegado.

O exemplo a seguir mostra como usar um script de regra de negócio para verificar o acesso de um cliente a uma operação. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse repositório contenha um aplicativo chamado despesas, uma tarefa chamada enviar despesa e uma operação chamada UseFormControl.


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

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



