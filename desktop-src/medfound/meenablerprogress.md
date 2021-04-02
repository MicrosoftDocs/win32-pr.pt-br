---
description: Sinaliza o progresso de um objeto de habilitador de conteúdo. Os objetos que expõem a interface IMFContentEnabler podem gerar esse evento para notificar o aplicativo sobre o progresso das ações de habilitadores de conteúdo.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165048"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="57a8a-104">Evento MEEnablerProgress</span><span class="sxs-lookup"><span data-stu-id="57a8a-104">MEEnablerProgress event</span></span>

<span data-ttu-id="57a8a-105">Sinaliza o progresso de um objeto de habilitador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="57a8a-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="57a8a-106">Os objetos que expõem a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) podem gerar esse evento para notificar o aplicativo sobre o progresso das ações do habilitador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="57a8a-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="57a8a-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="57a8a-107">Event values</span></span>

<span data-ttu-id="57a8a-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="57a8a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="57a8a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="57a8a-109">VARTYPE</span></span>               | <span data-ttu-id="57a8a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="57a8a-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="57a8a-111">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="57a8a-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="57a8a-112">Cadeia de caracteres largos que descreve o progresso.</span><span class="sxs-lookup"><span data-stu-id="57a8a-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="57a8a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="57a8a-113">Remarks</span></span>

<span data-ttu-id="57a8a-114">Para receber esse evento, consulte a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="57a8a-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="57a8a-115">Em seguida, chame [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), conforme descrito no tópico [geradores de eventos de mídia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="57a8a-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a8a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a8a-116">Requirements</span></span>



| <span data-ttu-id="57a8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a8a-117">Requirement</span></span> | <span data-ttu-id="57a8a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="57a8a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a8a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57a8a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57a8a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57a8a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57a8a-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57a8a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57a8a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57a8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a8a-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57a8a-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a8a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="57a8a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a8a-126">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="57a8a-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="57a8a-127">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="57a8a-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="57a8a-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57a8a-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




