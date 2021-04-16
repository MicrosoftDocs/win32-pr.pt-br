---
description: Gerado pelo processador de áudio quando o sistema de servidor de áudio do Windows é desligado. O processador de áudio agora é inválido.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Evento MEAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808372"
---
# <a name="meaudiosessionservershutdown-event"></a><span data-ttu-id="0564e-104">Evento MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="0564e-104">MEAudioSessionServerShutdown event</span></span>

<span data-ttu-id="0564e-105">Gerado pelo processador de áudio quando o sistema de servidor de áudio do Windows é desligado.</span><span class="sxs-lookup"><span data-stu-id="0564e-105">Raised by the audio renderer when the Windows audio server system is shut down.</span></span> <span data-ttu-id="0564e-106">O processador de áudio agora é inválido.</span><span class="sxs-lookup"><span data-stu-id="0564e-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="0564e-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0564e-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0564e-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0564e-108">Event values</span></span>

<span data-ttu-id="0564e-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0564e-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0564e-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0564e-110">VARTYPE</span></span>                | <span data-ttu-id="0564e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0564e-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0564e-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="0564e-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="0564e-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="0564e-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="0564e-114">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="0564e-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0564e-115">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="0564e-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0564e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0564e-116">Remarks</span></span>

<span data-ttu-id="0564e-117">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="0564e-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="0564e-118">O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonServerShutdown**.</span><span class="sxs-lookup"><span data-stu-id="0564e-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonServerShutdown**.</span></span>

<span data-ttu-id="0564e-119">O ponteiro [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se definido, não é útil, pois o fluxo de áudio não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="0564e-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0564e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0564e-120">Requirements</span></span>



| <span data-ttu-id="0564e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0564e-121">Requirement</span></span> | <span data-ttu-id="0564e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0564e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0564e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0564e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0564e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0564e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0564e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0564e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0564e-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0564e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0564e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0564e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0564e-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0564e-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0564e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0564e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0564e-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0564e-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0564e-131">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="0564e-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
