---
description: Enviado pelo processamento de áudio de streaming (SAR) quando o estado de volume ou mudo da sessão de áudio for alterado.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791088"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="6fc3b-103">Evento MEAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="6fc3b-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="6fc3b-104">Enviado pelo processamento de áudio de streaming (SAR) quando o estado de volume ou mudo da sessão de áudio for alterado.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="6fc3b-105">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="6fc3b-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6fc3b-106">Event values</span></span>

<span data-ttu-id="6fc3b-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6fc3b-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6fc3b-108">VARTYPE</span></span>                | <span data-ttu-id="6fc3b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fc3b-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc3b-110">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="6fc3b-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="6fc3b-111">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="6fc3b-112">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="6fc3b-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="6fc3b-113">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="6fc3b-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6fc3b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fc3b-114">Remarks</span></span>

<span data-ttu-id="6fc3b-115">Esse evento é gerado pelo coletor de fluxo do SAR.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="6fc3b-116">O evento é disparado quando o SAR recebe um evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) da sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="6fc3b-117">Para obter o novo nível de volume e o estado de mudo, chame [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) e [**IMFSimpleAudioVolume:: getmudo**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="6fc3b-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="6fc3b-118">O SAR envia esse evento se uma ação externa alterar o volume — por exemplo, se o usuário alterar o volume por meio do SndVol (programa de controle de volume de sistema).</span><span class="sxs-lookup"><span data-stu-id="6fc3b-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="6fc3b-119">O SAR não enviará o evento se o aplicativo alterar o volume diretamente no SAR.</span><span class="sxs-lookup"><span data-stu-id="6fc3b-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="6fc3b-120">Além disso, o SAR não envia esse evento quando o volume do canal é alterado ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="6fc3b-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc3b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc3b-121">Requirements</span></span>



| <span data-ttu-id="6fc3b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc3b-122">Requirement</span></span> | <span data-ttu-id="6fc3b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc3b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc3b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc3b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc3b-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fc3b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6fc3b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc3b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc3b-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fc3b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fc3b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fc3b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc3b-129"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fc3b-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fc3b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fc3b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc3b-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fc3b-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6fc3b-132">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="6fc3b-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
