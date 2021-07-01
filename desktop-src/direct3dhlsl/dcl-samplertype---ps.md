---
title: dcl_samplerType (sm2, sm3 – ps asm)
description: Declare um exemplo de sombreador de pixel.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129663"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="80c47-103">dcl \_ samplerType (sm2, sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="80c47-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="80c47-104">Declare um exemplo de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="80c47-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c47-105">Syntax</span></span>

<span data-ttu-id="80c47-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="80c47-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="80c47-107">em que:</span><span class="sxs-lookup"><span data-stu-id="80c47-107">where:</span></span>

-   <span data-ttu-id="80c47-108">\_samplerType define o tipo de dados sampler.</span><span class="sxs-lookup"><span data-stu-id="80c47-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="80c47-109">Isso determina quantas coordenadas são necessárias para cada coordenada de textura durante a amostragem.</span><span class="sxs-lookup"><span data-stu-id="80c47-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="80c47-110">As dimensões de coordenada de textura a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="80c47-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="80c47-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="80c47-111">\_2d</span></span>
    -   <span data-ttu-id="80c47-112">\_Cubo</span><span class="sxs-lookup"><span data-stu-id="80c47-112">\_cube</span></span>
    -   <span data-ttu-id="80c47-113">\_Volume</span><span class="sxs-lookup"><span data-stu-id="80c47-113">\_volume</span></span>
-   <span data-ttu-id="80c47-114">s identifica um exemplo em que s é uma abreviação para o \# exemplo e é o número do \# exemplo.</span><span class="sxs-lookup"><span data-stu-id="80c47-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="80c47-115">Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.</span><span class="sxs-lookup"><span data-stu-id="80c47-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="80c47-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c47-116">Remarks</span></span>



| <span data-ttu-id="80c47-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="80c47-117">Pixel shader versions</span></span> | <span data-ttu-id="80c47-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="80c47-118">1\_1</span></span> | <span data-ttu-id="80c47-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="80c47-119">1\_2</span></span> | <span data-ttu-id="80c47-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="80c47-120">1\_3</span></span> | <span data-ttu-id="80c47-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="80c47-121">1\_4</span></span> | <span data-ttu-id="80c47-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80c47-122">2\_0</span></span> | <span data-ttu-id="80c47-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="80c47-123">2\_x</span></span> | <span data-ttu-id="80c47-124">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="80c47-124">2\_sw</span></span> | <span data-ttu-id="80c47-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80c47-125">3\_0</span></span> | <span data-ttu-id="80c47-126">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="80c47-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="80c47-127">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="80c47-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="80c47-128">x</span><span class="sxs-lookup"><span data-stu-id="80c47-128">x</span></span>    | <span data-ttu-id="80c47-129">x</span><span class="sxs-lookup"><span data-stu-id="80c47-129">x</span></span>    | <span data-ttu-id="80c47-130">x</span><span class="sxs-lookup"><span data-stu-id="80c47-130">x</span></span>     | <span data-ttu-id="80c47-131">x</span><span class="sxs-lookup"><span data-stu-id="80c47-131">x</span></span>    | <span data-ttu-id="80c47-132">x</span><span class="sxs-lookup"><span data-stu-id="80c47-132">x</span></span>     |



 

<span data-ttu-id="80c47-133">Todas as instruções dcl \_ samplerType devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="80c47-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="80c47-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="80c47-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="80c47-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80c47-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c47-136">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="80c47-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




