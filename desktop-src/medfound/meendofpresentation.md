---
description: Gerado por uma origem de mídia quando uma apresentação termina. Esse evento sinaliza que todos os fluxos na apresentação são concluídos. A sessão de mídia encaminha esse evento para o aplicativo.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748111"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="f667b-105">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="f667b-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="f667b-106">Gerado por uma origem de mídia quando uma apresentação termina.</span><span class="sxs-lookup"><span data-stu-id="f667b-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="f667b-107">Esse evento sinaliza que todos os fluxos na apresentação são concluídos.</span><span class="sxs-lookup"><span data-stu-id="f667b-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="f667b-108">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f667b-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="f667b-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f667b-109">Event values</span></span>

<span data-ttu-id="f667b-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f667b-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f667b-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f667b-111">VARTYPE</span></span>              | <span data-ttu-id="f667b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f667b-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f667b-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="f667b-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f667b-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="f667b-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="f667b-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="f667b-115">Attributes</span></span>

<span data-ttu-id="f667b-116">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="f667b-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f667b-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="f667b-117">Attribute</span></span>                                                                                               | <span data-ttu-id="f667b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f667b-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f667b-119">**\_topologia de origem do evento MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="f667b-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="f667b-120">Especifica se a origem do sequenciador cancelou esta apresentação.</span><span class="sxs-lookup"><span data-stu-id="f667b-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f667b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f667b-121">Requirements</span></span>



| <span data-ttu-id="f667b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f667b-122">Requirement</span></span> | <span data-ttu-id="f667b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f667b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f667b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f667b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f667b-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f667b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f667b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f667b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f667b-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f667b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f667b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f667b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f667b-129"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f667b-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f667b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f667b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f667b-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f667b-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




