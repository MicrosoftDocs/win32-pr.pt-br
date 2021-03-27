---
title: se bool-PS
description: Início de um bloco If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638853"
---
# <a name="if-bool---ps"></a><span data-ttu-id="b0d29-103">se bool-PS</span><span class="sxs-lookup"><span data-stu-id="b0d29-103">if bool - ps</span></span>

<span data-ttu-id="b0d29-104">Início de um bloco If.</span><span class="sxs-lookup"><span data-stu-id="b0d29-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d29-105">Syntax</span></span>



| <span data-ttu-id="b0d29-106">se bool</span><span class="sxs-lookup"><span data-stu-id="b0d29-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="b0d29-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="b0d29-107">Where:</span></span>

-   <span data-ttu-id="b0d29-108">bool é um número de registro bool (booliano).</span><span class="sxs-lookup"><span data-stu-id="b0d29-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="b0d29-109">Consulte [constante de registro booliano](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="b0d29-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d29-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0d29-110">Remarks</span></span>



| <span data-ttu-id="b0d29-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0d29-111">Pixel shader versions</span></span> | <span data-ttu-id="b0d29-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="b0d29-112">1\_1</span></span> | <span data-ttu-id="b0d29-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="b0d29-113">1\_2</span></span> | <span data-ttu-id="b0d29-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0d29-114">1\_3</span></span> | <span data-ttu-id="b0d29-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0d29-115">1\_4</span></span> | <span data-ttu-id="b0d29-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0d29-116">2\_0</span></span> | <span data-ttu-id="b0d29-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b0d29-117">2\_x</span></span> | <span data-ttu-id="b0d29-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0d29-118">2\_sw</span></span> | <span data-ttu-id="b0d29-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0d29-119">3\_0</span></span> | <span data-ttu-id="b0d29-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0d29-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b0d29-121">se bool</span><span class="sxs-lookup"><span data-stu-id="b0d29-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="b0d29-122">x</span><span class="sxs-lookup"><span data-stu-id="b0d29-122">x</span></span>    | <span data-ttu-id="b0d29-123">x</span><span class="sxs-lookup"><span data-stu-id="b0d29-123">x</span></span>     | <span data-ttu-id="b0d29-124">x</span><span class="sxs-lookup"><span data-stu-id="b0d29-124">x</span></span>    | <span data-ttu-id="b0d29-125">x</span><span class="sxs-lookup"><span data-stu-id="b0d29-125">x</span></span>     |



 

<span data-ttu-id="b0d29-126">Se o registro booliano de origem na instrução If for true, o código incluído na instrução If e o [endif-PS](endif---ps.md) ou [else-PS](else---ps.md) correspondente serão executados.</span><span class="sxs-lookup"><span data-stu-id="b0d29-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="b0d29-127">Caso contrário, o código incluído pelo else-PS... endif-instruções PS são executadas.</span><span class="sxs-lookup"><span data-stu-id="b0d29-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="b0d29-128">Essa instrução consome um slot de instrução.</span><span class="sxs-lookup"><span data-stu-id="b0d29-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="b0d29-129">Um bloco If pode ser aninhado.</span><span class="sxs-lookup"><span data-stu-id="b0d29-129">An if block can be nested.</span></span>

<span data-ttu-id="b0d29-130">Um bloco If não pode ampliar um bloco de loop.</span><span class="sxs-lookup"><span data-stu-id="b0d29-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="b0d29-131">Um bloco If pode ser seguido por um bloco de instruções e/ou uma instrução [else-PS](else---ps.md) e/ou uma instrução [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="b0d29-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="b0d29-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0d29-132">Example</span></span>

<span data-ttu-id="b0d29-133">Essa instrução fornece controle de fluxo estático condicional.</span><span class="sxs-lookup"><span data-stu-id="b0d29-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="b0d29-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0d29-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0d29-135">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0d29-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="b0d29-136">else-PS</span><span class="sxs-lookup"><span data-stu-id="b0d29-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="b0d29-137">endif-PS</span><span class="sxs-lookup"><span data-stu-id="b0d29-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




