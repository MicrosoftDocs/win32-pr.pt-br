---
description: 'Gerado quando o método IMFMediaSession:: Stop é concluído de forma assíncrona.'
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: Evento MESessionStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297535"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="ef29f-103">Evento MESessionStopped</span><span class="sxs-lookup"><span data-stu-id="ef29f-103">MESessionStopped event</span></span>

<span data-ttu-id="ef29f-104">Gerado quando o método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ef29f-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ef29f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ef29f-105">Event values</span></span>

<span data-ttu-id="ef29f-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ef29f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ef29f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ef29f-107">VARTYPE</span></span>              | <span data-ttu-id="ef29f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef29f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ef29f-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="ef29f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ef29f-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="ef29f-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ef29f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef29f-111">Requirements</span></span>



| <span data-ttu-id="ef29f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef29f-112">Requirement</span></span> | <span data-ttu-id="ef29f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ef29f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef29f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef29f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ef29f-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef29f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ef29f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef29f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ef29f-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef29f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef29f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef29f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef29f-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef29f-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef29f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef29f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef29f-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef29f-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




