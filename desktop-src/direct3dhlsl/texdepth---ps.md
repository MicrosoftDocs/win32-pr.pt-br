---
title: texdepth-PS
description: Calcule os valores de profundidade a serem usados no teste de comparação de buffer de profundidade para este pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823438"
---
# <a name="texdepth---ps"></a><span data-ttu-id="d7466-103">texdepth-PS</span><span class="sxs-lookup"><span data-stu-id="d7466-103">texdepth - ps</span></span>

<span data-ttu-id="d7466-104">Calcule os valores de profundidade a serem usados no teste de comparação de buffer de profundidade para este pixel.</span><span class="sxs-lookup"><span data-stu-id="d7466-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7466-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7466-105">Syntax</span></span>



| <span data-ttu-id="d7466-106">texdepth DST</span><span class="sxs-lookup"><span data-stu-id="d7466-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="d7466-107">onde</span><span class="sxs-lookup"><span data-stu-id="d7466-107">where</span></span>

-   <span data-ttu-id="d7466-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d7466-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7466-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7466-109">Remarks</span></span>



| <span data-ttu-id="d7466-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d7466-110">Pixel shader versions</span></span> | <span data-ttu-id="d7466-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="d7466-111">1\_1</span></span> | <span data-ttu-id="d7466-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="d7466-112">1\_2</span></span> | <span data-ttu-id="d7466-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d7466-113">1\_3</span></span> | <span data-ttu-id="d7466-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="d7466-114">1\_4</span></span> | <span data-ttu-id="d7466-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7466-115">2\_0</span></span> | <span data-ttu-id="d7466-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d7466-116">2\_x</span></span> | <span data-ttu-id="d7466-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7466-117">2\_sw</span></span> | <span data-ttu-id="d7466-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7466-118">3\_0</span></span> | <span data-ttu-id="d7466-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7466-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d7466-120">texdepth</span><span class="sxs-lookup"><span data-stu-id="d7466-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="d7466-121">x</span><span class="sxs-lookup"><span data-stu-id="d7466-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="d7466-122">Essa instrução usa R5. r/R5. g no teste de comparação de buffer de profundidade para este pixel.</span><span class="sxs-lookup"><span data-stu-id="d7466-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="d7466-123">Os dados nos canais azul e alfa são ignorados.</span><span class="sxs-lookup"><span data-stu-id="d7466-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="d7466-124">Se r5. g = 0, o resultado de R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7466-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="d7466-125">O registro temporário R5 é o único registro que essa instrução pode usar.</span><span class="sxs-lookup"><span data-stu-id="d7466-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="d7466-126">Depois de executar essa instrução, o registro temporário R5 não estará disponível para uso adicional no sombreador.</span><span class="sxs-lookup"><span data-stu-id="d7466-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="d7466-127">Quando a multiamostragem, o uso dessa instrução elimina a maior parte do benefício do buffer de profundidade de resolução mais alto.</span><span class="sxs-lookup"><span data-stu-id="d7466-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="d7466-128">Como o sombreador de pixel é executado uma vez por pixel, a saída de valor de profundidade única por [texm3x2depth-PS](texm3x2depth---ps.md) ou texdepth será usada para cada um dos testes de comparação de profundidade de subpixel.</span><span class="sxs-lookup"><span data-stu-id="d7466-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="d7466-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7466-129">Examples</span></span>

<span data-ttu-id="d7466-130">Aqui está um exemplo usando texdepth.</span><span class="sxs-lookup"><span data-stu-id="d7466-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="d7466-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7466-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7466-132">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d7466-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




