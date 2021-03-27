---
title: texm3x2depth-PS
description: Calcule o valor de profundidade a ser usado em testes de profundidade para este pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967109"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="3b021-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="3b021-103">texm3x2depth - ps</span></span>

<span data-ttu-id="3b021-104">Calcule o valor de profundidade a ser usado em testes de profundidade para este pixel.</span><span class="sxs-lookup"><span data-stu-id="3b021-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b021-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b021-105">Syntax</span></span>



| <span data-ttu-id="3b021-106">texm3x2depth DST, src</span><span class="sxs-lookup"><span data-stu-id="3b021-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="3b021-107">onde</span><span class="sxs-lookup"><span data-stu-id="3b021-107">where</span></span>

-   <span data-ttu-id="3b021-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3b021-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3b021-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3b021-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b021-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b021-110">Remarks</span></span>



| <span data-ttu-id="3b021-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3b021-111">Pixel shader versions</span></span> | <span data-ttu-id="3b021-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3b021-112">1\_1</span></span> | <span data-ttu-id="3b021-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="3b021-113">1\_2</span></span> | <span data-ttu-id="3b021-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3b021-114">1\_3</span></span> | <span data-ttu-id="3b021-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="3b021-115">1\_4</span></span> | <span data-ttu-id="3b021-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b021-116">2\_0</span></span> | <span data-ttu-id="3b021-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3b021-117">2\_x</span></span> | <span data-ttu-id="3b021-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3b021-118">2\_sw</span></span> | <span data-ttu-id="3b021-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b021-119">3\_0</span></span> | <span data-ttu-id="3b021-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3b021-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3b021-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="3b021-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="3b021-122">x</span><span class="sxs-lookup"><span data-stu-id="3b021-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3b021-123">Essa instrução deve ser usada com a instrução [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3b021-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="3b021-124">Ao usar essas duas instruções, os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b021-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="3b021-125">O cálculo de profundidade é feito após o uso de uma operação de produto de ponto para localizar z e w.</span><span class="sxs-lookup"><span data-stu-id="3b021-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="3b021-126">Veja mais detalhes sobre como o cálculo de profundidade é realizado.</span><span class="sxs-lookup"><span data-stu-id="3b021-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="3b021-127">A instrução texm3x2pad calcula z.</span><span class="sxs-lookup"><span data-stu-id="3b021-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="3b021-128">z = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3b021-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="3b021-129">A instrução texm3x2depth calcula w.</span><span class="sxs-lookup"><span data-stu-id="3b021-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="3b021-130">w = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3b021-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="3b021-131">Calcule a profundidade e armazene o resultado em t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="3b021-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="3b021-132">A profundidade calculada é marcada para ser usada no teste de profundidade do pixel, substituindo o valor de teste de profundidade existente para o pixel.</span><span class="sxs-lookup"><span data-stu-id="3b021-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="3b021-133">Certifique-se de que fixe z/w esteja no intervalo de (0-1).</span><span class="sxs-lookup"><span data-stu-id="3b021-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="3b021-134">Se z/w estiver fora desse intervalo, o resultado armazenado no buffer de profundidade será indefinido.</span><span class="sxs-lookup"><span data-stu-id="3b021-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="3b021-135">Depois de executar o texm3x2depth, o registro t (m + 1) não estará mais disponível para uso no sombreador.</span><span class="sxs-lookup"><span data-stu-id="3b021-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="3b021-136">Quando a multiamostragem, o uso dessa instrução elimina a maior parte do benefício do buffer de profundidade de resolução mais alto.</span><span class="sxs-lookup"><span data-stu-id="3b021-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="3b021-137">Como o sombreador de pixel é executado uma vez por pixel, a saída de valor de profundidade única por texm3x2depth ou [texdepth-PS](texdepth---ps.md) será usada para cada um dos testes de comparação de profundidade de subpixel.</span><span class="sxs-lookup"><span data-stu-id="3b021-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b021-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b021-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b021-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3b021-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




