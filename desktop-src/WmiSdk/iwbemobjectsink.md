---
description: A interface IWbemObjectSink cria uma interface de coletor que pode receber todos os tipos de notificações dentro do modelo de programação WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interface IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767710"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="8b077-103">Interface IWbemObjectSink</span><span class="sxs-lookup"><span data-stu-id="8b077-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="8b077-104">A interface **IWbemObjectSink** cria uma interface de coletor que pode receber todos os tipos de notificações dentro do modelo de programação WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="8b077-105">Os clientes devem implementar essa interface para receber os resultados dos [métodos assíncronos](making-an-asynchronous-call-with-c--.md) de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)e tipos específicos de notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="8b077-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="8b077-106">Os provedores usam, mas não implementam essa interface para fornecer eventos e objetos ao WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="8b077-107">Normalmente, os provedores chamam uma implementação fornecida a eles pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="8b077-108">Nesses casos, chame [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) para fornecer objetos ao serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="8b077-109">Depois disso, chame [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para indicar o final da sequência de notificação.</span><span class="sxs-lookup"><span data-stu-id="8b077-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="8b077-110">Você também pode chamar **SetStatus** para indicar erros quando o coletor não tiver nenhum objeto.</span><span class="sxs-lookup"><span data-stu-id="8b077-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="8b077-111">Ao programar clientes assíncronos do WMI, o usuário fornece a implementação.</span><span class="sxs-lookup"><span data-stu-id="8b077-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="8b077-112">O WMI chama os métodos para entregar objetos e definir o status do resultado.</span><span class="sxs-lookup"><span data-stu-id="8b077-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="8b077-113">Se um aplicativo cliente passar a mesma interface de coletor em duas chamadas assíncronas sobrepostas diferentes, o WMI não garantirá a ordem do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8b077-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="8b077-114">Os aplicativos cliente que fazem chamadas assíncronas sobrepostas devem passar objetos de coletor diferentes ou serializar suas chamadas.</span><span class="sxs-lookup"><span data-stu-id="8b077-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="8b077-115">Como o retorno de chamada para o coletor não pode ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8b077-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="8b077-116">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b077-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="8b077-117">Membros</span><span class="sxs-lookup"><span data-stu-id="8b077-117">Members</span></span>

<span data-ttu-id="8b077-118">A interface **IWbemObjectSink** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b077-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="8b077-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b077-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b077-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b077-120">Methods</span></span>

<span data-ttu-id="8b077-121">A interface **IWbemObjectSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8b077-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="8b077-122">Método</span><span class="sxs-lookup"><span data-stu-id="8b077-122">Method</span></span>                                         | <span data-ttu-id="8b077-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b077-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b077-124">**Indicar**</span><span class="sxs-lookup"><span data-stu-id="8b077-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="8b077-125">Recebe objetos de notificação.</span><span class="sxs-lookup"><span data-stu-id="8b077-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="8b077-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="8b077-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="8b077-127">Chamado por fontes para indicar o final de uma sequência de notificação ou para enviar outros códigos de status ao coletor.</span><span class="sxs-lookup"><span data-stu-id="8b077-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b077-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b077-128">Remarks</span></span>

<span data-ttu-id="8b077-129">Ao implementar um coletor de assinatura de evento (**IWbemObjectSink** ou [**IWbemEventSink**](iwbemeventsink.md)), não chame o WMI de dentro dos métodos de [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ou [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) no objeto do coletor.</span><span class="sxs-lookup"><span data-stu-id="8b077-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="8b077-130">Por exemplo, chamar [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar o coletor de dentro de uma implementação de [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) pode interferir no estado do WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="8b077-131">Para cancelar uma assinatura de evento, defina um sinalizador e chame **IWbemServices:: CancelAsyncCall** de outro thread ou objeto.</span><span class="sxs-lookup"><span data-stu-id="8b077-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="8b077-132">Para implementações que não estão relacionadas a um coletor de eventos, como recuperações de objeto, enum e consulta, você pode chamar de volta para o WMI.</span><span class="sxs-lookup"><span data-stu-id="8b077-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="8b077-133">As implementações do coletor devem processar a notificação de eventos dentro de 100 ms porque o thread WMI que entrega a notificação de eventos não pode realizar outro trabalho até que o objeto do coletor tenha concluído o processamento.</span><span class="sxs-lookup"><span data-stu-id="8b077-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="8b077-134">Se a notificação exigir uma grande quantidade de processamento, o coletor poderá usar uma fila interna para que outro thread manipule o processamento.</span><span class="sxs-lookup"><span data-stu-id="8b077-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="8b077-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b077-135">Examples</span></span>

<span data-ttu-id="8b077-136">O exemplo de código a seguir é uma implementação simples de um coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="8b077-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="8b077-137">Este exemplo pode ser usado com [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) para receber as instâncias retornadas:</span><span class="sxs-lookup"><span data-stu-id="8b077-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="8b077-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b077-138">Requirements</span></span>



| <span data-ttu-id="8b077-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b077-139">Requirement</span></span> | <span data-ttu-id="8b077-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8b077-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b077-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b077-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8b077-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b077-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="8b077-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b077-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8b077-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b077-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="8b077-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b077-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b077-146"><dt>Wbemcli. h (incluir Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b077-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8b077-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b077-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b077-148"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b077-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="8b077-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8b077-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b077-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b077-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="8b077-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b077-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b077-152">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="8b077-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="8b077-153">Fazendo uma chamada assíncrona com C++</span><span class="sxs-lookup"><span data-stu-id="8b077-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="8b077-154">Definindo a segurança em uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="8b077-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="8b077-155">Recebendo eventos para a duração do seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="8b077-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




