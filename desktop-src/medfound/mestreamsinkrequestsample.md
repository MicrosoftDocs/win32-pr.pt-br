---
description: Gerado por um coletor de fluxo para solicitar um novo exemplo de mídia do pipeline.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782279"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="9cbf3-103">Evento MEStreamSinkRequestSample</span><span class="sxs-lookup"><span data-stu-id="9cbf3-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="9cbf3-104">Gerado por um coletor de fluxo para solicitar um novo exemplo de mídia do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9cbf3-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="9cbf3-105">Para cada evento MEStreamSinkRequestSample, o pipeline solicita dados do próximo componente upstream.</span><span class="sxs-lookup"><span data-stu-id="9cbf3-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="9cbf3-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9cbf3-106">Event values</span></span>

<span data-ttu-id="9cbf3-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9cbf3-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9cbf3-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9cbf3-108">VARTYPE</span></span>              | <span data-ttu-id="9cbf3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cbf3-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9cbf3-110">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="9cbf3-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9cbf3-111">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="9cbf3-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="9cbf3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbf3-112">Requirements</span></span>



| <span data-ttu-id="9cbf3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbf3-113">Requirement</span></span> | <span data-ttu-id="9cbf3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbf3-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbf3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbf3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9cbf3-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cbf3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9cbf3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbf3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9cbf3-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cbf3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9cbf3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cbf3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cbf3-120"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbf3-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbf3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbf3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbf3-122">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9cbf3-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9cbf3-123">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="9cbf3-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




