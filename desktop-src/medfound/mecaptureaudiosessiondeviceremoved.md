---
description: Enviado por uma fonte de captura de áudio quando o dispositivo é removido.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Evento MECaptureAudioSessionDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765171"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a><span data-ttu-id="a9da0-103">Evento MECaptureAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="a9da0-103">MECaptureAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="a9da0-104">Enviado por uma fonte de captura de áudio quando o dispositivo é removido.</span><span class="sxs-lookup"><span data-stu-id="a9da0-104">Sent by an audio capture source when the device is removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="a9da0-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a9da0-105">Event values</span></span>

<span data-ttu-id="a9da0-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a9da0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a9da0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a9da0-107">VARTYPE</span></span>               | <span data-ttu-id="a9da0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9da0-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="a9da0-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="a9da0-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="a9da0-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="a9da0-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a9da0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9da0-111">Remarks</span></span>

<span data-ttu-id="a9da0-112">Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="a9da0-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="a9da0-113">A origem de captura envia esse evento quando recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonDeviceRemoval**.</span><span class="sxs-lookup"><span data-stu-id="a9da0-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9da0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9da0-114">Requirements</span></span>



| <span data-ttu-id="a9da0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9da0-115">Requirement</span></span> | <span data-ttu-id="a9da0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a9da0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9da0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9da0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9da0-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9da0-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a9da0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9da0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9da0-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9da0-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9da0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9da0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9da0-122"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9da0-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9da0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9da0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9da0-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9da0-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
