---
description: Inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interface IWbemEventSink (Wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764457"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="990eb-103">Interface IWbemEventSink</span><span class="sxs-lookup"><span data-stu-id="990eb-103">IWbemEventSink interface</span></span>

<span data-ttu-id="990eb-104">A interface **IWbemEventSink** inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas.</span><span class="sxs-lookup"><span data-stu-id="990eb-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="990eb-105">Essa interface estende o [**IWbemObjectSink**](iwbemobjectsink.md), fornecendo novos métodos que lidam com segurança e desempenho.</span><span class="sxs-lookup"><span data-stu-id="990eb-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="990eb-106">Para obter mais informações sobre como usar essa interface, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md) e [protegendo eventos WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="990eb-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="990eb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="990eb-107">Members</span></span>

<span data-ttu-id="990eb-108">A interface **IWbemEventSink** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="990eb-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="990eb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="990eb-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="990eb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="990eb-110">Methods</span></span>

<span data-ttu-id="990eb-111">A interface **IWbemEventSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="990eb-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="990eb-112">Método</span><span class="sxs-lookup"><span data-stu-id="990eb-112">Method</span></span>                                                                | <span data-ttu-id="990eb-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="990eb-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="990eb-114">**GetRestrictedSink**</span><span class="sxs-lookup"><span data-stu-id="990eb-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="990eb-115">Chamado pelo consumidor para configurar consultas de eventos restritos.</span><span class="sxs-lookup"><span data-stu-id="990eb-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="990eb-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="990eb-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="990eb-117">Verifica o status do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="990eb-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="990eb-118">**SetBatchingParameters**</span><span class="sxs-lookup"><span data-stu-id="990eb-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="990eb-119">Chamado pelo consumidor para definir parâmetros de envio em lote.</span><span class="sxs-lookup"><span data-stu-id="990eb-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="990eb-120">**SetSinkSecurity**</span><span class="sxs-lookup"><span data-stu-id="990eb-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="990eb-121">Usado para atualizar o descritor de segurança em um coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="990eb-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="990eb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="990eb-122">Remarks</span></span>

<span data-ttu-id="990eb-123">Ao implementar um coletor de assinatura de evento ([**IWbemObjectSink**](iwbemobjectsink.md) ou **IWbemEventSink**), não chame o WMI de dentro dos métodos no objeto Sink.</span><span class="sxs-lookup"><span data-stu-id="990eb-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="990eb-124">Por exemplo, chamar [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar o coletor de dentro de uma implementação de [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) pode interferir no estado do WMI.</span><span class="sxs-lookup"><span data-stu-id="990eb-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="990eb-125">Para cancelar uma assinatura de evento, defina um sinalizador e chame **IWbemServices:: CancelAsyncCall** de outro thread ou objeto.</span><span class="sxs-lookup"><span data-stu-id="990eb-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="990eb-126">Para implementações que não estão relacionadas a um coletor de eventos, como recuperações de objeto, enum e consulta, você pode chamar de volta para o WMI.</span><span class="sxs-lookup"><span data-stu-id="990eb-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="990eb-127">As implementações do coletor devem processar a notificação de eventos dentro de 100 ms porque o thread WMI que entrega a notificação de eventos não pode realizar outro trabalho até que o objeto do coletor tenha concluído o processamento.</span><span class="sxs-lookup"><span data-stu-id="990eb-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="990eb-128">Se a notificação exigir uma grande quantidade de processamento, o coletor poderá usar uma fila interna para que outro thread manipule o processamento.</span><span class="sxs-lookup"><span data-stu-id="990eb-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="990eb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="990eb-129">Requirements</span></span>



| <span data-ttu-id="990eb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="990eb-130">Requirement</span></span> | <span data-ttu-id="990eb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="990eb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="990eb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="990eb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="990eb-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="990eb-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="990eb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="990eb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="990eb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="990eb-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="990eb-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="990eb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="990eb-137"><dt>Wbemprov. h (incluir Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="990eb-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="990eb-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="990eb-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="990eb-139"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="990eb-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="990eb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="990eb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="990eb-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="990eb-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="990eb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="990eb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990eb-143">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="990eb-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




