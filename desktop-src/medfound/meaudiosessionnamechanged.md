---
description: Gerado pelo processador de áudio quando o nome de exibição da sessão de áudio é alterado.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Evento MEAudioSessionNameChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647494"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="05a38-103">Evento MEAudioSessionNameChanged</span><span class="sxs-lookup"><span data-stu-id="05a38-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="05a38-104">Gerado pelo processador de áudio quando o nome de exibição da sessão de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="05a38-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="05a38-105">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05a38-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="05a38-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="05a38-106">Event values</span></span>

<span data-ttu-id="05a38-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="05a38-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="05a38-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="05a38-108">VARTYPE</span></span>                | <span data-ttu-id="05a38-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="05a38-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a38-110">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="05a38-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="05a38-111">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="05a38-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="05a38-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="05a38-112">Remarks</span></span>

<span data-ttu-id="05a38-113">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="05a38-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="05a38-114">O evento é disparado quando o renderizador de áudio recebe um evento [**IAudioSessionEvents:: Ondisplaynamechanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) da sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="05a38-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="05a38-115">Para obter o novo nome de exibição, chame [**IMFAudioPolicy:: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span><span class="sxs-lookup"><span data-stu-id="05a38-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05a38-116">Requirements</span></span>



| <span data-ttu-id="05a38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a38-117">Requirement</span></span> | <span data-ttu-id="05a38-118">Valor</span><span class="sxs-lookup"><span data-stu-id="05a38-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a38-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05a38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05a38-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05a38-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05a38-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05a38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05a38-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05a38-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05a38-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05a38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a38-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05a38-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a38-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="05a38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a38-126">**IMFAudioPolicy:: GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="05a38-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="05a38-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05a38-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="05a38-128">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="05a38-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
