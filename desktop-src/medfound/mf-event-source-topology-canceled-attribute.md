---
description: Especifica se a origem do sequenciador cancelou uma topologia.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Atributo MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755500"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="0a2b0-103">\_Atributo de topologia de origem de evento MF \_ \_ \_ cancelado</span><span class="sxs-lookup"><span data-stu-id="0a2b0-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="0a2b0-104">Especifica se a [origem do sequenciador](sequencer-source.md) cancelou uma topologia.</span><span class="sxs-lookup"><span data-stu-id="0a2b0-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a2b0-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0a2b0-105">Data type</span></span>

<span data-ttu-id="0a2b0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0a2b0-106">**UINT32**</span></span>

<span data-ttu-id="0a2b0-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="0a2b0-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a2b0-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a2b0-108">Remarks</span></span>

<span data-ttu-id="0a2b0-109">Esse atributo é usado com os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="0a2b0-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="0a2b0-110">MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="0a2b0-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="0a2b0-111">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="0a2b0-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="0a2b0-112">Se esse atributo estiver presente e for diferente de zero, significa que o segmento de apresentação terminou porque a origem do sequenciador cancelou a topologia.</span><span class="sxs-lookup"><span data-stu-id="0a2b0-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="0a2b0-113">Caso contrário, o segmento de apresentação terminou normalmente.</span><span class="sxs-lookup"><span data-stu-id="0a2b0-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="0a2b0-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0a2b0-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a2b0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a2b0-115">Requirements</span></span>



| <span data-ttu-id="0a2b0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a2b0-116">Requirement</span></span> | <span data-ttu-id="0a2b0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0a2b0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2b0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a2b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a2b0-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a2b0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0a2b0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a2b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a2b0-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a2b0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a2b0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a2b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a2b0-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b0-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a2b0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a2b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2b0-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a2b0-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a2b0-126">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="0a2b0-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a2b0-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0a2b0-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0a2b0-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="0a2b0-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0a2b0-129">Eventos de origem do Sequencer</span><span class="sxs-lookup"><span data-stu-id="0a2b0-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




