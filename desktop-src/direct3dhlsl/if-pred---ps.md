---
title: se Pred-PS
description: Início de um booliano-PS... else-PS... endif – bloco PS, com a condição retirada do conteúdo do registro de predicado.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638860"
---
# <a name="if-pred---ps"></a><span data-ttu-id="0e5c6-103">se Pred-PS</span><span class="sxs-lookup"><span data-stu-id="0e5c6-103">if pred - ps</span></span>

<span data-ttu-id="0e5c6-104">Início de um [booliano-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif – bloco PS](endif---ps.md) , com a condição retirada do conteúdo do registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e5c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e5c6-105">Syntax</span></span>



| <span data-ttu-id="0e5c6-106">Se \[ ! \] pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="0e5c6-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="0e5c6-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="0e5c6-107">Where:</span></span>

-   <span data-ttu-id="0e5c6-108">\[!\] é um modificador NOT opcional.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="0e5c6-109">Isso modifica o valor no registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="0e5c6-110">Pred é o [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="0e5c6-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="0e5c6-111">replicateSwizzle é um componente único que é copiado (ou replicado) para todos os quatro componentes (swizzled).</span><span class="sxs-lookup"><span data-stu-id="0e5c6-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="0e5c6-112">Os componentes válidos são: \[ x, y, z, w \] ou \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="0e5c6-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="0e5c6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e5c6-113">Remarks</span></span>



| <span data-ttu-id="0e5c6-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0e5c6-114">Pixel shader versions</span></span> | <span data-ttu-id="0e5c6-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="0e5c6-115">1\_1</span></span> | <span data-ttu-id="0e5c6-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="0e5c6-116">1\_2</span></span> | <span data-ttu-id="0e5c6-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0e5c6-117">1\_3</span></span> | <span data-ttu-id="0e5c6-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="0e5c6-118">1\_4</span></span> | <span data-ttu-id="0e5c6-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e5c6-119">2\_0</span></span> | <span data-ttu-id="0e5c6-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0e5c6-120">2\_x</span></span> | <span data-ttu-id="0e5c6-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e5c6-121">2\_sw</span></span> | <span data-ttu-id="0e5c6-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e5c6-122">3\_0</span></span> | <span data-ttu-id="0e5c6-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e5c6-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0e5c6-124">Se \_ Pred</span><span class="sxs-lookup"><span data-stu-id="0e5c6-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="0e5c6-125">x</span><span class="sxs-lookup"><span data-stu-id="0e5c6-125">x</span></span>    | <span data-ttu-id="0e5c6-126">x</span><span class="sxs-lookup"><span data-stu-id="0e5c6-126">x</span></span>     | <span data-ttu-id="0e5c6-127">x</span><span class="sxs-lookup"><span data-stu-id="0e5c6-127">x</span></span>    | <span data-ttu-id="0e5c6-128">x</span><span class="sxs-lookup"><span data-stu-id="0e5c6-128">x</span></span>     |



 

<span data-ttu-id="0e5c6-129">Essa instrução é usada para ignorar um bloco de código, com base em um canal do registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="0e5c6-130">Cada \_ bloco If Pred deve terminar com uma instrução [else-PS](else---ps.md) ou [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5c6-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="0e5c6-131">As restrições incluem:</span><span class="sxs-lookup"><span data-stu-id="0e5c6-131">Restrictions include:</span></span>

<span data-ttu-id="0e5c6-132">Se \_ blocos Pred puderem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="0e5c6-133">Isso conta com a profundidade de aninhamento dinâmico total, juntamente com os blocos de [ \_ comp](if-comp---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5c6-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="0e5c6-134">Um \_ bloco If Pred não pode ampliar um bloco de loops; ele deve estar completamente dentro dele ou colocá-lo.</span><span class="sxs-lookup"><span data-stu-id="0e5c6-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e5c6-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e5c6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e5c6-136">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0e5c6-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




