---
description: Enviado por uma fonte de captura de áudio quando o formato de áudio é alterado.
ms.assetid: 8197BBAD-8102-43C3-BA61-8DC3BC13B7D6
title: Evento MECaptureAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb260d186a9e4d8434669e6a8c3ef08078b93af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296486"
---
# <a name="mecaptureaudiosessionformatchanged-event"></a><span data-ttu-id="75199-103">Evento MECaptureAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="75199-103">MECaptureAudioSessionFormatChanged event</span></span>

<span data-ttu-id="75199-104">Enviado por uma fonte de captura de áudio quando o formato de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="75199-104">Sent by an audio capture source when the audio format changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="75199-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="75199-105">Event values</span></span>

<span data-ttu-id="75199-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="75199-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="75199-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="75199-107">VARTYPE</span></span>               | <span data-ttu-id="75199-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="75199-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="75199-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="75199-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="75199-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="75199-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="75199-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="75199-111">Remarks</span></span>

<span data-ttu-id="75199-112">Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="75199-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="75199-113">A origem de captura envia esse evento quando recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonFormatChanged**.</span><span class="sxs-lookup"><span data-stu-id="75199-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

## <a name="requirements"></a><span data-ttu-id="75199-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75199-114">Requirements</span></span>



| <span data-ttu-id="75199-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75199-115">Requirement</span></span> | <span data-ttu-id="75199-116">Valor</span><span class="sxs-lookup"><span data-stu-id="75199-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75199-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75199-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75199-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="75199-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="75199-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75199-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75199-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="75199-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75199-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75199-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75199-122"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75199-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75199-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="75199-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75199-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75199-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
