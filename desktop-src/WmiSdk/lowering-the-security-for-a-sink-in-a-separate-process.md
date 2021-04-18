---
description: Instrumentação de Gerenciamento do Windows (WMI) pode criar o coletor para receber retornos de chamada assíncronos para um aplicativo cliente em um processo separado.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Reduzindo a segurança de um coletor em um processo separado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807199"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="bb1a3-103">Reduzindo a segurança de um coletor em um processo separado</span><span class="sxs-lookup"><span data-stu-id="bb1a3-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="bb1a3-104">Instrumentação de Gerenciamento do Windows (WMI) pode criar o coletor para receber retornos de chamada assíncronos para um aplicativo cliente em um processo separado.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="bb1a3-105">O processo separado é Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="bb1a3-106">Use a interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="bb1a3-107">**IWbemUnsecuredApartment** permite que você controle se Unsecapp.exe autentica retornos de chamada para o coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="bb1a3-108">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="bb1a3-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="bb1a3-109">Você pode reduzir a segurança nesse processo e o WMI pode acessar o coletor sem restrição.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="bb1a3-110">Para ajudar com essa técnica, o WMI fornece o Unsecapp.exe processo para funcionar como o processo separado.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="bb1a3-111">Você pode hospedar Unsecapp.exe com uma chamada para a interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="bb1a3-112">A interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permite que um aplicativo cliente crie um processo dedicado separado executando Unsecapp.exe para hospedar uma implementação [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="bb1a3-113">O processo dedicado pode chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para conceder acesso de WMI ao processo dedicado sem comprometer a segurança do processo principal.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="bb1a3-114">Após a inicialização, o processo dedicado atua como um intermediário entre o processo principal e o WMI.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="bb1a3-115">O procedimento a seguir descreve como executar uma chamada assíncrona com [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="bb1a3-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="bb1a3-116">**Para executar uma chamada assíncrona com IUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="bb1a3-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="bb1a3-117">Crie um processo dedicado com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="bb1a3-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="bb1a3-118">O exemplo de código a seguir chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um processo dedicado.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="bb1a3-119">Crie uma instância do objeto Sink.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="bb1a3-120">O exemplo de código a seguir cria um novo objeto de coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="bb1a3-121">Crie um stub para o coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="bb1a3-122">Um stub é uma função de wrapper produzida do coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="bb1a3-123">O exemplo de código a seguir chama [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) para criar um stub para o coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="bb1a3-124">Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para o wrapper e solicite um ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="bb1a3-125">O exemplo de código a seguir chama [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e solicita um ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="bb1a3-126">Libere o ponteiro do objeto do coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="bb1a3-127">Você pode liberar o ponteiro do objeto porque o stub agora possui o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="bb1a3-128">O exemplo de código a seguir libera o ponteiro do objeto do coletor.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="bb1a3-129">Use o stub em qualquer chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="bb1a3-130">Quando terminar com a chamada, libere a contagem de referência local.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="bb1a3-131">O exemplo de código a seguir usa o stub em uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="bb1a3-132">Às vezes, talvez seja necessário cancelar uma chamada assíncrona depois de fazer a chamada.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="bb1a3-133">Se você precisar cancelar a chamada, cancele a chamada com o mesmo ponteiro que originalmente fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="bb1a3-134">O exemplo de código a seguir mostra como cancelar uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="bb1a3-135">Libere a contagem de referência local quando terminar de usar a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="bb1a3-136">Certifique-se de liberar o ponteiro *pStubSink* somente depois de confirmar que a chamada assíncrona não precisa ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="bb1a3-137">Além disso, não libere *pStubSink* depois que o WMI liberar o ponteiro do coletor *pSink* .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="bb1a3-138">A liberação de *pStubSink* após o *pSink* cria uma contagem de referência circular na qual o coletor e o stub permanecem na memória para sempre.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="bb1a3-139">Em vez disso, um local possível para liberar o ponteiro está na chamada [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , feita pelo WMI para relatar que a chamada assíncrona original foi concluída.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="bb1a3-140">Quando terminar, não inicializar com com uma chamada para [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="bb1a3-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="bb1a3-141">O exemplo de código a seguir mostra como chamar [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="bb1a3-142">Os exemplos de código neste tópico exigem a referência a seguir e \# incluem a instrução para compilação correta.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="bb1a3-143">Para obter mais informações sobre a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) e os parâmetros, consulte a documentação [com](../cossdk/component-services-portal.md) no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
