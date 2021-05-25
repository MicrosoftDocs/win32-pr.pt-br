---
description: As constantes de limite do sombreador de vértice. Essas constantes são usadas pelo membro VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342941"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="67994-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="67994-104">D3DVS20CAPS</span></span>

<span data-ttu-id="67994-105">As constantes de limite do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="67994-105">Vertex shader caps constants.</span></span> <span data-ttu-id="67994-106">Essas constantes são usadas pelo membro VS20Caps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="67994-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="67994-107">\#Definir</span><span class="sxs-lookup"><span data-stu-id="67994-107">\#define</span></span>                              | <span data-ttu-id="67994-108">Valor</span><span class="sxs-lookup"><span data-stu-id="67994-108">Value</span></span>          | <span data-ttu-id="67994-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="67994-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67994-110">PREDICAÇÃO DE D3DVS20CAPS \_</span><span class="sxs-lookup"><span data-stu-id="67994-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="67994-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="67994-111">(1 << 0)</span></span> | <span data-ttu-id="67994-112">Há suporte para a predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="67994-112">Instruction predication is supported.</span></span> <span data-ttu-id="67994-113">Consulte [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="67994-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="67994-114">D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="67994-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="67994-115">24</span><span class="sxs-lookup"><span data-stu-id="67994-115">24</span></span>             | <span data-ttu-id="67994-116">O nível máximo de aninhamento de instruções de controle de fluxo dinâmico ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="67994-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="67994-117">D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="67994-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="67994-118">0</span><span class="sxs-lookup"><span data-stu-id="67994-118">0</span></span>              | <span data-ttu-id="67994-119">O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="67994-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="67994-120">D3DVS20 \_ \_ NUMTEMPS MÁXIMO</span><span class="sxs-lookup"><span data-stu-id="67994-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="67994-121">32</span><span class="sxs-lookup"><span data-stu-id="67994-121">32</span></span>             | <span data-ttu-id="67994-122">O número máximo de registros temporários com suporte.</span><span class="sxs-lookup"><span data-stu-id="67994-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="67994-123">D3DVS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="67994-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="67994-124">12</span><span class="sxs-lookup"><span data-stu-id="67994-124">12</span></span>             | <span data-ttu-id="67994-125">O número mínimo de registros temporários com suporte.</span><span class="sxs-lookup"><span data-stu-id="67994-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="67994-126">D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="67994-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="67994-127">4</span><span class="sxs-lookup"><span data-stu-id="67994-127">4</span></span>              | <span data-ttu-id="67994-128">A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="67994-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="67994-129">D3DVS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="67994-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="67994-130">1</span><span class="sxs-lookup"><span data-stu-id="67994-130">1</span></span>              | <span data-ttu-id="67994-131">A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="67994-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="67994-132">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="67994-132">Constant Information</span></span>



| <span data-ttu-id="67994-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="67994-133">Requirement</span></span>                         | <span data-ttu-id="67994-134">Valor</span><span class="sxs-lookup"><span data-stu-id="67994-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="67994-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67994-135">Header</span></span>                   | <span data-ttu-id="67994-136">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="67994-136">d3d9caps.h</span></span> |
| <span data-ttu-id="67994-137">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="67994-137">Minimum operating system</span></span> | <span data-ttu-id="67994-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="67994-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="67994-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67994-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67994-140">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="67994-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="67994-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="67994-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
