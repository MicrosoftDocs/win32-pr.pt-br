---
description: 'Gerado por uma origem de mídia quando o método IMFMediaSource:: Stop é concluído de forma assíncrona.'
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Evento MESourceStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788615"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="632e2-103">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="632e2-103">MESourceStopped event</span></span>

<span data-ttu-id="632e2-104">Gerado por uma origem de mídia quando o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="632e2-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="632e2-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="632e2-105">Event values</span></span>

<span data-ttu-id="632e2-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="632e2-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="632e2-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="632e2-107">VARTYPE</span></span>              | <span data-ttu-id="632e2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="632e2-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="632e2-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="632e2-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="632e2-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="632e2-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="632e2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="632e2-111">Requirements</span></span>



| <span data-ttu-id="632e2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="632e2-112">Requirement</span></span> | <span data-ttu-id="632e2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="632e2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632e2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="632e2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="632e2-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="632e2-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="632e2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="632e2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="632e2-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="632e2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="632e2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="632e2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="632e2-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="632e2-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="632e2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="632e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632e2-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="632e2-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




