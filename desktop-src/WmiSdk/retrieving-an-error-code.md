---
description: Assim como acontece com todos os aplicativos, o WMI recebe códigos de erro do sistema operacional Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recuperando um código de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780325"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="560a3-103">Recuperando um código de erro</span><span class="sxs-lookup"><span data-stu-id="560a3-103">Retrieving an Error Code</span></span>

<span data-ttu-id="560a3-104">Assim como acontece com todos os aplicativos, o WMI recebe códigos de erro do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="560a3-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="560a3-105">Ao receber um código de erro, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="560a3-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="560a3-106">Examine o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="560a3-106">Look at the event log.</span></span>

    <span data-ttu-id="560a3-107">O WMI envia mensagens de erro para o serviço log de eventos que verifica os logs de eventos para ajudar a determinar a causa de um erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="560a3-108">Você pode usar as classes que o provedor de [log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) dá suporte para acessar logs de eventos programaticamente.</span><span class="sxs-lookup"><span data-stu-id="560a3-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="560a3-109">Recupere o código de erro normalmente.</span><span class="sxs-lookup"><span data-stu-id="560a3-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="560a3-110">O WMI dá suporte às técnicas padrão para recuperar códigos de erro, que são códigos de erro COM para C++ e objetos de erro nativos, como o [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))ou [**SWbemLastError**](swbemlasterror.md) , se o provedor fornecer informações de erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="560a3-111">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="560a3-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="560a3-112">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="560a3-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="560a3-113">Tratamento de um erro com o VBScript</span><span class="sxs-lookup"><span data-stu-id="560a3-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="560a3-114">Tratando um erro usando C++</span><span class="sxs-lookup"><span data-stu-id="560a3-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="560a3-115">Tratamento de um erro com o VBScript</span><span class="sxs-lookup"><span data-stu-id="560a3-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="560a3-116">Se uma chamada para o WMI por meio da API de script para WMI causar um erro, você terá as seguintes opções para acessar as informações de erro:</span><span class="sxs-lookup"><span data-stu-id="560a3-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="560a3-117">Use mecanismos de erro nativos da linguagem de script, por exemplo, no VBScript, use o [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) para dar suporte ao tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="560a3-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="560a3-118">Crie um objeto [**SWbemLastError**](swbemlasterror.md) para obter um relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="560a3-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="560a3-119">O script a seguir mostra o uso do [objeto de erro nativo (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="560a3-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="560a3-120">Quando um valor incorreto para o identificador de processo é fornecido, um erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="560a3-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="560a3-121">A propriedade **Description** do [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) está vazia ao se conectar ao WMI por meio do moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="560a3-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="560a3-122">No entanto, se você se conectar usando [**SWbemLocator**](swbemlocator.md), a descrição estará disponível.</span><span class="sxs-lookup"><span data-stu-id="560a3-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="560a3-123">A tabela a seguir lista as propriedades de [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="560a3-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="560a3-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="560a3-124">Property</span></span>                   | <span data-ttu-id="560a3-125">Contém</span><span class="sxs-lookup"><span data-stu-id="560a3-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="560a3-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="560a3-126">**Description**</span></span><br/> | <span data-ttu-id="560a3-127">Descrição de erro localizada e legível pelo homem.</span><span class="sxs-lookup"><span data-stu-id="560a3-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="560a3-128">**Número**</span><span class="sxs-lookup"><span data-stu-id="560a3-128">**Number**</span></span><br/>      | <span data-ttu-id="560a3-129">**HRESULT** RETORNADO pela API de script para WMI.</span><span class="sxs-lookup"><span data-stu-id="560a3-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="560a3-130">**Origem**</span><span class="sxs-lookup"><span data-stu-id="560a3-130">**Source**</span></span><br/>      | <span data-ttu-id="560a3-131">Identifica o objeto que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="560a3-132">O script a seguir mostra o uso de um objeto [**SWbemLastError**](swbemlasterror.md) para obter informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="560a3-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="560a3-133">Observe que nem todos os provedores fornecem informações para **SWbemLastError**.</span><span class="sxs-lookup"><span data-stu-id="560a3-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="560a3-134">Para obter mais informações sobre códigos de erro no script, consulte [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="560a3-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="560a3-135">Tratando um erro usando C++</span><span class="sxs-lookup"><span data-stu-id="560a3-135">Handling an Error Using C++</span></span>

<span data-ttu-id="560a3-136">Um aplicativo cliente WMI pode receber erros específicos de COM ou WMI.</span><span class="sxs-lookup"><span data-stu-id="560a3-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="560a3-137">Os erros de COM estão em conformidade com a estrutura de códigos de erro COM.</span><span class="sxs-lookup"><span data-stu-id="560a3-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="560a3-138">Todas as interfaces WMI podem retornar um erro específico COM, exceto as interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)e [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="560a3-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="560a3-139">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="560a3-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="560a3-140">As páginas de referência das interfaces WMI listam os códigos de erro WMI apropriados na seção códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="560a3-141">Um aplicativo cliente deve seguir os padrões COM para verificar o status e os códigos de retorno de erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="560a3-142">A principal diferença que você deve escolher é se deseja recuperar o código de erro de uma chamada síncrona, semisynchronous ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="560a3-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="560a3-143">**Para acessar mensagens de erro síncronas e semisynchronouss usando C++**</span><span class="sxs-lookup"><span data-stu-id="560a3-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="560a3-144">Recupere as informações de erro com uma chamada para a função com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="560a3-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="560a3-145">Certifique-se de chamar [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) imediatamente após um método de interface indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="560a3-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="560a3-146">Isso inclui qualquer um dos métodos [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) que você chama ao processar um processo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="560a3-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="560a3-147">Examine o objeto de erro COM retornado com uma chamada para o método [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="560a3-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="560a3-148">Certifique-se de especificar \_ o WbemClassObject de IID para o parâmetro *riid* na chamada [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="560a3-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="560a3-149">O método **QueryInterface** retorna uma instância de uma classe WMI, normalmente [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="560a3-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="560a3-150">O WMI não entrega o objeto de erro por meio do [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) para uma chamada assíncrona porque não há como saber quando ou em qual thread a chamada assíncrona ocorreu.</span><span class="sxs-lookup"><span data-stu-id="560a3-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="560a3-151">Portanto, o código só pode tratar erros específicos ou passar a falha de chamada por meio de COM.</span><span class="sxs-lookup"><span data-stu-id="560a3-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="560a3-152">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="560a3-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="560a3-153">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="560a3-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="560a3-154">**Para acessar mensagens de erro assíncronas usando C++**</span><span class="sxs-lookup"><span data-stu-id="560a3-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="560a3-155">Recupere o objeto de erro COM de sua implementação de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="560a3-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="560a3-156">O pseudocódigo a seguir mostra uma implementação típica de tratamento de erros para um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="560a3-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

