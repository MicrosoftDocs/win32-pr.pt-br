---
description: Enviado por um coletor de fluxo quando o formato downstream se tornou invalidado e precisa ser renegociado.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Evento MEStreamSinkFormatInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798496"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="35439-103">Evento MEStreamSinkFormatInvalidated</span><span class="sxs-lookup"><span data-stu-id="35439-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="35439-104">Enviado por um coletor de fluxo quando o formato downstream se tornou invalidado e precisa ser renegociado.</span><span class="sxs-lookup"><span data-stu-id="35439-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="35439-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="35439-105">Event values</span></span>

<span data-ttu-id="35439-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="35439-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="35439-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="35439-107">VARTYPE</span></span>              | <span data-ttu-id="35439-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="35439-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="35439-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="35439-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="35439-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="35439-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="35439-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="35439-111">Remarks</span></span>

<span data-ttu-id="35439-112">Os dados que foram enfileirados para o coletor, após a posição de reprodução atual, devem ser reenviados.</span><span class="sxs-lookup"><span data-stu-id="35439-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="35439-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35439-113">Requirements</span></span>



| <span data-ttu-id="35439-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="35439-114">Requirement</span></span> | <span data-ttu-id="35439-115">Valor</span><span class="sxs-lookup"><span data-stu-id="35439-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35439-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35439-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35439-117">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35439-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="35439-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35439-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35439-119">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="35439-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="35439-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35439-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35439-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35439-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35439-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="35439-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35439-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35439-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




