---
title: Constantes de TS_ATTR_ (Textstor. h)
description: As \_ constantes TS attr \_ \ são usadas para obter e alterar os valores dos atributos do documento. Essas constantes formam possíveis valores de sinalizadores de campo de bits nos métodos ITextStoreACP e ITextStoreAnchor.
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455573"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="146d9-104">\_Constantes de atributo TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="146d9-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="146d9-105">As \_ constantes de atributo TS \_ \* são usadas para obter e alterar os valores dos atributos do documento.</span><span class="sxs-lookup"><span data-stu-id="146d9-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="146d9-106">Essas constantes formam possíveis valores de sinalizadores de campo de bits nos métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="146d9-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="146d9-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="146d9-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="146d9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="146d9-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="146d9-109"><dt>**TS \_ ATTR \_ localizar \_ versões anteriores**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="146d9-110">Pesquisar retroativamente a partir do caractere inicial ou da posição da âncora para a posição em que ocorre uma transição em um valor de atributo de documento.</span><span class="sxs-lookup"><span data-stu-id="146d9-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="146d9-111">O padrão é Pesquisar em frente.</span><span class="sxs-lookup"><span data-stu-id="146d9-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="146d9-112"><dt>**TS \_ Atributo de \_ localização de local \_ \_ attr**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="146d9-113">Retorna o número de caracteres entre o caractere inicial ou a posição da âncora (**acpStart** em [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) ou **PaStart** em [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) e a posição na qual ocorre uma transição de atributo.</span><span class="sxs-lookup"><span data-stu-id="146d9-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="146d9-114"><dt>**TS \_ ATTR \_ localizar \_ UPDATESTART**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="146d9-115">Usado por [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) para posicionar a âncora de entrada na próxima transição de atributo, se uma for encontrada.</span><span class="sxs-lookup"><span data-stu-id="146d9-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="146d9-116">Caso contrário, a âncora de entrada não será modificada.</span><span class="sxs-lookup"><span data-stu-id="146d9-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="146d9-117"><dt>**TS \_ Atributo \_ de \_ localização \_ do attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="146d9-118">Carregue os valores de atributo de documento com suporte na estrutura [TS \_ ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .</span><span class="sxs-lookup"><span data-stu-id="146d9-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="146d9-119"><dt>**TS \_ \_ \_ \_ Término da localização**</dt> de ' attr ' <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="146d9-120">Usado por [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) e [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) para obter os valores de atributo de documento que terminam no caractere ou posição de âncora especificada.</span><span class="sxs-lookup"><span data-stu-id="146d9-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="146d9-121"><dt>**TS \_ ATTR \_ localizar \_ oculto**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="146d9-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="146d9-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="146d9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="146d9-123">Requirements</span></span>



| <span data-ttu-id="146d9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="146d9-124">Requirement</span></span> | <span data-ttu-id="146d9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="146d9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="146d9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="146d9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="146d9-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="146d9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="146d9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="146d9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="146d9-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="146d9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="146d9-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="146d9-130">Redistributable</span></span><br/>          | <span data-ttu-id="146d9-131">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="146d9-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="146d9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="146d9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="146d9-133"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="146d9-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="146d9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="146d9-135"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="146d9-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="146d9-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="146d9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="146d9-137">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="146d9-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="146d9-138">\_ATTRVAL TS</span><span class="sxs-lookup"><span data-stu-id="146d9-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="146d9-139">ITextStoreACP:: FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="146d9-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="146d9-140">ITextStoreACP:: RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="146d9-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="146d9-141">ITextStoreAnchor::FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="146d9-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="146d9-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="146d9-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





