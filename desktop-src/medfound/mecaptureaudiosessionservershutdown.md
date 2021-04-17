---
description: Enviado por uma fonte de captura de áudio quando a sessão de captura de áudio é desconectada devido ao desligamento do servidor de áudio.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Evento MECaptureAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812126"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="0b4e8-103">Evento MECaptureAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="0b4e8-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="0b4e8-104">Enviado por uma fonte de captura de áudio quando a sessão de captura de áudio é desconectada devido ao desligamento do servidor de áudio.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="0b4e8-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0b4e8-105">Event values</span></span>

<span data-ttu-id="0b4e8-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0b4e8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0b4e8-107">VARTYPE</span></span>               | <span data-ttu-id="0b4e8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b4e8-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="0b4e8-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="0b4e8-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="0b4e8-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0b4e8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b4e8-111">Requirements</span></span>



| <span data-ttu-id="0b4e8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b4e8-112">Requirement</span></span> | <span data-ttu-id="0b4e8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0b4e8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4e8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b4e8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0b4e8-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b4e8-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="0b4e8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b4e8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0b4e8-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b4e8-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b4e8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b4e8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b4e8-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b4e8-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b4e8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b4e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4e8-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b4e8-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




