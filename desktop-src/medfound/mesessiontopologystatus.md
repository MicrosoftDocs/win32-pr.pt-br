---
description: Gerado pela sessão de mídia quando o status de uma topologia é alterado.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921282"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="0349c-103">Evento MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="0349c-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="0349c-104">Gerado pela sessão de mídia quando o status de uma topologia é alterado.</span><span class="sxs-lookup"><span data-stu-id="0349c-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="0349c-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0349c-105">Event values</span></span>

<span data-ttu-id="0349c-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0349c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0349c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0349c-107">VARTYPE</span></span>                | <span data-ttu-id="0349c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0349c-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0349c-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="0349c-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0349c-110">Ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.</span><span class="sxs-lookup"><span data-stu-id="0349c-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0349c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0349c-111">Attributes</span></span>

<span data-ttu-id="0349c-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="0349c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0349c-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="0349c-113">Attribute</span></span>                                                                            | <span data-ttu-id="0349c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0349c-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0349c-115">**\_status da \_ topologia de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="0349c-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="0349c-116">Especifica o novo status da topologia.</span><span class="sxs-lookup"><span data-stu-id="0349c-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0349c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0349c-117">Remarks</span></span>

<span data-ttu-id="0349c-118">Para obter um exemplo de código que recupera o ponteiro [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) do evento, consulte evento [MESessionTopologySet](mesessiontopologyset.md) .</span><span class="sxs-lookup"><span data-stu-id="0349c-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0349c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0349c-119">Requirements</span></span>



| <span data-ttu-id="0349c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0349c-120">Requirement</span></span> | <span data-ttu-id="0349c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0349c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0349c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0349c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0349c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0349c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0349c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0349c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0349c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0349c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0349c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0349c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0349c-127"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0349c-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0349c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0349c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0349c-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0349c-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




