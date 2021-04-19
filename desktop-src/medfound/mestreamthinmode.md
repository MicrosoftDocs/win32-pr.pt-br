---
description: Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo. Para obter informações sobre a fina, consulte sobre o controle de taxa.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793289"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="e9f0b-104">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="e9f0b-104">MEStreamThinMode event</span></span>

<span data-ttu-id="e9f0b-105">Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9f0b-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="e9f0b-106">Para obter informações sobre a *fina*, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="e9f0b-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="e9f0b-107">Esse evento pode ser enviado em resposta ao método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) ou ao método [**IMFQualityAdvise:: setdropmode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .</span><span class="sxs-lookup"><span data-stu-id="e9f0b-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="e9f0b-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e9f0b-108">Event values</span></span>

<span data-ttu-id="e9f0b-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="e9f0b-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9f0b-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e9f0b-110">VARTYPE</span></span></th>
<th><span data-ttu-id="e9f0b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9f0b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9f0b-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="e9f0b-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="e9f0b-113">Indica se a fina foi iniciada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="e9f0b-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="e9f0b-114">VARIANT_TRUE: amostras entregues depois que esse evento é finado.</span><span class="sxs-lookup"><span data-stu-id="e9f0b-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="e9f0b-115">VARIANT_FALSE: exemplos entregues após esse evento não são Finados.</span><span class="sxs-lookup"><span data-stu-id="e9f0b-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e9f0b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f0b-116">Requirements</span></span>



| <span data-ttu-id="e9f0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f0b-117">Requirement</span></span> | <span data-ttu-id="e9f0b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e9f0b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f0b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f0b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9f0b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9f0b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f0b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9f0b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9f0b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9f0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f0b-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f0b-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f0b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9f0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f0b-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9f0b-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




