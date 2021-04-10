---
description: Sinaliza que uma fonte de mídia parou de armazenar em buffer os dados.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Evento MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296509"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="96be3-103">Evento MEBufferingStopped</span><span class="sxs-lookup"><span data-stu-id="96be3-103">MEBufferingStopped event</span></span>

<span data-ttu-id="96be3-104">Sinaliza que uma fonte de mídia parou de armazenar em buffer os dados.</span><span class="sxs-lookup"><span data-stu-id="96be3-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="96be3-105">Uma origem de mídia envia isso ao parar de armazenar dados em buffer depois de enviar o evento [MEBufferingStarted](mebufferingstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="96be3-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="96be3-106">Os fluxos de bytes que implementam a interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) também enviam esse evento.</span><span class="sxs-lookup"><span data-stu-id="96be3-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="96be3-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="96be3-107">Event values</span></span>

<span data-ttu-id="96be3-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="96be3-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="96be3-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="96be3-109">VARTYPE</span></span>              | <span data-ttu-id="96be3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="96be3-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="96be3-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="96be3-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="96be3-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="96be3-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="96be3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96be3-113">Remarks</span></span>

<span data-ttu-id="96be3-114">Quando a sessão de mídia recebe esse evento, ele reinicia o relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="96be3-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="96be3-115">A sessão de mídia também encaminha o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96be3-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="96be3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96be3-116">Requirements</span></span>



| <span data-ttu-id="96be3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="96be3-117">Requirement</span></span> | <span data-ttu-id="96be3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="96be3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96be3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96be3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96be3-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96be3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96be3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96be3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96be3-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96be3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96be3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96be3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96be3-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96be3-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96be3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="96be3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96be3-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96be3-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




