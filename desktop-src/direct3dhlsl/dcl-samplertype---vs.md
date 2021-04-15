---
title: dcl_samplerType (SM3-vs ASM)
description: Declare uma amostra de sombreador de vértice.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988614"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="e135c-103">\_SampleType de DCL (SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="e135c-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="e135c-104">Declare uma amostra de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="e135c-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="e135c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e135c-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="e135c-106">\_amostrador DCL s\#</span><span class="sxs-lookup"><span data-stu-id="e135c-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="e135c-107">em que:</span><span class="sxs-lookup"><span data-stu-id="e135c-107">where:</span></span>

-   <span data-ttu-id="e135c-108">\_SampleType define o tipo de dados de amostra.</span><span class="sxs-lookup"><span data-stu-id="e135c-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="e135c-109">Isso determina quantas coordenadas são exigidas por cada coordenada de textura durante a amostragem.</span><span class="sxs-lookup"><span data-stu-id="e135c-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="e135c-110">As dimensões de coordenadas de textura a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="e135c-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="e135c-111">\_Dimensiona</span><span class="sxs-lookup"><span data-stu-id="e135c-111">\_2d</span></span>
    -   <span data-ttu-id="e135c-112">\_simples</span><span class="sxs-lookup"><span data-stu-id="e135c-112">\_cube</span></span>
    -   <span data-ttu-id="e135c-113">\_volume</span><span class="sxs-lookup"><span data-stu-id="e135c-113">\_volume</span></span>
-   <span data-ttu-id="e135c-114">s \# identifica um amostra em que s é uma abreviação para a amostra e \# é o número de amostra.</span><span class="sxs-lookup"><span data-stu-id="e135c-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="e135c-115">As [amostras (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s são superregistradas porque você não pode ler ou gravar diretamente nelas.</span><span class="sxs-lookup"><span data-stu-id="e135c-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="e135c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e135c-116">Remarks</span></span>



| <span data-ttu-id="e135c-117">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e135c-117">Vertex shader versions</span></span> | <span data-ttu-id="e135c-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="e135c-118">1\_1</span></span> | <span data-ttu-id="e135c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e135c-119">2\_0</span></span> | <span data-ttu-id="e135c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e135c-120">2\_x</span></span> | <span data-ttu-id="e135c-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e135c-121">2\_sw</span></span> | <span data-ttu-id="e135c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e135c-122">3\_0</span></span> | <span data-ttu-id="e135c-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e135c-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e135c-124">\_classificador de DCL</span><span class="sxs-lookup"><span data-stu-id="e135c-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="e135c-125">x</span><span class="sxs-lookup"><span data-stu-id="e135c-125">x</span></span>    | <span data-ttu-id="e135c-126">x</span><span class="sxs-lookup"><span data-stu-id="e135c-126">x</span></span>     |



 

<span data-ttu-id="e135c-127">Todas as \_ instruções de SampleType de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="e135c-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e135c-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e135c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e135c-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e135c-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




