---
description: Gerado por uma origem de mídia quando as características das fontes são alteradas.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788616"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="2354f-103">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="2354f-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="2354f-104">Gerado por uma origem de mídia quando as características da fonte são alteradas.</span><span class="sxs-lookup"><span data-stu-id="2354f-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="2354f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="2354f-105">Event values</span></span>

<span data-ttu-id="2354f-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="2354f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2354f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2354f-107">VARTYPE</span></span>              | <span data-ttu-id="2354f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2354f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2354f-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="2354f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2354f-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="2354f-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="2354f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="2354f-111">Attributes</span></span>

<span data-ttu-id="2354f-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="2354f-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="2354f-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="2354f-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="2354f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2354f-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="2354f-115">**\_características de \_ origem do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="2354f-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="2354f-116">Novas características da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="2354f-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="2354f-117">**\_características de origem do evento MF \_ \_ \_ antigas**</span><span class="sxs-lookup"><span data-stu-id="2354f-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="2354f-118">Características anteriores da origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="2354f-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="2354f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2354f-119">Requirements</span></span>



| <span data-ttu-id="2354f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2354f-120">Requirement</span></span> | <span data-ttu-id="2354f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2354f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2354f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2354f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2354f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2354f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2354f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2354f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2354f-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2354f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2354f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2354f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2354f-127"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2354f-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2354f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2354f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2354f-129">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="2354f-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="2354f-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2354f-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




