---
description: Gerado por um coletor de fluxo quando o fluxo recebeu dados de pré-roll suficientes para começar a renderização. Esse evento é gerado por coletores de mídia que dão suporte à interface IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661579"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="26dca-104">Evento MEStreamSinkPrerolled</span><span class="sxs-lookup"><span data-stu-id="26dca-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="26dca-105">Gerado por um coletor de fluxo quando o fluxo recebeu dados de pré-roll suficientes para começar a renderização.</span><span class="sxs-lookup"><span data-stu-id="26dca-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="26dca-106">Esse evento é gerado por coletores de mídia que dão suporte à interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="26dca-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="26dca-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="26dca-107">Event values</span></span>

<span data-ttu-id="26dca-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="26dca-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="26dca-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="26dca-109">VARTYPE</span></span>              | <span data-ttu-id="26dca-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="26dca-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="26dca-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="26dca-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="26dca-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="26dca-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="26dca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26dca-113">Requirements</span></span>



| <span data-ttu-id="26dca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="26dca-114">Requirement</span></span> | <span data-ttu-id="26dca-115">Valor</span><span class="sxs-lookup"><span data-stu-id="26dca-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26dca-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26dca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="26dca-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26dca-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26dca-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26dca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="26dca-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26dca-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26dca-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26dca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="26dca-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26dca-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26dca-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="26dca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26dca-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26dca-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="26dca-124">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="26dca-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




