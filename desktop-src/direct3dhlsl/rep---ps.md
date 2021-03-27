---
title: Rep-PS
description: Iniciar um representante... endrep-bloco de PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638864"
---
# <a name="rep---ps"></a><span data-ttu-id="b2f2a-103">Rep-PS</span><span class="sxs-lookup"><span data-stu-id="b2f2a-103">rep - ps</span></span>

<span data-ttu-id="b2f2a-104">Iniciar um representante... [endrep-bloco de PS](endrep---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f2a-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f2a-105">Syntax</span></span>



| <span data-ttu-id="b2f2a-106">representante i\#</span><span class="sxs-lookup"><span data-stu-id="b2f2a-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="b2f2a-107">onde eu \# é um registro de número inteiro que especifica a contagem de repetições no componente. x.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="b2f2a-108">Consulte [o registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="b2f2a-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f2a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2f2a-109">Remarks</span></span>



| <span data-ttu-id="b2f2a-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b2f2a-110">Pixel shader versions</span></span> | <span data-ttu-id="b2f2a-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="b2f2a-111">1\_1</span></span> | <span data-ttu-id="b2f2a-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="b2f2a-112">1\_2</span></span> | <span data-ttu-id="b2f2a-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b2f2a-113">1\_3</span></span> | <span data-ttu-id="b2f2a-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="b2f2a-114">1\_4</span></span> | <span data-ttu-id="b2f2a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2f2a-115">2\_0</span></span> | <span data-ttu-id="b2f2a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b2f2a-116">2\_x</span></span> | <span data-ttu-id="b2f2a-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2f2a-117">2\_sw</span></span> | <span data-ttu-id="b2f2a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2f2a-118">3\_0</span></span> | <span data-ttu-id="b2f2a-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2f2a-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b2f2a-120">representante</span><span class="sxs-lookup"><span data-stu-id="b2f2a-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="b2f2a-121">x</span><span class="sxs-lookup"><span data-stu-id="b2f2a-121">x</span></span>    | <span data-ttu-id="b2f2a-122">x</span><span class="sxs-lookup"><span data-stu-id="b2f2a-122">x</span></span>     | <span data-ttu-id="b2f2a-123">x</span><span class="sxs-lookup"><span data-stu-id="b2f2a-123">x</span></span>    | <span data-ttu-id="b2f2a-124">x</span><span class="sxs-lookup"><span data-stu-id="b2f2a-124">x</span></span>     |



 

-   <span data-ttu-id="b2f2a-125">i \# . x especifica a contagem de iteração.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="b2f2a-126">O intervalo legal é \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="b2f2a-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="b2f2a-127">Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="b2f2a-128">i \# . yzw não são usadas pelo bloco REPEAT.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="b2f2a-129">Os blocos de repetição podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="b2f2a-130">Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="b2f2a-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="b2f2a-131">Os blocos de repetição podem estar completamente dentro de um \* bloco If ou completamente em torno dele.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="b2f2a-132">Não é permitido ampliar.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="b2f2a-133">O uso do mesmo i \# para instruções de representante diferentes ou aninhadas é bem-cada loop será iterado com base na contagem especificada.</span><span class="sxs-lookup"><span data-stu-id="b2f2a-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="b2f2a-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b2f2a-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="b2f2a-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f2a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f2a-136">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b2f2a-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




