---
description: Especifica se o pipeline apara amostras.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Atributo MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165015"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="348ba-103">\_Topologia MF \_ sem \_ marca de marcação \_ atributo de marcação</span><span class="sxs-lookup"><span data-stu-id="348ba-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="348ba-104">Especifica se o pipeline apara amostras.</span><span class="sxs-lookup"><span data-stu-id="348ba-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="348ba-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="348ba-105">Data type</span></span>

<span data-ttu-id="348ba-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="348ba-106">**UINT32**</span></span>

<span data-ttu-id="348ba-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="348ba-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="348ba-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="348ba-108">Remarks</span></span>

<span data-ttu-id="348ba-109">Por padrão, o pipeline corta exemplos para corresponder aos tempos de apresentação corretos.</span><span class="sxs-lookup"><span data-stu-id="348ba-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="348ba-110">A remoção é feita nos nós de topologia que têm [**a \_ marca de TOPONODE MF \_ \_ aqui**](mf-toponode-markin-here-attribute.md) e os atributos [**MF \_ TOPONODE \_ markout \_ aqui**](mf-toponode-markout-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="348ba-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="348ba-111">Se a **\_ topologia MF \_ sem \_ marca \_** de marcação atributo de marcação estiver definida como **true** na topologia, o pipeline não cortará amostras e os atributos **MF \_ TOPONODE \_ marking \_ aqui** e **MF \_ TOPONODE \_ markout \_** serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="348ba-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="348ba-112">Se o atributo não estiver definido ou tiver o valor **false**, o pipeline cortará os exemplos.</span><span class="sxs-lookup"><span data-stu-id="348ba-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="348ba-113">Um aplicativo pode definir a **\_ topologia MF \_ sem \_ marca \_** de marcação atributo de marcação como **true** se o aplicativo receber amostras compactadas do pipeline e precisar obter todos os quadros-chave que, de outra forma, podem ser cortados.</span><span class="sxs-lookup"><span data-stu-id="348ba-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="348ba-114">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="348ba-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="348ba-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="348ba-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="348ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="348ba-116">Requirements</span></span>



| <span data-ttu-id="348ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="348ba-117">Requirement</span></span> | <span data-ttu-id="348ba-118">Valor</span><span class="sxs-lookup"><span data-stu-id="348ba-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="348ba-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="348ba-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="348ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="348ba-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="348ba-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="348ba-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="348ba-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="348ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="348ba-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="348ba-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348ba-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="348ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348ba-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="348ba-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="348ba-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="348ba-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="348ba-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="348ba-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="348ba-129">**\_Mark TOPONODE do MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="348ba-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="348ba-130">**\_marcação de TOPONODE MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="348ba-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="348ba-131">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="348ba-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




