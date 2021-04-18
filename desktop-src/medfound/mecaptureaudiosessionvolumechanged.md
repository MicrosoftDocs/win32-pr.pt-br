---
description: Enviado por uma fonte de captura de áudio quando o volume é alterado.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791087"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="dc684-103">Evento MECaptureAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="dc684-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="dc684-104">Enviado por uma fonte de captura de áudio quando o volume é alterado.</span><span class="sxs-lookup"><span data-stu-id="dc684-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="dc684-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="dc684-105">Event values</span></span>

<span data-ttu-id="dc684-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="dc684-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dc684-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dc684-107">VARTYPE</span></span>               | <span data-ttu-id="dc684-108">Description</span><span class="sxs-lookup"><span data-stu-id="dc684-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="dc684-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="dc684-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="dc684-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="dc684-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="dc684-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc684-111">Remarks</span></span>

<span data-ttu-id="dc684-112">Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="dc684-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="dc684-113">A fonte de captura de áudio enviará esse evento se uma ação externa alterar o volume, por exemplo, se o usuário alterar o volume por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="dc684-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="dc684-114">A origem da captura não enviará o evento se o aplicativo alterar o volume diretamente na origem.</span><span class="sxs-lookup"><span data-stu-id="dc684-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc684-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc684-115">Requirements</span></span>



| <span data-ttu-id="dc684-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc684-116">Requirement</span></span> | <span data-ttu-id="dc684-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dc684-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc684-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc684-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc684-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc684-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="dc684-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc684-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc684-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc684-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc684-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc684-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc684-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc684-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc684-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc684-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc684-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc684-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




