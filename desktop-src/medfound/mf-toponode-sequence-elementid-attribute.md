---
description: Especifica o elemento que contém este nó de origem.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Atributo MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798468"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="e0be7-103">\_ \_ Atributo ElementID da sequência MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="e0be7-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="e0be7-104">Especifica o elemento que contém este nó de origem.</span><span class="sxs-lookup"><span data-stu-id="e0be7-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0be7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e0be7-105">Data type</span></span>

<span data-ttu-id="e0be7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e0be7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0be7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0be7-107">Remarks</span></span>

<span data-ttu-id="e0be7-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="e0be7-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="e0be7-109">O pipeline de mídia usa esse atributo para descobrir quando as fontes de mídia fazem parte do mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="e0be7-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="e0be7-110">O pipeline trata todos os nós de origem que fazem parte do mesmo elemento como tendo o mesmo relógio.</span><span class="sxs-lookup"><span data-stu-id="e0be7-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="e0be7-111">Quando o pipeline enfileira uma nova topologia que contém nós de origem que fazem parte de um elemento que está presente na topologia anterior, o pipeline trata esses nós de origem como tendo o mesmo relógio que os nós de origem desse elemento na topologia anterior.</span><span class="sxs-lookup"><span data-stu-id="e0be7-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="e0be7-112">O pipeline de mídia não corrige carimbos de data/hora para nós de origem com taxas de clock diferentes.</span><span class="sxs-lookup"><span data-stu-id="e0be7-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="e0be7-113">Uma fonte de mídia que pode fornecer topologias deve implementar a interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ou a interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) .</span><span class="sxs-lookup"><span data-stu-id="e0be7-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="e0be7-114">Uma fonte de mídia que fornece topologias deve definir o atributo **\_ TOPONODE \_ Sequence \_ ElementID** em cada nó de origem que ele cria.</span><span class="sxs-lookup"><span data-stu-id="e0be7-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="e0be7-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e0be7-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0be7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0be7-116">Requirements</span></span>



| <span data-ttu-id="e0be7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0be7-117">Requirement</span></span> | <span data-ttu-id="e0be7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e0be7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0be7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0be7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0be7-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0be7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0be7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0be7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0be7-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0be7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0be7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0be7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0be7-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0be7-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0be7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0be7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0be7-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0be7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0be7-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e0be7-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e0be7-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e0be7-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e0be7-129">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="e0be7-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="e0be7-130">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="e0be7-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="e0be7-131">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e0be7-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e0be7-132">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="e0be7-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0be7-133">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="e0be7-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




