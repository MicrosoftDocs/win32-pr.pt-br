---
description: 'Chamadas Semisynchronous são os meios recomendados para chamar métodos WMI, como os métodos IWbemServices:: ExecMethod e Provider, como o método chkdsk da classe do disco \_ lógico do Win32.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Fazendo uma chamada Semisynchronous com C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506048"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="f7ae3-103">Fazendo uma chamada Semisynchronous com C++</span><span class="sxs-lookup"><span data-stu-id="f7ae3-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="f7ae3-104">Chamadas Semisynchronous são os meios recomendados para chamar métodos WMI, como os métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) e Provider, como o [**método chkdsk da classe do disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="f7ae3-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="f7ae3-105">Uma desvantagem do processamento síncrono é que o thread do chamador é bloqueado até que a chamada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="f7ae3-106">O bloqueio pode causar um atraso no tempo de processamento.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="f7ae3-107">Por outro lado, uma chamada assíncrona deve implementar [**SWbemSink**](swbemsink.md) no script.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="f7ae3-108">Em C++, o código assíncrono deve implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) , usar vários threads e controlar o fluxo de informações de volta para o chamador.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="f7ae3-109">Conjuntos de resultados grandes de consultas, por exemplo, podem levar um tempo considerável para fornecer e obriga o chamador a gastar recursos de sistema significativos para lidar com a entrega.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="f7ae3-110">O processamento de Semisynchronous resolve o bloqueio de thread e os problemas de entrega não controlados sondando um objeto de status especial que implementa a interface [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="f7ae3-111">Por meio do **IWbemCallResult**, você pode melhorar a velocidade e a eficiência de consultas, enumerações e notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="f7ae3-112">O procedimento a seguir descreve como fazer uma chamada semisynchronous com a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="f7ae3-113">**Para fazer uma chamada semisynchronous com a interface IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="f7ae3-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="f7ae3-114">Faça sua chamada normalmente, mas com o **sinalizador WBEM \_ , \_ retorne \_ imediatamente** o sinalizador definido no parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="f7ae3-115">Você pode combinar **o \_ retorno do sinalizador WBEM \_ \_ imediatamente** com outros sinalizadores que são válidos para o método específico.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="f7ae3-116">Por exemplo, use o sinalizador de **\_ \_ \_ somente encaminhamento do sinalizador WBEM** para todas as chamadas que retornam enumeradores.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="f7ae3-117">Definir esses sinalizadores em combinação economiza tempo e espaço e melhora a capacidade de resposta.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="f7ae3-118">Sondar seus resultados.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-118">Poll for your results.</span></span>

    <span data-ttu-id="f7ae3-119">Se você chamar um método que retorna um enumerador, como [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) ou [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), poderá sondar os enumeradores com os métodos [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="f7ae3-120">A chamada **IEnumWbemClassObject:: NextAsync** é não bloqueada e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="f7ae3-121">Em segundo plano, o WMI começa a entregar o número solicitado de objetos chamando [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="f7ae3-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="f7ae3-122">Em seguida, o WMI para e aguarda outra chamada **NextAsync** .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="f7ae3-123">Se você chamar um método que não retorna um enumerador, como [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), deverá definir o parâmetro *ppCallResult* como um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="f7ae3-124">Use o [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) no ponteiro retornado para recuperar o **WBEM \_ S \_ sem \_ erro**.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="f7ae3-125">Conclua sua chamada.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-125">Finish your call.</span></span>

    <span data-ttu-id="f7ae3-126">Para uma chamada que retorna um enumerador, o WMI chama [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para relatar a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="f7ae3-127">Se você não precisar do resultado inteiro, libere o enumerador chamando o método [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="f7ae3-128">Chamar resultados de **liberação** no WMI cancela a entrega de todos os objetos que permanecem.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="f7ae3-129">Para uma chamada que não usa um enumerador, recupere o objeto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) por meio do parâmetro *plStatus* do seu método.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="f7ae3-130">O exemplo de código C++ neste tópico requer as seguintes \# instruções include para serem compiladas corretamente.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="f7ae3-131">O exemplo de código a seguir mostra como fazer uma chamada de semisynchronous para [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="f7ae3-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="f7ae3-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7ae3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ae3-133">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="f7ae3-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
