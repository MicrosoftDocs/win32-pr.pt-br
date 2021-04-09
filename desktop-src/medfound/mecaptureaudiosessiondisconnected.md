---
description: Enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão do WTS (serviços de terminal do Windows).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090814"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="4baf5-103">Evento MECaptureAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="4baf5-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="4baf5-104">Enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão do WTS (serviços de terminal do Windows).</span><span class="sxs-lookup"><span data-stu-id="4baf5-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="4baf5-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="4baf5-105">Event values</span></span>

<span data-ttu-id="4baf5-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4baf5-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4baf5-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4baf5-107">VARTYPE</span></span>               | <span data-ttu-id="4baf5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4baf5-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="4baf5-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="4baf5-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="4baf5-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="4baf5-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4baf5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4baf5-111">Remarks</span></span>

<span data-ttu-id="4baf5-112">Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="4baf5-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="4baf5-113">A origem de captura envia esse evento quando recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonSessionDisconnected**.</span><span class="sxs-lookup"><span data-stu-id="4baf5-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4baf5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4baf5-114">Requirements</span></span>



| <span data-ttu-id="4baf5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4baf5-115">Requirement</span></span> | <span data-ttu-id="4baf5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4baf5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4baf5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4baf5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4baf5-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4baf5-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4baf5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4baf5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4baf5-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4baf5-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4baf5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4baf5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4baf5-122"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4baf5-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4baf5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4baf5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4baf5-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4baf5-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
