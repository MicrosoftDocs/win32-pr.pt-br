---
description: Gerado pelo processador de áudio quando o ícone de sessão de áudio é alterado.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788798"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="f0a2c-103">Evento MEAudioSessionIconChanged</span><span class="sxs-lookup"><span data-stu-id="f0a2c-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="f0a2c-104">Gerado pelo processador de áudio quando o ícone de sessão de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="f0a2c-105">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="f0a2c-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f0a2c-106">Event values</span></span>

<span data-ttu-id="f0a2c-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f0a2c-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a2c-108">VARTYPE</span></span>                | <span data-ttu-id="f0a2c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0a2c-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a2c-110">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="f0a2c-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="f0a2c-111">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="f0a2c-112">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="f0a2c-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="f0a2c-113">Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="f0a2c-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f0a2c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0a2c-114">Remarks</span></span>

<span data-ttu-id="f0a2c-115">Esse evento é enviado pelo coletor de fluxo do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="f0a2c-116">O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) da sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="f0a2c-117">Para obter o novo ícone, chame [**IMFAudioPolicy:: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="f0a2c-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a2c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a2c-118">Requirements</span></span>



| <span data-ttu-id="f0a2c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a2c-119">Requirement</span></span> | <span data-ttu-id="f0a2c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f0a2c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a2c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a2c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a2c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0a2c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0a2c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a2c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a2c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0a2c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0a2c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0a2c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a2c-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0a2c-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a2c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0a2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a2c-128">**IMFAudioPolicy::GetIconPath**</span><span class="sxs-lookup"><span data-stu-id="f0a2c-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="f0a2c-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0a2c-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f0a2c-130">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="f0a2c-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
