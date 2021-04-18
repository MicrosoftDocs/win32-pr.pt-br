---
description: Fornece comentários para o Gerenciador de qualidade sobre a qualidade da reprodução.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502395"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="6a47e-103">Evento MEQualityNotify</span><span class="sxs-lookup"><span data-stu-id="6a47e-103">MEQualityNotify event</span></span>

<span data-ttu-id="6a47e-104">Fornece comentários para o Gerenciador de qualidade sobre a qualidade da reprodução.</span><span class="sxs-lookup"><span data-stu-id="6a47e-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="6a47e-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6a47e-105">Event values</span></span>

<span data-ttu-id="6a47e-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6a47e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6a47e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6a47e-107">VARTYPE</span></span>           | <span data-ttu-id="6a47e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a47e-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="6a47e-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="6a47e-109">VT\_I8</span></span><br/> | <span data-ttu-id="6a47e-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="6a47e-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a47e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a47e-111">Remarks</span></span>

<span data-ttu-id="6a47e-112">Esse evento é gerado por alguns componentes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a47e-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="6a47e-113">A sessão de mídia encaminha o evento para o Gerenciador de qualidade chamando o método [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .</span><span class="sxs-lookup"><span data-stu-id="6a47e-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="6a47e-114">O tipo estendido do evento indica o significado dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="6a47e-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="6a47e-115">Tipo estendido</span><span class="sxs-lookup"><span data-stu-id="6a47e-115">Extended type</span></span>                            | <span data-ttu-id="6a47e-116">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="6a47e-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a47e-117">\_latência de \_ processamento de notificação de qualidade MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="6a47e-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="6a47e-118">Latência de processamento aproximada introduzida pelo componente, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="6a47e-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="6a47e-119">A latência de processamento é a quantidade de latência que um componente apresenta ao pipeline processando um exemplo.</span><span class="sxs-lookup"><span data-stu-id="6a47e-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="6a47e-120">Em alguns casos, a latência não pode ser derivada simplesmente observando as chamadas para [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) e [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span><span class="sxs-lookup"><span data-stu-id="6a47e-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="6a47e-121">Por exemplo, pode não haver uma correspondência um-para-um entre exemplos de entrada e exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="6a47e-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="6a47e-122">Nesse caso, o componente pode enviar um evento MEQualityNotify com a latência de processamento.</span><span class="sxs-lookup"><span data-stu-id="6a47e-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="6a47e-123">Se a latência de processamento for alterada, o componente poderá enviar um novo evento a qualquer momento durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="6a47e-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="6a47e-124">\_atraso de \_ amostra de notificação de qualidade MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="6a47e-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="6a47e-125">Tempo de retardo para o exemplo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="6a47e-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="6a47e-126">Se o valor for positivo, o exemplo foi atrasado.</span><span class="sxs-lookup"><span data-stu-id="6a47e-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="6a47e-127">Se o valor for negativo, o exemplo foi antecipado.</span><span class="sxs-lookup"><span data-stu-id="6a47e-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="6a47e-128">Para obter o tipo estendido, chame [**IMFMediaEvent:: getextendedattribute**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="6a47e-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="6a47e-129">Os componentes de pipeline não são necessários para enviar este evento.</span><span class="sxs-lookup"><span data-stu-id="6a47e-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a47e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a47e-130">Requirements</span></span>



| <span data-ttu-id="6a47e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a47e-131">Requirement</span></span> | <span data-ttu-id="6a47e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6a47e-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a47e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a47e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6a47e-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a47e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a47e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a47e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6a47e-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a47e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6a47e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a47e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a47e-138"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a47e-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a47e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a47e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a47e-140">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="6a47e-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="6a47e-141">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a47e-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




