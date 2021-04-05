---
description: Gerado por um fluxo de mídia quando o fluxo termina.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Evento MEEndOfStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827639"
---
# <a name="meendofstream-event"></a><span data-ttu-id="b5cea-103">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="b5cea-103">MEEndOfStream event</span></span>

<span data-ttu-id="b5cea-104">Gerado por um fluxo de mídia quando o fluxo termina.</span><span class="sxs-lookup"><span data-stu-id="b5cea-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="b5cea-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b5cea-105">Event values</span></span>

<span data-ttu-id="b5cea-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b5cea-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b5cea-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b5cea-107">VARTYPE</span></span>              | <span data-ttu-id="b5cea-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5cea-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b5cea-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="b5cea-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b5cea-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="b5cea-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b5cea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5cea-111">Remarks</span></span>

<span data-ttu-id="b5cea-112">Quando a [sessão de mídia](media-session.md) recebe o evento MEEndOfStream, ela chama [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) no coletor de mídia correspondente, com o tipo de marcador **\_ \_ ENDOFSEGMENT do marcador MFSTREAMSINK** .</span><span class="sxs-lookup"><span data-stu-id="b5cea-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5cea-113">Requirements</span></span>



| <span data-ttu-id="b5cea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cea-114">Requirement</span></span> | <span data-ttu-id="b5cea-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b5cea-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cea-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5cea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cea-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5cea-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5cea-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5cea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cea-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5cea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5cea-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5cea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cea-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5cea-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cea-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5cea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cea-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5cea-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




