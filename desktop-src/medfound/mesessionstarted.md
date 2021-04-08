---
description: 'Gerado quando o método IMFMediaSession:: Start é concluído de forma assíncrona.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Evento MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010724"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="70ce4-103">Evento MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="70ce4-103">MESessionStarted event</span></span>

<span data-ttu-id="70ce4-104">Gerado quando o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="70ce4-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="70ce4-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="70ce4-105">Event values</span></span>

<span data-ttu-id="70ce4-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="70ce4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="70ce4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="70ce4-107">VARTYPE</span></span>              | <span data-ttu-id="70ce4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70ce4-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="70ce4-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="70ce4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="70ce4-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="70ce4-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="70ce4-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="70ce4-111">Attributes</span></span>

<span data-ttu-id="70ce4-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="70ce4-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="70ce4-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="70ce4-113">Attribute</span></span>                                                                                               | <span data-ttu-id="70ce4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="70ce4-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70ce4-115">**\_deslocamento do \_ tempo de apresentação do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70ce4-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="70ce4-116">Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="70ce4-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="70ce4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ce4-117">Requirements</span></span>



| <span data-ttu-id="70ce4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ce4-118">Requirement</span></span> | <span data-ttu-id="70ce4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70ce4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ce4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70ce4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70ce4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70ce4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70ce4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70ce4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70ce4-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70ce4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70ce4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70ce4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70ce4-125"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70ce4-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ce4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="70ce4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ce4-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70ce4-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




