---
description: Gerado pelo processador de áudio quando o dispositivo de áudio é removido. O processador de áudio agora é inválido.
ms.assetid: a65a3931-e0d6-47ac-b545-9d616e914109
title: Evento MEAudioSessionDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8153eca68d480f092a358c35bfcbad7cedffd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501285"
---
# <a name="meaudiosessiondeviceremoved-event"></a><span data-ttu-id="06182-104">Evento MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="06182-104">MEAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="06182-105">Gerado pelo processador de áudio quando o dispositivo de áudio é removido.</span><span class="sxs-lookup"><span data-stu-id="06182-105">Raised by the audio renderer when the audio device is removed.</span></span> <span data-ttu-id="06182-106">O processador de áudio agora é inválido.</span><span class="sxs-lookup"><span data-stu-id="06182-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="06182-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06182-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="06182-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="06182-108">Event values</span></span>

<span data-ttu-id="06182-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="06182-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="06182-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="06182-110">VARTYPE</span></span>                | <span data-ttu-id="06182-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="06182-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="06182-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="06182-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="06182-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="06182-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="06182-114">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="06182-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="06182-115">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="06182-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="06182-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="06182-116">Remarks</span></span>

<span data-ttu-id="06182-117">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="06182-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="06182-118">O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonDeviceRemoval**.</span><span class="sxs-lookup"><span data-stu-id="06182-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

<span data-ttu-id="06182-119">O ponteiro [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se definido, não é útil, pois o fluxo de áudio não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="06182-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="06182-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06182-120">Requirements</span></span>



| <span data-ttu-id="06182-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="06182-121">Requirement</span></span> | <span data-ttu-id="06182-122">Valor</span><span class="sxs-lookup"><span data-stu-id="06182-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06182-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06182-123">Minimum supported client</span></span><br/> | <span data-ttu-id="06182-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06182-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="06182-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06182-125">Minimum supported server</span></span><br/> | <span data-ttu-id="06182-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06182-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06182-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06182-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="06182-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06182-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06182-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="06182-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06182-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06182-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="06182-131">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="06182-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
