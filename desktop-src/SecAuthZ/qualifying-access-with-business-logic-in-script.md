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
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="687e8-103">Qualificando o acesso com a lógica de negócios no script</span><span class="sxs-lookup"><span data-stu-id="687e8-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="687e8-104">Use scripts de regra de negócio para fornecer lógica de tempo de execução para verificar o acesso.</span><span class="sxs-lookup"><span data-stu-id="687e8-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="687e8-105">Para obter mais informações sobre regras de negócio, consulte [regras de negócio](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="687e8-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="687e8-106">Para atribuir uma regra de negócio a uma tarefa, primeiro defina a propriedade [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) do objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="687e8-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="687e8-107">O script deve ser escrito usando a linguagem de programação Visual Basic Scripting Edition (VBScript) ou o software de desenvolvimento JScript.</span><span class="sxs-lookup"><span data-stu-id="687e8-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="687e8-108">Depois de especificar a linguagem de script, defina a propriedade [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) do objeto **IAzTask** com uma representação de cadeia de caracteres do script.</span><span class="sxs-lookup"><span data-stu-id="687e8-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="687e8-109">Ao verificar o acesso de uma operação contida em uma tarefa que tem uma regra de negócio associada, o aplicativo deve criar duas matrizes do mesmo tamanho a serem passadas como os parâmetros *varParameterNames* e *VarParameterValues* do método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="687e8-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="687e8-110">Para obter informações sobre como criar um contexto de cliente, consulte [estabelecendo um contexto de cliente no script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="687e8-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="687e8-111">O método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) cria um objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que é passado para o script de regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="687e8-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="687e8-112">Em seguida, o script define a propriedade [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) do objeto **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="687e8-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="687e8-113">Um valor **true** indica que o acesso é concedido e um valor **false** indica que o acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="687e8-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="687e8-114">Um script de regra de negócio não pode ser atribuído a um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contido por um objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegado.</span><span class="sxs-lookup"><span data-stu-id="687e8-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="687e8-115">O exemplo a seguir mostra como usar um script de regra de negócio para verificar o acesso de um cliente a uma operação.</span><span class="sxs-lookup"><span data-stu-id="687e8-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="687e8-116">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse repositório contenha um aplicativo chamado despesas, uma tarefa chamada enviar despesa e uma operação chamada UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="687e8-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



