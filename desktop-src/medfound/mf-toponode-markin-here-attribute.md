---
description: Especifica se o pipeline aplica o marca-in neste nó.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Atributo MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765331"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="01a2d-103">\_TOPONODE MF \_ \_ aqui atributo</span><span class="sxs-lookup"><span data-stu-id="01a2d-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="01a2d-104">Especifica se o pipeline aplica o marca-in neste nó.</span><span class="sxs-lookup"><span data-stu-id="01a2d-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="01a2d-105">Mark-in é o ponto em que uma apresentação é iniciada.</span><span class="sxs-lookup"><span data-stu-id="01a2d-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="01a2d-106">Se os componentes de pipeline geram dados antes do ponto de marcação, os dados não são renderizados.</span><span class="sxs-lookup"><span data-stu-id="01a2d-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="01a2d-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="01a2d-107">Data type</span></span>

<span data-ttu-id="01a2d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="01a2d-108">**UINT32**</span></span>

<span data-ttu-id="01a2d-109">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="01a2d-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a2d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a2d-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01a2d-111">A maioria dos aplicativos não precisa usar esse atributo.</span><span class="sxs-lookup"><span data-stu-id="01a2d-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="01a2d-112">A [sessão de mídia](media-session.md) define automaticamente esse atributo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="01a2d-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="01a2d-113">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="01a2d-113">This attribute applies to all node types.</span></span> <span data-ttu-id="01a2d-114">Se o atributo for **true**, o pipeline de Media Foundation apara as amostras de saída deste nó para corresponder à hora de início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="01a2d-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="01a2d-115">O carregador de topologia define esse atributo ao resolver uma topologia.</span><span class="sxs-lookup"><span data-stu-id="01a2d-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="01a2d-116">É recomendável que exatamente um nó em cada ramificação da topologia tenha esse atributo definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="01a2d-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="01a2d-117">Uma ramificação de topologia é definida como o caminho de um nó de origem para um nó de saída.</span><span class="sxs-lookup"><span data-stu-id="01a2d-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="01a2d-118">Dentro de um Branch, os atributos [MF \_ TOPONODE \_ markout \_ ](mf-toponode-markout-here-attribute.md) e MF \_ TOPONODE \_ \_ aqui devem ser definidos no mesmo nó do Branch.</span><span class="sxs-lookup"><span data-stu-id="01a2d-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="01a2d-119">Eles não podem ser definidos em nós diferentes dentro da mesma ramificação.</span><span class="sxs-lookup"><span data-stu-id="01a2d-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="01a2d-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="01a2d-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a2d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a2d-121">Requirements</span></span>



| <span data-ttu-id="01a2d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a2d-122">Requirement</span></span> | <span data-ttu-id="01a2d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="01a2d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01a2d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a2d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="01a2d-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01a2d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01a2d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a2d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="01a2d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01a2d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01a2d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01a2d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a2d-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a2d-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a2d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="01a2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a2d-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01a2d-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01a2d-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="01a2d-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="01a2d-133">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="01a2d-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="01a2d-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="01a2d-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="01a2d-135">**\_marcação de TOPONODE MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="01a2d-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="01a2d-136">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="01a2d-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




