---
description: Especifica se o pipeline aplica a marcação neste nó. A marcação é o ponto em que uma apresentação termina. Se os componentes de pipeline geram dados além do ponto de marcação, os dados não são renderizados.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Atributo MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798469"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="f20b2-105">\_Atributo de \_ marcação MF TOPONODE \_ aqui</span><span class="sxs-lookup"><span data-stu-id="f20b2-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="f20b2-106">Especifica se o pipeline aplica a marcação neste nó.</span><span class="sxs-lookup"><span data-stu-id="f20b2-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="f20b2-107">A marcação é o ponto em que uma apresentação termina.</span><span class="sxs-lookup"><span data-stu-id="f20b2-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="f20b2-108">Se os componentes de pipeline geram dados além do ponto de marcação, os dados não são renderizados.</span><span class="sxs-lookup"><span data-stu-id="f20b2-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="f20b2-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f20b2-109">Data type</span></span>

<span data-ttu-id="f20b2-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f20b2-110">**UINT32**</span></span>

<span data-ttu-id="f20b2-111">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="f20b2-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f20b2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f20b2-112">Remarks</span></span>

<span data-ttu-id="f20b2-113">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="f20b2-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="f20b2-114">Se esse atributo for **true**, o pipeline de Media Foundation apara as amostras de saída deste nó para corresponder à hora de parada da apresentação.</span><span class="sxs-lookup"><span data-stu-id="f20b2-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="f20b2-115">O carregador de topologia define esse atributo ao resolver uma topologia.</span><span class="sxs-lookup"><span data-stu-id="f20b2-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="f20b2-116">A maioria dos aplicativos não precisa definir ou recuperar esse atributo.</span><span class="sxs-lookup"><span data-stu-id="f20b2-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="f20b2-117">É recomendável que exatamente um nó em cada ramificação da topologia tenha esse atributo definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="f20b2-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="f20b2-118">Uma ramificação de topologia é definida como o caminho de um nó de origem para um nó de saída.</span><span class="sxs-lookup"><span data-stu-id="f20b2-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="f20b2-119">Dentro de um Branch, os \_ atributos MF TOPONODE \_ markout \_ e [MF \_ TOPONODE \_ \_ aqui](mf-toponode-markin-here-attribute.md) devem ser definidos no mesmo nó do Branch.</span><span class="sxs-lookup"><span data-stu-id="f20b2-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="f20b2-120">Eles não podem ser definidos em nós diferentes dentro da mesma ramificação.</span><span class="sxs-lookup"><span data-stu-id="f20b2-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="f20b2-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f20b2-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f20b2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20b2-122">Requirements</span></span>



| <span data-ttu-id="f20b2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20b2-123">Requirement</span></span> | <span data-ttu-id="f20b2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f20b2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f20b2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f20b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f20b2-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f20b2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f20b2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f20b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f20b2-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f20b2-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f20b2-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f20b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f20b2-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f20b2-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f20b2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f20b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20b2-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f20b2-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f20b2-133">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f20b2-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f20b2-134">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="f20b2-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f20b2-135">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f20b2-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f20b2-136">**\_Mark TOPONODE do MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="f20b2-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="f20b2-137">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="f20b2-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




