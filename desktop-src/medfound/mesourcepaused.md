---
description: Gerado por uma origem de mídia quando o método IMFMediaSource::P ause é concluído de forma assíncrona.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Evento MESourcePaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827632"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="dc415-103">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="dc415-103">MESourcePaused event</span></span>

<span data-ttu-id="dc415-104">Gerado por uma origem de mídia quando o método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="dc415-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="dc415-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="dc415-105">Event values</span></span>

<span data-ttu-id="dc415-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="dc415-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dc415-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dc415-107">VARTYPE</span></span>              | <span data-ttu-id="dc415-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc415-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="dc415-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="dc415-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="dc415-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="dc415-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="dc415-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc415-111">Requirements</span></span>



| <span data-ttu-id="dc415-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc415-112">Requirement</span></span> | <span data-ttu-id="dc415-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dc415-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc415-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc415-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dc415-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc415-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc415-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc415-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dc415-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc415-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc415-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc415-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc415-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc415-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc415-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc415-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc415-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc415-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




