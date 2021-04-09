---
description: 'Gerado por uma origem de mídia quando a taxa de reprodução é alterada. Esse evento é enviado depois que o método IMFRateControl:: SetRate é concluído de forma assíncrona.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Evento MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090701"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="78db9-104">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="78db9-104">MESourceRateChanged event</span></span>

<span data-ttu-id="78db9-105">Gerado por uma origem de mídia quando a taxa de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="78db9-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="78db9-106">Esse evento é enviado depois que o método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="78db9-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="78db9-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="78db9-107">Event values</span></span>

<span data-ttu-id="78db9-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="78db9-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="78db9-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="78db9-109">VARTYPE</span></span>           | <span data-ttu-id="78db9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="78db9-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="78db9-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="78db9-111">VT\_R4</span></span><br/> | <span data-ttu-id="78db9-112">A nova taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="78db9-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="78db9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78db9-113">Requirements</span></span>



| <span data-ttu-id="78db9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="78db9-114">Requirement</span></span> | <span data-ttu-id="78db9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="78db9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78db9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78db9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78db9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78db9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78db9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78db9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78db9-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78db9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78db9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78db9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78db9-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78db9-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78db9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="78db9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78db9-123">Implementando o controle de taxa</span><span class="sxs-lookup"><span data-stu-id="78db9-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="78db9-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78db9-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="78db9-125">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="78db9-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="78db9-126">**IMFRateControl:: SetRate**</span><span class="sxs-lookup"><span data-stu-id="78db9-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




