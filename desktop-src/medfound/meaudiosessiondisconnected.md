---
description: Gerado pelo processador de áudio quando a sessão de áudio é desconectada de uma sessão dos serviços de terminal do Windows (WTS). O processador de áudio agora é inválido.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Evento MEAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791089"
---
# <a name="meaudiosessiondisconnected-event"></a><span data-ttu-id="89252-104">Evento MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="89252-104">MEAudioSessionDisconnected event</span></span>

<span data-ttu-id="89252-105">Gerado pelo processador de áudio quando a sessão de áudio é desconectada de uma sessão dos serviços de terminal do Windows (WTS).</span><span class="sxs-lookup"><span data-stu-id="89252-105">Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session.</span></span> <span data-ttu-id="89252-106">O processador de áudio agora é inválido.</span><span class="sxs-lookup"><span data-stu-id="89252-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="89252-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89252-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="89252-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="89252-108">Event values</span></span>

<span data-ttu-id="89252-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="89252-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="89252-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="89252-110">VARTYPE</span></span>                | <span data-ttu-id="89252-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="89252-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="89252-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="89252-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="89252-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="89252-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="89252-114">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="89252-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="89252-115">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="89252-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="89252-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="89252-116">Remarks</span></span>

<span data-ttu-id="89252-117">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="89252-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="89252-118">O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a DisconnectReasonSessionDisconnected.</span><span class="sxs-lookup"><span data-stu-id="89252-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonSessionDisconnected.</span></span>

<span data-ttu-id="89252-119">O ponteiro [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se definido, não é útil, pois o fluxo de áudio não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="89252-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="89252-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89252-120">Requirements</span></span>



| <span data-ttu-id="89252-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="89252-121">Requirement</span></span> | <span data-ttu-id="89252-122">Valor</span><span class="sxs-lookup"><span data-stu-id="89252-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89252-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89252-123">Minimum supported client</span></span><br/> | <span data-ttu-id="89252-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89252-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89252-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89252-125">Minimum supported server</span></span><br/> | <span data-ttu-id="89252-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89252-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89252-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89252-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="89252-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89252-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89252-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="89252-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89252-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89252-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="89252-131">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="89252-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
