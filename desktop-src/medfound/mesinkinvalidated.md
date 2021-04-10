---
description: Gerado quando um coletor de mídia se torna inválido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164655"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="7a8bb-103">Evento MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="7a8bb-103">MESinkInvalidated event</span></span>

<span data-ttu-id="7a8bb-104">Gerado quando um coletor de mídia se torna inválido.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="7a8bb-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="7a8bb-105">Event values</span></span>

<span data-ttu-id="7a8bb-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7a8bb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7a8bb-107">VARTYPE</span></span>              | <span data-ttu-id="7a8bb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a8bb-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7a8bb-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="7a8bb-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7a8bb-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="7a8bb-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a8bb-111">Attributes</span></span>

<span data-ttu-id="7a8bb-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="7a8bb-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="7a8bb-113">Attribute</span></span>                                                                    | <span data-ttu-id="7a8bb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a8bb-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="7a8bb-115">**\_nó de \_ saída do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="7a8bb-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="7a8bb-116">Identifica o nó de topologia para este coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7a8bb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a8bb-117">Remarks</span></span>

<span data-ttu-id="7a8bb-118">A sessão de mídia gerará esse evento se receber qualquer um dos seguintes eventos do coletor de mídia:</span><span class="sxs-lookup"><span data-stu-id="7a8bb-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="7a8bb-119">MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="7a8bb-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="7a8bb-120">MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="7a8bb-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="7a8bb-121">MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="7a8bb-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="7a8bb-122">MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="7a8bb-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="7a8bb-123">MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="7a8bb-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="7a8bb-124">Um coletor de mídia também pode gerar esse evento; nesse caso, a sessão de mídia define o atributo de [**\_ nó de \_ saída \_ de evento MF**](mf-event-output-node-attribute.md) no evento e encaminha o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="7a8bb-125">Se o aplicativo receber esse evento, ele precisará recriar o coletor de mídia e enfileirar a topologia novamente.</span><span class="sxs-lookup"><span data-stu-id="7a8bb-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a8bb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a8bb-126">Requirements</span></span>



| <span data-ttu-id="7a8bb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a8bb-127">Requirement</span></span> | <span data-ttu-id="7a8bb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7a8bb-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8bb-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a8bb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8bb-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a8bb-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a8bb-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a8bb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8bb-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a8bb-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a8bb-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a8bb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a8bb-134"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a8bb-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a8bb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a8bb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8bb-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a8bb-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




