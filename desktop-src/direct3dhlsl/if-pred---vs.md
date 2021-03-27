---
title: se Pred-vs
description: Início de um If Pred-vs... else-vs... endif – bloco vs, com a condição retirada do conteúdo do registro de predicado.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293558"
---
# <a name="if-pred---vs"></a><span data-ttu-id="da06f-103">se Pred-vs</span><span class="sxs-lookup"><span data-stu-id="da06f-103">if pred - vs</span></span>

<span data-ttu-id="da06f-104">Início de um If Pred-vs... [else-vs](else---vs.md)... [endif – bloco vs](endif---vs.md) , com a condição retirada do conteúdo do registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="da06f-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="da06f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da06f-105">Syntax</span></span>



| <span data-ttu-id="da06f-106">Se \[ ! \] pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="da06f-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="da06f-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="da06f-107">Where:</span></span>

-   <span data-ttu-id="da06f-108">\[!\] um modificador NOT opcional.</span><span class="sxs-lookup"><span data-stu-id="da06f-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="da06f-109">Isso modifica o valor no registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="da06f-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="da06f-110">Pred é o predicado Register, P0.</span><span class="sxs-lookup"><span data-stu-id="da06f-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="da06f-111">Consulte [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="da06f-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="da06f-112">replicateSwizzle é um componente único que é copiado (ou replicado) para todos os quatro componentes (swizzled).</span><span class="sxs-lookup"><span data-stu-id="da06f-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="da06f-113">Os componentes válidos são: x, y, z, w ou r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="da06f-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="da06f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="da06f-114">Remarks</span></span>



| <span data-ttu-id="da06f-115">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="da06f-115">Vertex shader versions</span></span> | <span data-ttu-id="da06f-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="da06f-116">1\_1</span></span> | <span data-ttu-id="da06f-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da06f-117">2\_0</span></span> | <span data-ttu-id="da06f-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="da06f-118">2\_x</span></span> | <span data-ttu-id="da06f-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="da06f-119">2\_sw</span></span> | <span data-ttu-id="da06f-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da06f-120">3\_0</span></span> | <span data-ttu-id="da06f-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="da06f-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="da06f-122">se Pred</span><span class="sxs-lookup"><span data-stu-id="da06f-122">if pred</span></span>                |      |      | <span data-ttu-id="da06f-123">x</span><span class="sxs-lookup"><span data-stu-id="da06f-123">x</span></span>    | <span data-ttu-id="da06f-124">x</span><span class="sxs-lookup"><span data-stu-id="da06f-124">x</span></span>     | <span data-ttu-id="da06f-125">x</span><span class="sxs-lookup"><span data-stu-id="da06f-125">x</span></span>    | <span data-ttu-id="da06f-126">x</span><span class="sxs-lookup"><span data-stu-id="da06f-126">x</span></span>     |



 

<span data-ttu-id="da06f-127">Essa instrução é usada para ignorar um bloco de código, com base em um canal do registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="da06f-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="da06f-128">Cada \_ bloco If Pred deve terminar com uma instrução else ou endif.</span><span class="sxs-lookup"><span data-stu-id="da06f-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="da06f-129">As restrições incluem:</span><span class="sxs-lookup"><span data-stu-id="da06f-129">Restrictions include:</span></span>

<span data-ttu-id="da06f-130">Se \_ blocos Pred puderem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="da06f-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="da06f-131">Isso conta com a profundidade de aninhamento dinâmico total, juntamente com os blocos de [ \_ comp](if-comp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="da06f-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="da06f-132">Um \_ bloco If Pred não pode ampliar um bloco de loop, ele deve estar completamente dentro dele ou colocá-lo.</span><span class="sxs-lookup"><span data-stu-id="da06f-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da06f-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da06f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da06f-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="da06f-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




