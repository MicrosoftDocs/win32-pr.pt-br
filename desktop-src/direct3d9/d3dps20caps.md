---
description: Sinalizadores de capacidade do sombreador de pixel.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995263"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="bddbb-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bddbb-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="bddbb-104">Sinalizadores de capacidade do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bddbb-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="bddbb-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="bddbb-105">\#define</span></span>                                     | <span data-ttu-id="bddbb-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bddbb-106">Value</span></span>          | <span data-ttu-id="bddbb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bddbb-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddbb-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="bddbb-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="bddbb-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="bddbb-109">(1 << 0)</span></span> | <span data-ttu-id="bddbb-110">Há suporte para swizzling arbitrários.</span><span class="sxs-lookup"><span data-stu-id="bddbb-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="bddbb-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="bddbb-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="bddbb-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="bddbb-112">(1 << 1)</span></span> | <span data-ttu-id="bddbb-113">Há suporte para instruções de gradiente.</span><span class="sxs-lookup"><span data-stu-id="bddbb-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="bddbb-114">D3DD3DPSHADERCAPS2 \_ 0 \_ predicação</span><span class="sxs-lookup"><span data-stu-id="bddbb-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="bddbb-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="bddbb-115">(1 << 2)</span></span> | <span data-ttu-id="bddbb-116">Há suporte para predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="bddbb-116">Instruction predication is supported.</span></span> <span data-ttu-id="bddbb-117">Consulte [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="bddbb-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="bddbb-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="bddbb-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="bddbb-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="bddbb-119">(1 << 3)</span></span> | <span data-ttu-id="bddbb-120">Não há limite para o número de leituras dependentes por instrução.</span><span class="sxs-lookup"><span data-stu-id="bddbb-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="bddbb-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="bddbb-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="bddbb-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="bddbb-122">(1 << 4)</span></span> | <span data-ttu-id="bddbb-123">Não há limite para o número de instruções Tex.</span><span class="sxs-lookup"><span data-stu-id="bddbb-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="bddbb-124">D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bddbb-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="bddbb-125">24</span><span class="sxs-lookup"><span data-stu-id="bddbb-125">24</span></span>             | <span data-ttu-id="bddbb-126">O nível máximo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="bddbb-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="bddbb-127">D3DPS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bddbb-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="bddbb-128">0</span><span class="sxs-lookup"><span data-stu-id="bddbb-128">0</span></span>              | <span data-ttu-id="bddbb-129">O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="bddbb-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="bddbb-130">D3DPS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="bddbb-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="bddbb-131">32</span><span class="sxs-lookup"><span data-stu-id="bddbb-131">32</span></span>             | <span data-ttu-id="bddbb-132">O driver dará suporte a, no máximo, esse número de registros temporários.</span><span class="sxs-lookup"><span data-stu-id="bddbb-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="bddbb-133">D3DPS20 \_ min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="bddbb-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="bddbb-134">12</span><span class="sxs-lookup"><span data-stu-id="bddbb-134">12</span></span>             | <span data-ttu-id="bddbb-135">O driver dará suporte a, pelo menos, esse número de registros temporários.</span><span class="sxs-lookup"><span data-stu-id="bddbb-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="bddbb-136">D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bddbb-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="bddbb-137">4</span><span class="sxs-lookup"><span data-stu-id="bddbb-137">4</span></span>              | <span data-ttu-id="bddbb-138">A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="bddbb-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="bddbb-139">D3DPS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bddbb-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="bddbb-140">1</span><span class="sxs-lookup"><span data-stu-id="bddbb-140">1</span></span>              | <span data-ttu-id="bddbb-141">A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="bddbb-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="bddbb-142">D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="bddbb-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="bddbb-143">512</span><span class="sxs-lookup"><span data-stu-id="bddbb-143">512</span></span>            | <span data-ttu-id="bddbb-144">O driver dará suporte a, no máximo, várias instruções.</span><span class="sxs-lookup"><span data-stu-id="bddbb-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="bddbb-145">D3DPS20 \_ min \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="bddbb-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="bddbb-146">96</span><span class="sxs-lookup"><span data-stu-id="bddbb-146">96</span></span>             | <span data-ttu-id="bddbb-147">O driver dará suporte a pelo menos este número de instruções.</span><span class="sxs-lookup"><span data-stu-id="bddbb-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="bddbb-148">Essas constantes são usadas pelo membro D3DPSHADERCAPS2 \_ 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="bddbb-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="bddbb-149">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="bddbb-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="bddbb-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bddbb-150">Header</span></span>                   | <span data-ttu-id="bddbb-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="bddbb-151">d3d9caps.h</span></span> |
| <span data-ttu-id="bddbb-152">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="bddbb-152">Minimum operating system</span></span> | <span data-ttu-id="bddbb-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bddbb-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bddbb-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bddbb-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bddbb-155">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="bddbb-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="bddbb-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="bddbb-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
