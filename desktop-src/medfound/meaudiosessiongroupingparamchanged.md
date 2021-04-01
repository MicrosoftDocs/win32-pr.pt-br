---
description: Gerado pelo processador de áudio quando os parâmetros de agrupamento mudam para a sessão de áudio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Evento MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164717"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="b5b24-103">Evento MEAudioSessionGroupingParamChanged</span><span class="sxs-lookup"><span data-stu-id="b5b24-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="b5b24-104">Gerado pelo processador de áudio quando os parâmetros de agrupamento mudam para a sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="b5b24-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="b5b24-105">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b5b24-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="b5b24-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b5b24-106">Event values</span></span>

<span data-ttu-id="b5b24-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b5b24-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b5b24-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b5b24-108">VARTYPE</span></span>                | <span data-ttu-id="b5b24-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5b24-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b24-110">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="b5b24-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="b5b24-111">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="b5b24-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b5b24-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5b24-112">Remarks</span></span>

<span data-ttu-id="b5b24-113">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="b5b24-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="b5b24-114">O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) da sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="b5b24-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="b5b24-115">Para obter os novos parâmetros de agrupamento, chame [**IMFAudioPolicy:: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="b5b24-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5b24-116">Requirements</span></span>



| <span data-ttu-id="b5b24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5b24-117">Requirement</span></span> | <span data-ttu-id="b5b24-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b5b24-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b24-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5b24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b24-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5b24-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5b24-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5b24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b24-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5b24-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5b24-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5b24-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5b24-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5b24-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b24-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5b24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b24-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5b24-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b5b24-127">**IMFAudioPolicy::GetGroupingParam**</span><span class="sxs-lookup"><span data-stu-id="b5b24-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="b5b24-128">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="b5b24-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
