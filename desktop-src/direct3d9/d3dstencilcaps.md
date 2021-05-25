---
description: Sinalizadores de recurso de estêncil de driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343051"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="e9599-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="e9599-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="e9599-104">Sinalizadores de recurso de estêncil de driver.</span><span class="sxs-lookup"><span data-stu-id="e9599-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="e9599-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="e9599-105">\#define</span></span>                 | <span data-ttu-id="e9599-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e9599-106">Value</span></span>       | <span data-ttu-id="e9599-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9599-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9599-108">D3DSTENCILCAPS \_ manter</span><span class="sxs-lookup"><span data-stu-id="e9599-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="e9599-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="e9599-109">0x00000001L</span></span> | <span data-ttu-id="e9599-110">Não atualize a entrada no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="e9599-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="e9599-111">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e9599-111">This is the default value.</span></span>                             |
| <span data-ttu-id="e9599-112">D3DSTENCILCAPS \_ zero</span><span class="sxs-lookup"><span data-stu-id="e9599-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="e9599-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e9599-113">0x00000002L</span></span> | <span data-ttu-id="e9599-114">Defina a entrada de buffer de estêncil como 0.</span><span class="sxs-lookup"><span data-stu-id="e9599-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="e9599-115">D3DSTENCILCAPS \_ substituir</span><span class="sxs-lookup"><span data-stu-id="e9599-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="e9599-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="e9599-116">0x00000004L</span></span> | <span data-ttu-id="e9599-117">Substitua a entrada de buffer de estêncil pelo valor de referência.</span><span class="sxs-lookup"><span data-stu-id="e9599-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="e9599-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="e9599-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="e9599-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="e9599-119">0x00000008L</span></span> | <span data-ttu-id="e9599-120">Aumente a entrada do buffer de estêncil, fixação MSS para o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="e9599-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="e9599-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="e9599-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="e9599-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="e9599-122">0x00000010L</span></span> | <span data-ttu-id="e9599-123">Decrementar a entrada de buffer de estêncil, fixação MSS para zero.</span><span class="sxs-lookup"><span data-stu-id="e9599-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="e9599-124">\_Inverter D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="e9599-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="e9599-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="e9599-125">0x00000020L</span></span> | <span data-ttu-id="e9599-126">Inverta os bits na entrada do buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="e9599-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="e9599-127">D3DSTENCILCAPS \_ incr</span><span class="sxs-lookup"><span data-stu-id="e9599-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="e9599-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="e9599-128">0x00000040L</span></span> | <span data-ttu-id="e9599-129">Aumente a entrada do buffer de estêncil, encapsulando para zero se o novo valor exceder o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="e9599-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="e9599-130">D3DSTENCILCAPS \_ DECR</span><span class="sxs-lookup"><span data-stu-id="e9599-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="e9599-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="e9599-131">0x00000080L</span></span> | <span data-ttu-id="e9599-132">Decrementar a entrada de buffer de estêncil, encapsulando o valor máximo se o novo valor for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="e9599-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="e9599-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="e9599-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="e9599-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="e9599-134">0x00000100L</span></span> | <span data-ttu-id="e9599-135">O dispositivo dá suporte a um estêncil de duas pontas.</span><span class="sxs-lookup"><span data-stu-id="e9599-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="e9599-136">Entradas de buffer de estêncil são valores inteiros variando de 0 a 2 ⁿ-1, em que n é a profundidade de bits do buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="e9599-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="e9599-137">Essas constantes são usadas pelo membro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e9599-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="e9599-138">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="e9599-138">Constant Information</span></span>



| <span data-ttu-id="e9599-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9599-139">Requirement</span></span>                         | <span data-ttu-id="e9599-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e9599-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e9599-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9599-141">Header</span></span>                   | <span data-ttu-id="e9599-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="e9599-142">d3d9caps.h</span></span> |
| <span data-ttu-id="e9599-143">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="e9599-143">Minimum operating system</span></span> | <span data-ttu-id="e9599-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e9599-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e9599-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9599-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9599-146">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e9599-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



