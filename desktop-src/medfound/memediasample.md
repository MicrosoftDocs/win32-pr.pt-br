---
description: 'Enviado quando um fluxo de mídia fornece um novo exemplo em resposta a uma chamada para IMFMediaStream:: RequestSample.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Evento MEMediaSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764979"
---
# <a name="memediasample-event"></a><span data-ttu-id="49aef-103">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="49aef-103">MEMediaSample event</span></span>

<span data-ttu-id="49aef-104">Enviado quando um fluxo de mídia fornece um novo exemplo em resposta a uma chamada para [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="49aef-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="49aef-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="49aef-105">Event values</span></span>

<span data-ttu-id="49aef-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="49aef-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="49aef-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="49aef-107">VARTYPE</span></span>                | <span data-ttu-id="49aef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="49aef-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49aef-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="49aef-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="49aef-110">Ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="49aef-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="49aef-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49aef-111">Requirements</span></span>



| <span data-ttu-id="49aef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="49aef-112">Requirement</span></span> | <span data-ttu-id="49aef-113">Valor</span><span class="sxs-lookup"><span data-stu-id="49aef-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49aef-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49aef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="49aef-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49aef-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49aef-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49aef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="49aef-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49aef-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49aef-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49aef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="49aef-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49aef-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49aef-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="49aef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49aef-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49aef-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="49aef-122">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="49aef-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




