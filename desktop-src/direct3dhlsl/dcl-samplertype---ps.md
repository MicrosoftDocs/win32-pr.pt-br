---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Declare uma amostra de sombreador de pixel.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006925"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="bd999-103">\_SampleType de DCL (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="bd999-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="bd999-104">Declare uma amostra de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bd999-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd999-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd999-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="bd999-106">\_amostrador DCL s\#</span><span class="sxs-lookup"><span data-stu-id="bd999-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="bd999-107">em que:</span><span class="sxs-lookup"><span data-stu-id="bd999-107">where:</span></span>

-   <span data-ttu-id="bd999-108">\_SampleType define o tipo de dados de amostra.</span><span class="sxs-lookup"><span data-stu-id="bd999-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="bd999-109">Isso determina quantas coordenadas são exigidas por cada coordenada de textura durante a amostragem.</span><span class="sxs-lookup"><span data-stu-id="bd999-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="bd999-110">As dimensões de coordenadas de textura a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="bd999-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="bd999-111">\_Dimensiona</span><span class="sxs-lookup"><span data-stu-id="bd999-111">\_2d</span></span>
    -   <span data-ttu-id="bd999-112">\_simples</span><span class="sxs-lookup"><span data-stu-id="bd999-112">\_cube</span></span>
    -   <span data-ttu-id="bd999-113">\_volume</span><span class="sxs-lookup"><span data-stu-id="bd999-113">\_volume</span></span>
-   <span data-ttu-id="bd999-114">s \# identifica um amostra em que s é uma abreviação para a amostra e \# é o número de amostra.</span><span class="sxs-lookup"><span data-stu-id="bd999-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="bd999-115">Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.</span><span class="sxs-lookup"><span data-stu-id="bd999-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd999-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd999-116">Remarks</span></span>



| <span data-ttu-id="bd999-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bd999-117">Pixel shader versions</span></span> | <span data-ttu-id="bd999-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="bd999-118">1\_1</span></span> | <span data-ttu-id="bd999-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="bd999-119">1\_2</span></span> | <span data-ttu-id="bd999-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd999-120">1\_3</span></span> | <span data-ttu-id="bd999-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="bd999-121">1\_4</span></span> | <span data-ttu-id="bd999-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bd999-122">2\_0</span></span> | <span data-ttu-id="bd999-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bd999-123">2\_x</span></span> | <span data-ttu-id="bd999-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bd999-124">2\_sw</span></span> | <span data-ttu-id="bd999-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bd999-125">3\_0</span></span> | <span data-ttu-id="bd999-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bd999-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bd999-127">\_classificador de DCL</span><span class="sxs-lookup"><span data-stu-id="bd999-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="bd999-128">x</span><span class="sxs-lookup"><span data-stu-id="bd999-128">x</span></span>    | <span data-ttu-id="bd999-129">x</span><span class="sxs-lookup"><span data-stu-id="bd999-129">x</span></span>    | <span data-ttu-id="bd999-130">x</span><span class="sxs-lookup"><span data-stu-id="bd999-130">x</span></span>     | <span data-ttu-id="bd999-131">x</span><span class="sxs-lookup"><span data-stu-id="bd999-131">x</span></span>    | <span data-ttu-id="bd999-132">x</span><span class="sxs-lookup"><span data-stu-id="bd999-132">x</span></span>     |



 

<span data-ttu-id="bd999-133">Todas as \_ instruções de SampleType de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="bd999-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="bd999-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bd999-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="bd999-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd999-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd999-136">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bd999-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




