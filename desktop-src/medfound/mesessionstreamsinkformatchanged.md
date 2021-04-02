---
description: Gerado pela sessão de mídia quando o formato é alterado em um coletor de mídia.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165040"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="9326c-103">Evento MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="9326c-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="9326c-104">Gerado pela sessão de mídia quando o formato é alterado em um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="9326c-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="9326c-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9326c-105">Event values</span></span>

<span data-ttu-id="9326c-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9326c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9326c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9326c-107">VARTYPE</span></span>              | <span data-ttu-id="9326c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9326c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9326c-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="9326c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9326c-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="9326c-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="9326c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9326c-111">Attributes</span></span>

<span data-ttu-id="9326c-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="9326c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="9326c-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="9326c-113">Attribute</span></span>                                                                    | <span data-ttu-id="9326c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9326c-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9326c-115">**\_nó de \_ saída do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="9326c-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="9326c-116">Identifica o nó de topologia para o coletor de mídia cujo formato foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9326c-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="9326c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9326c-117">Requirements</span></span>



| <span data-ttu-id="9326c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9326c-118">Requirement</span></span> | <span data-ttu-id="9326c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9326c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9326c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9326c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9326c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9326c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9326c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9326c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9326c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9326c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9326c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9326c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9326c-125"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9326c-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9326c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9326c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9326c-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9326c-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




