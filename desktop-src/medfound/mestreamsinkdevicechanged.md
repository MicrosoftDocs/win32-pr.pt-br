---
description: Gerado pelos coletores de fluxo do processador de vídeo aprimorado (EVR) se o dispositivo de vídeo for alterado.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793396"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="9f74e-103">Evento MEStreamSinkDeviceChanged</span><span class="sxs-lookup"><span data-stu-id="9f74e-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="9f74e-104">Gerado pelos coletores de fluxo do processador de vídeo aprimorado (EVR) se o dispositivo de vídeo for alterado.</span><span class="sxs-lookup"><span data-stu-id="9f74e-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="9f74e-105">Por exemplo, o EVR gera esse evento quando recebe um evento [**de \_ exibição \_ de EC alterado**](../directshow/ec-display-changed.md) .</span><span class="sxs-lookup"><span data-stu-id="9f74e-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="9f74e-106">O pipeline de Media Foundation responde a esse evento Reenviando todas as solicitações de exemplo que falharam enquanto o dispositivo estava sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="9f74e-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="9f74e-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9f74e-107">Event values</span></span>

<span data-ttu-id="9f74e-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9f74e-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9f74e-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9f74e-109">VARTYPE</span></span>              | <span data-ttu-id="9f74e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f74e-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9f74e-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="9f74e-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9f74e-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="9f74e-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="9f74e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f74e-113">Requirements</span></span>



| <span data-ttu-id="9f74e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f74e-114">Requirement</span></span> | <span data-ttu-id="9f74e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9f74e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f74e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f74e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f74e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f74e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f74e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f74e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f74e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f74e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f74e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f74e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f74e-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f74e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f74e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f74e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f74e-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f74e-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9f74e-124">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="9f74e-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
