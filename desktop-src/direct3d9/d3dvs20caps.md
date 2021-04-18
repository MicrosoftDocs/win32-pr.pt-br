---
description: Constantes do sombreador de vértices. Essas constantes são usadas pelo membro VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762161"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="11ece-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="11ece-104">D3DVS20CAPS</span></span>

<span data-ttu-id="11ece-105">Constantes do sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="11ece-105">Vertex shader caps constants.</span></span> <span data-ttu-id="11ece-106">Essas constantes são usadas pelo membro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="11ece-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="11ece-107">\#definir</span><span class="sxs-lookup"><span data-stu-id="11ece-107">\#define</span></span>                              | <span data-ttu-id="11ece-108">Valor</span><span class="sxs-lookup"><span data-stu-id="11ece-108">Value</span></span>          | <span data-ttu-id="11ece-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="11ece-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ece-110">D3DVS20CAPS \_ predicação</span><span class="sxs-lookup"><span data-stu-id="11ece-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="11ece-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="11ece-111">(1 << 0)</span></span> | <span data-ttu-id="11ece-112">Há suporte para predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="11ece-112">Instruction predication is supported.</span></span> <span data-ttu-id="11ece-113">Consulte [setp \_ comp-vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="11ece-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="11ece-114">D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="11ece-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="11ece-115">24</span><span class="sxs-lookup"><span data-stu-id="11ece-115">24</span></span>             | <span data-ttu-id="11ece-116">O nível máximo de aninhamento de instruções de controle de fluxo dinâmico ([Break-vs](../direct3dhlsl/break---vs.md), [Break \_ comp](../direct3dhlsl/break-comp---vs.md)-vs, [breakp-vs](../direct3dhlsl/breakp---vs.md), [se \_ comp-vs](../direct3dhlsl/if-comp---vs.md), se \_ comp-vs, [se Pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="11ece-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="11ece-117">D3DVS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="11ece-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="11ece-118">0</span><span class="sxs-lookup"><span data-stu-id="11ece-118">0</span></span>              | <span data-ttu-id="11ece-119">O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico ([Break-vs](../direct3dhlsl/break---vs.md), [Break \_ comp](../direct3dhlsl/break-comp---vs.md)-vs, [breakp-vs](../direct3dhlsl/breakp---vs.md), [se \_ comp-](../direct3dhlsl/if-comp---vs.md)vs, se \_ comp-vs, [se Pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="11ece-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="11ece-120">D3DVS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="11ece-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="11ece-121">32</span><span class="sxs-lookup"><span data-stu-id="11ece-121">32</span></span>             | <span data-ttu-id="11ece-122">O número máximo de registros temporários com suporte.</span><span class="sxs-lookup"><span data-stu-id="11ece-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="11ece-123">D3DVS20 \_ min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="11ece-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="11ece-124">12</span><span class="sxs-lookup"><span data-stu-id="11ece-124">12</span></span>             | <span data-ttu-id="11ece-125">O número mínimo de registros temporários com suporte.</span><span class="sxs-lookup"><span data-stu-id="11ece-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="11ece-126">D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="11ece-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="11ece-127">4</span><span class="sxs-lookup"><span data-stu-id="11ece-127">4</span></span>              | <span data-ttu-id="11ece-128">A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="11ece-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="11ece-129">D3DVS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="11ece-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="11ece-130">1</span><span class="sxs-lookup"><span data-stu-id="11ece-130">1</span></span>              | <span data-ttu-id="11ece-131">A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.</span><span class="sxs-lookup"><span data-stu-id="11ece-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="11ece-132">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="11ece-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="11ece-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11ece-133">Header</span></span>                   | <span data-ttu-id="11ece-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="11ece-134">d3d9caps.h</span></span> |
| <span data-ttu-id="11ece-135">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="11ece-135">Minimum operating system</span></span> | <span data-ttu-id="11ece-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="11ece-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="11ece-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11ece-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ece-138">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="11ece-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="11ece-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="11ece-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
