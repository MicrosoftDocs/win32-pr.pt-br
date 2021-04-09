---
description: Sinalizadores de capacidade do sombreador de pixel.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089563"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="d0a85-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0a85-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="d0a85-104">Sinalizadores de capacidade do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="d0a85-104">Pixel shader capability flags.</span></span>



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a85-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="d0a85-105">\#define</span></span>                                     | <span data-ttu-id="d0a85-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d0a85-106">Value</span></span>          | <span data-ttu-id="d0a85-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0a85-107">Description</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="d0a85-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="d0a85-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="d0a85-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="d0a85-109">(1 << 0)</span></span> | <span data-ttu-id="d0a85-110">Há suporte para swizzling arbitrários.</span><span class="sxs-lookup"><span data-stu-id="d0a85-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d0a85-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="d0a85-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="d0a85-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="d0a85-112">(1 << 1)</span></span> | <span data-ttu-id="d0a85-113">Há suporte para instruções de gradiente.</span><span class="sxs-lookup"><span data-stu-id="d0a85-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="d0a85-114">D3DD3DPSHADERCAPS2 \_ 0 \_ predicação</span><span class="sxs-lookup"><span data-stu-id="d0a85-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="d0a85-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="d0a85-115">(1 << 2)</span></span> | <span data-ttu-id="d0a85-116">Há suporte para predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="d0a85-116">Instruction predication is supported.</span></span> <span data-ttu-id="d0a85-117">Consulte [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="d0a85-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="d0a85-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="d0a85-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="d0a85-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="d0a85-119">(1 << 3)</span></span> | <span data-ttu-id="d0a85-120">Não há limite para o número de leituras dependentes por instrução.</span><span class="sxs-lookup"><span data-stu-id="d0a85-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="d0a85-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="d0a85-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="d0a85-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="d0a85-122">(1 << 4)</span></span> | <span data-ttu-id="d0a85-123">Não há limite para o número de instruções Tex.</span><span class="sxs-lookup"><span data-stu-id="d0a85-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d0a85-124">D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="d0a85-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="d0a85-125">24</span><span class="sxs-lookup"><span data-stu-id="d0a85-125">24</span></span>             | <span data-ttu-id="d0a85-126">O nível máximo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="d0a85-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="d0a85-127">D3DPS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="d0a85-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="d0a85-128">0</span><span class="sxs-lookup"><span data-stu-id="d0a85-128">0</span></span>              | <span data-ttu-id="d0a85-129">O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="d0a85-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="d0a85-130">D3DPS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="d0a85-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="d0a85-131">32</span><span class="sxs-lookup"><span data-stu-id="d0a85-131">32</span></span>             | <span data-ttu-id="d0a85-132">O driver dará suporte a, no máximo, esse número de registros temporários.</span><span class="sxs-lookup"><span data-stu-id="d0a85-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="d0a85-133">D3DPS20 \_ min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="d0a85-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="d0a85-134">12</span><span class="sxs-lookup"><span data-stu-id="d0a85-134">12</span></span>             | <span data-ttu-id="d0a85-135">O driver dará suporte a, pelo menos, esse número de registros temporários.</span><span class="sxs-lookup"><span data-stu-id="d0a85-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d0a85-136">D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="d0a85-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="d0a85-137">4</span><span class="sxs-lookup"><span data-stu-id="d0a85-137">4</span></span>              | <span data-ttu-id="d0a85-138">A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="d0a85-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="d0a85-139">D3DPS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="d0a85-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="d0a85-140">1</span><span class="sxs-lookup"><span data-stu-id="d0a85-140">1</span></span>              | <span data-ttu-id="d0a85-141">A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="d0a85-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="d0a85-142">D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="d0a85-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="d0a85-143">512</span><span class="sxs-lookup"><span data-stu-id="d0a85-143">512</span></span>            | <span data-ttu-id="d0a85-144">O driver dará suporte a, no máximo, várias instruções.</span><span class="sxs-lookup"><span data-stu-id="d0a85-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="d0a85-145">D3DPS20 \_ min \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="d0a85-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="d0a85-146">96</span><span class="sxs-lookup"><span data-stu-id="d0a85-146">96</span></span>             | <span data-ttu-id="d0a85-147">O driver dará suporte a pelo menos este número de instruções.</span><span class="sxs-lookup"><span data-stu-id="d0a85-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="d0a85-148">Essas constantes são usadas pelo membro D3DPSHADERCAPS2 \_ 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="d0a85-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d0a85-149">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="d0a85-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d0a85-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0a85-150">Header</span></span>                   | <span data-ttu-id="d0a85-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d0a85-151">d3d9caps.h</span></span> |
| <span data-ttu-id="d0a85-152">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="d0a85-152">Minimum operating system</span></span> | <span data-ttu-id="d0a85-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d0a85-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0a85-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0a85-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0a85-155">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d0a85-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="d0a85-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="d0a85-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
