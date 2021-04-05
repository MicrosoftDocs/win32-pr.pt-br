---
description: Usando scripts de regra de negócio em C++ para fornecer lógica de tempo de execução para verificar o acesso.
ms.assetid: 058086ab-8ebd-4ff6-b552-8d3c19ae5d38
title: Qualificando o acesso com a lógica de negócios em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e176fb9cbb221fb52404e22c7ba61d272897082c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090753"
---
# <a name="qualifying-access-with-business-logic-in-c"></a><span data-ttu-id="c5a93-103">Qualificando o acesso com a lógica de negócios em C++</span><span class="sxs-lookup"><span data-stu-id="c5a93-103">Qualifying Access with Business Logic in C++</span></span>

<span data-ttu-id="c5a93-104">Use scripts de regra de negócio para fornecer lógica de tempo de execução para verificar o acesso.</span><span class="sxs-lookup"><span data-stu-id="c5a93-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="c5a93-105">Para obter mais informações sobre regras de negócio, consulte [regras de negócio](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="c5a93-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="c5a93-106">Para atribuir uma regra de negócio a uma tarefa, primeiro defina a propriedade [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) do objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c5a93-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="c5a93-107">O script deve estar em Visual Basic Scripting Edition ou JScript.</span><span class="sxs-lookup"><span data-stu-id="c5a93-107">The script must be in Visual Basic Scripting Edition or JScript.</span></span> <span data-ttu-id="c5a93-108">Depois de especificar a linguagem de script, defina a propriedade [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) do objeto **IAzTask** com uma representação de cadeia de caracteres do script.</span><span class="sxs-lookup"><span data-stu-id="c5a93-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="c5a93-109">Ao verificar o acesso de uma operação contida em uma tarefa que tem uma regra de negócio associada, o aplicativo deve criar duas matrizes do mesmo tamanho a serem passadas como os parâmetros *varParameterNames* e *VarParameterValues* do método [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="c5a93-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**IAzClientContext::AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method.</span></span> <span data-ttu-id="c5a93-110">Para obter informações sobre como criar um contexto de cliente, consulte [estabelecendo um contexto de cliente com o Gerenciador de autorização em C++](establishing-a-client-context-with-authorization-manager-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="c5a93-110">For information about creating a client context, see [Establishing a Client Context with Authorization Manager in C++](establishing-a-client-context-with-authorization-manager-in-c--.md).</span></span>

<span data-ttu-id="c5a93-111">O método [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) cria um objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que é passado para o script de regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="c5a93-111">The [**IAzClientContext::AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="c5a93-112">Em seguida, o script define a propriedade [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) do objeto **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="c5a93-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="c5a93-113">Um valor **true** indica que o acesso é concedido e um valor **false** indica que o acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="c5a93-113">A value of **TRUE** indicates that access is granted, and a value of **FALSE** indicates that access is denied.</span></span>

<span data-ttu-id="c5a93-114">Um script de regra de negócio não pode ser atribuído a um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contido por um objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegado.</span><span class="sxs-lookup"><span data-stu-id="c5a93-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="c5a93-115">O exemplo a seguir mostra como usar um script de regra de negócio para verificar o acesso de um cliente a uma operação.</span><span class="sxs-lookup"><span data-stu-id="c5a93-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="c5a93-116">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo chamado despesas, uma tarefa chamada enviar despesa e uma operação chamada UseFormControl, e que a variável hToken contém um token de cliente válido.</span><span class="sxs-lookup"><span data-stu-id="c5a93-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl, and that the variable hToken contains a valid client token.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
//  Void CheckAccess().
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    IAzTask* pTask = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    BSTR taskName = NULL;
    BSTR bizRule = NULL;
    BSTR bizRuleLanguage = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    VARIANT varParamName;
    VARIANT varParamValue;
    VARIANT nameString;
    VARIANT expenseAmount;
    void MyHandleError(char *s);

    VARIANT myVar;
    VariantInit(&myVar);

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
          &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Create a business rule for the Submit Expense task.

    //  Open the Submit Expense task.
    if(!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->OpenTask(taskName, myVar, &pTask);

    //  Assign a business rule to the task.

    //  Set the business rule language to VBScript.
    if(!(bizRuleLanguage = SysAllocString(L"VBScript")))
        MyHandleError("Could not allocate business rule language string.");
    hr = pTask->put_BizRuleLanguage(bizRuleLanguage);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not allocate business rule language string.");

    //  Create a BSTR with the business rule code.
    if(!(bizRule = SysAllocString(
        L"Dim Amount \n"
        L"AzBizRuleContext.BusinessRuleResult = FALSE \n"
        L"Amount = AzBizRuleContext.GetParameter(\"ExpAmount\") \n"
        L"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"
        )))
         MyHandleError("Could not allocate business rule string.");

    
    hr = pTask->put_BizRule(bizRule);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not assign business rule.");

    //  Save the new task data to the store.
    hr = pTask->Submit(0, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data.");

    //  Set up parameters for access check.

    //  Set up the object name.
    if (!(operationName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");

    //  Get the ID of the operation to check.
    hr = pApp->OpenOperation(operationName, myVar, &pOperation);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open operation.");

    hr = pOperation->get_OperationID(&operationID);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not get operation ID.");

    //  Create a SAFEARRAY for the operation ID.
    varOperationIdArray.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);

    //  Create an array of indexes.
    LONG* index = new LONG[1];
    index[0] = 0;

    //  Populate a SAFEARRAY with the operation ID.
    varOperationId.vt = VT_I4;
    varOperationId.lVal = operationID;

    hr = SafeArrayPutElement(varOperationIdArray.parray, index,
          &varOperationId);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not put operation ID in array.");
    
    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create business rule parameters.

    //  Create array of business rule parameter names.
    varParamName.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamName.vt = VT_ARRAY | VT_VARIANT;
    nameString.vt = VT_BSTR;
    nameString.bstrVal = SysAllocString(L"ExpAmount");
    SafeArrayPutElement(varParamName.parray, index, &nameString);

    //  Create array of business rule parameter values.
    varParamValue.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamValue.vt = VT_ARRAY | VT_VARIANT;
    expenseAmount.vt = VT_I4;
    expenseAmount.lVal = 100;  // access denied if 500 or more
    SafeArrayPutElement(varParamValue.parray, index, &expenseAmount);

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,                  // use default application scope
        varOperationIdArray,
        varParamName,
        varParamValue,
        myVar,
        myVar,
        myVar,
        &varResultsArray);

    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not complete access check.");

    hr = SafeArrayGetElement(varResultsArray.parray, index, &varResult);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not get result from array.");

    if (varResult.lVal == 0)
        printf("Access granted.\n");
    else
        printf("Access denied.\n");
    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pOperation->Release();
    pClientContext->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    SysFreeString(taskName);
    SysFreeString(bizRule);
    SysFreeString(bizRuleLanguage);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult);
    VariantClear(&varParamName);
    VariantClear(&varParamValue);
    VariantClear(&nameString);
    VariantClear(&expenseAmount);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



