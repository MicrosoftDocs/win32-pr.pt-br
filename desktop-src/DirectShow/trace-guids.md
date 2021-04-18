---
description: Os GUIDs a seguir são usados para rastreamento de eventos no DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUIDs de rastreamento (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753498"
---
# <a name="trace-guids"></a><span data-ttu-id="f026c-103">GUIDs de rastreamento</span><span class="sxs-lookup"><span data-stu-id="f026c-103">Trace GUIDs</span></span>

<span data-ttu-id="f026c-104">Os GUIDs a seguir são usados para rastreamento de eventos no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f026c-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="f026c-105">GUID</span><span class="sxs-lookup"><span data-stu-id="f026c-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="f026c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f026c-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="f026c-107"><dt>**\_AUDIOBREAK GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="f026c-108">Evento de quebra de áudio.</span><span class="sxs-lookup"><span data-stu-id="f026c-108">Audio break event.</span></span> <span data-ttu-id="f026c-109">Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para dados de evento.</span><span class="sxs-lookup"><span data-stu-id="f026c-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="f026c-110"><dt>**\_CTL de DShow de GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="f026c-111">Provedor de eventos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f026c-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="f026c-112"><dt>**\_STREAMTRACE GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="f026c-113">Evento de streaming geral.</span><span class="sxs-lookup"><span data-stu-id="f026c-113">General streaming event.</span></span> <span data-ttu-id="f026c-114">Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) para dados de evento.</span><span class="sxs-lookup"><span data-stu-id="f026c-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="f026c-115"><dt>**\_VIDEOREND GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="f026c-116">Evento de renderização de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f026c-116">Video rendering event.</span></span> <span data-ttu-id="f026c-117">Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ AVREND**](perfinfo-dshow-avrend.md) para dados de evento.</span><span class="sxs-lookup"><span data-stu-id="f026c-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="f026c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f026c-118">Requirements</span></span>



| <span data-ttu-id="f026c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f026c-119">Requirement</span></span> | <span data-ttu-id="f026c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f026c-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f026c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f026c-121">Header</span></span><br/> | <dl> <span data-ttu-id="f026c-122"><dt>PerfStruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f026c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f026c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f026c-124">Rastreamento de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="f026c-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




