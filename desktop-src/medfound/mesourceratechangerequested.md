---
description: 'Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução. O aplicativo deve chamar IMFRateControl:: SetRate com a taxa solicitada. Uma fonte de mídia poderá gerar esse evento se não for possível continuar a reprodução na taxa atual.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165038"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="be220-105">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="be220-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="be220-106">Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="be220-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="be220-107">O aplicativo deve chamar [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) com a taxa solicitada.</span><span class="sxs-lookup"><span data-stu-id="be220-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="be220-108">Uma fonte de mídia poderá gerar esse evento se não for possível continuar a reprodução na taxa atual.</span><span class="sxs-lookup"><span data-stu-id="be220-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="be220-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="be220-109">Event values</span></span>

<span data-ttu-id="be220-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="be220-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="be220-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="be220-111">VARTYPE</span></span>           | <span data-ttu-id="be220-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="be220-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="be220-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="be220-113">VT\_R4</span></span><br/> | <span data-ttu-id="be220-114">A nova taxa de reprodução solicitada.</span><span class="sxs-lookup"><span data-stu-id="be220-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="be220-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="be220-115">Attributes</span></span>

<span data-ttu-id="be220-116">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="be220-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="be220-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="be220-117">Attribute</span></span>                                                                    | <span data-ttu-id="be220-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="be220-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="be220-119">**o \_ evento MF \_ faz a \_ finação**</span><span class="sxs-lookup"><span data-stu-id="be220-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="be220-120">Especifica se a origem da mídia também solicita a fina.</span><span class="sxs-lookup"><span data-stu-id="be220-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="be220-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be220-121">Requirements</span></span>



| <span data-ttu-id="be220-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be220-122">Requirement</span></span> | <span data-ttu-id="be220-123">Valor</span><span class="sxs-lookup"><span data-stu-id="be220-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be220-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be220-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be220-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be220-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be220-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be220-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be220-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be220-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be220-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be220-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be220-129"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be220-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be220-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="be220-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be220-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be220-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




