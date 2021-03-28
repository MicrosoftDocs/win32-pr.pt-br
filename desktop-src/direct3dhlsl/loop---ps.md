---
title: loop-PS
description: Inicia um loop... bloco ENDLOOP-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006896"
---
# <a name="loop---ps"></a><span data-ttu-id="37327-103">loop-PS</span><span class="sxs-lookup"><span data-stu-id="37327-103">loop - ps</span></span>

<span data-ttu-id="37327-104">Inicia um loop... bloco [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="37327-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="37327-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37327-105">Syntax</span></span>



| <span data-ttu-id="37327-106">loop aL, i\#</span><span class="sxs-lookup"><span data-stu-id="37327-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="37327-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="37327-107">Where:</span></span>

-   <span data-ttu-id="37327-108">aL é o [registro de contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) que mantém a contagem de loops atual.</span><span class="sxs-lookup"><span data-stu-id="37327-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="37327-109">i \# é um [registro inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="37327-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="37327-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="37327-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="37327-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="37327-111">Remarks</span></span>



| <span data-ttu-id="37327-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="37327-112">Pixel shader versions</span></span> | <span data-ttu-id="37327-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="37327-113">1\_1</span></span> | <span data-ttu-id="37327-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="37327-114">1\_2</span></span> | <span data-ttu-id="37327-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="37327-115">1\_3</span></span> | <span data-ttu-id="37327-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="37327-116">1\_4</span></span> | <span data-ttu-id="37327-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37327-117">2\_0</span></span> | <span data-ttu-id="37327-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37327-118">2\_x</span></span> | <span data-ttu-id="37327-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37327-119">2\_sw</span></span> | <span data-ttu-id="37327-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37327-120">3\_0</span></span> | <span data-ttu-id="37327-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37327-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="37327-122">loop</span><span class="sxs-lookup"><span data-stu-id="37327-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="37327-123">x</span><span class="sxs-lookup"><span data-stu-id="37327-123">x</span></span>    | <span data-ttu-id="37327-124">x</span><span class="sxs-lookup"><span data-stu-id="37327-124">x</span></span>     |



 

-   <span data-ttu-id="37327-125">O [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) mantém a contagem de loops atual e pode ser usado para endereçamento relativo no [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dentro do bloco de loop.</span><span class="sxs-lookup"><span data-stu-id="37327-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="37327-126">i \# . x especifica a contagem de iteração.</span><span class="sxs-lookup"><span data-stu-id="37327-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="37327-127">O intervalo legal é \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="37327-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="37327-128">Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="37327-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="37327-129">i \# . y especifica o valor inicial do registro do [contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al).</span><span class="sxs-lookup"><span data-stu-id="37327-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="37327-130">O intervalo legal é \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="37327-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="37327-131">Observe que essa instrução não incrementa nem Decrementa o valor de i \# . y.</span><span class="sxs-lookup"><span data-stu-id="37327-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="37327-132">i \# . z especifica o tamanho Step/Stride.</span><span class="sxs-lookup"><span data-stu-id="37327-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="37327-133">O intervalo legal é \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="37327-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="37327-134">i \# . w não é usado pelo bloco de loop e deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="37327-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="37327-135">Blocos de loop podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="37327-135">Loop blocks may be nested.</span></span> <span data-ttu-id="37327-136">Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="37327-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="37327-137">Quando aninhado, o valor do [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) refere-se ao bloco de loops de circunscrição imediato.</span><span class="sxs-lookup"><span data-stu-id="37327-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="37327-138">Os blocos de loops podem estar completamente dentro de um \* bloco If ou completamente em torno dele.</span><span class="sxs-lookup"><span data-stu-id="37327-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="37327-139">Não é permitido ampliar.</span><span class="sxs-lookup"><span data-stu-id="37327-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="37327-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="37327-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="37327-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37327-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37327-142">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="37327-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




