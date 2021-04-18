---
description: Esses sinalizadores fornecem informações adicionais sobre os parâmetros de efeito.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780676"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="974bb-103">\_Parâmetro D3DX</span><span class="sxs-lookup"><span data-stu-id="974bb-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="974bb-104">Esses sinalizadores fornecem informações adicionais sobre os parâmetros de efeito.</span><span class="sxs-lookup"><span data-stu-id="974bb-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="974bb-105">Constantes de parâmetro de efeito são usadas por [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="974bb-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="974bb-106">Constante</span><span class="sxs-lookup"><span data-stu-id="974bb-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="974bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="974bb-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="974bb-108"><dt>**\_Anotação de parâmetro D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="974bb-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="974bb-109">Esse parâmetro é marcado como uma anotação.</span><span class="sxs-lookup"><span data-stu-id="974bb-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="974bb-110">Consulte [adicionar informações para parâmetros de efeito com anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="974bb-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="974bb-111"><dt>**\_Literal de parâmetro D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="974bb-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="974bb-112">Esse parâmetro é marcado como um valor literal.</span><span class="sxs-lookup"><span data-stu-id="974bb-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="974bb-113">Os parâmetros literais não podem ser alterados após a compilação, permitindo que o compilador Otimize seu uso.</span><span class="sxs-lookup"><span data-stu-id="974bb-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="974bb-114">Os parâmetros compartilhados não podem ser marcados como um literal.</span><span class="sxs-lookup"><span data-stu-id="974bb-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="974bb-115">Consulte [usos e literais (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="974bb-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="974bb-116"><dt>**\_Parâmetro D3DX \_ compartilhado**</dt></span><span class="sxs-lookup"><span data-stu-id="974bb-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="974bb-117">O valor de um parâmetro será compartilhado por todos os efeitos no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="974bb-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="974bb-118">Alterar o valor em um efeito irá alterá-lo em todos os efeitos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="974bb-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="974bb-119">Consulte [compartilhando parâmetros](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="974bb-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="974bb-120">**D3DX \_ O parâmetro \_ compartilhado** não pode ser combinado com o **\_ parâmetro D3DX \_ literal** ou a **\_ \_ anotação de parâmetro D3DX**.</span><span class="sxs-lookup"><span data-stu-id="974bb-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="974bb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="974bb-121">Requirements</span></span>



| <span data-ttu-id="974bb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="974bb-122">Requirement</span></span> | <span data-ttu-id="974bb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="974bb-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="974bb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="974bb-124">Header</span></span><br/> | <dl> <span data-ttu-id="974bb-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="974bb-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="974bb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="974bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="974bb-127">Constantes de efeito</span><span class="sxs-lookup"><span data-stu-id="974bb-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




