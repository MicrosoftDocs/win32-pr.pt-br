---
title: se bool-vs
description: Inicia um if... senão... endif – bloco vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006862"
---
# <a name="if-bool---vs"></a><span data-ttu-id="1fa65-103">se bool-vs</span><span class="sxs-lookup"><span data-stu-id="1fa65-103">if bool - vs</span></span>

<span data-ttu-id="1fa65-104">Inicia um if... [senão](else---vs.md)... [endif – bloco vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa65-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fa65-105">Syntax</span></span>



| <span data-ttu-id="1fa65-106">se bool</span><span class="sxs-lookup"><span data-stu-id="1fa65-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="1fa65-107">em que bool é um número de registro bool.</span><span class="sxs-lookup"><span data-stu-id="1fa65-107">where bool is a bool register number.</span></span> <span data-ttu-id="1fa65-108">Consulte [constante de registro booliano](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="1fa65-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa65-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fa65-109">Remarks</span></span>



| <span data-ttu-id="1fa65-110">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1fa65-110">Vertex shader versions</span></span> | <span data-ttu-id="1fa65-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="1fa65-111">1\_1</span></span> | <span data-ttu-id="1fa65-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1fa65-112">2\_0</span></span> | <span data-ttu-id="1fa65-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1fa65-113">2\_x</span></span> | <span data-ttu-id="1fa65-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1fa65-114">2\_sw</span></span> | <span data-ttu-id="1fa65-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1fa65-115">3\_0</span></span> | <span data-ttu-id="1fa65-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1fa65-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="1fa65-117">se bool</span><span class="sxs-lookup"><span data-stu-id="1fa65-117">if bool</span></span>                |      | <span data-ttu-id="1fa65-118">x</span><span class="sxs-lookup"><span data-stu-id="1fa65-118">x</span></span>    | <span data-ttu-id="1fa65-119">x</span><span class="sxs-lookup"><span data-stu-id="1fa65-119">x</span></span>    | <span data-ttu-id="1fa65-120">x</span><span class="sxs-lookup"><span data-stu-id="1fa65-120">x</span></span>     | <span data-ttu-id="1fa65-121">x</span><span class="sxs-lookup"><span data-stu-id="1fa65-121">x</span></span>    | <span data-ttu-id="1fa65-122">x</span><span class="sxs-lookup"><span data-stu-id="1fa65-122">x</span></span>     |



 

<span data-ttu-id="1fa65-123">Se o registro booliano de origem na instrução If for true, o código incluído na instrução If e a outra correspondência serão executados.</span><span class="sxs-lookup"><span data-stu-id="1fa65-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="1fa65-124">Caso contrário, o código incluído no [else](else---vs.md)... [endif-](endif---vs.md) as instruções vs são executadas.</span><span class="sxs-lookup"><span data-stu-id="1fa65-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="1fa65-125">Essa instrução consome um slot de instrução.</span><span class="sxs-lookup"><span data-stu-id="1fa65-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="1fa65-126">se blocos podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="1fa65-126">if blocks can be nested.</span></span>

<span data-ttu-id="1fa65-127">Um bloco If não pode ampliar um bloco de loop.</span><span class="sxs-lookup"><span data-stu-id="1fa65-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="1fa65-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1fa65-128">Example</span></span>

<span data-ttu-id="1fa65-129">Essa instrução fornece controle de fluxo estático condicional.</span><span class="sxs-lookup"><span data-stu-id="1fa65-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="1fa65-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fa65-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa65-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1fa65-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="1fa65-132">else-vs</span><span class="sxs-lookup"><span data-stu-id="1fa65-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="1fa65-133">endif-vs</span><span class="sxs-lookup"><span data-stu-id="1fa65-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




