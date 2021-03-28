---
title: Rep-vs
description: Iniciar um representante... bloco endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365217"
---
# <a name="rep---vs"></a><span data-ttu-id="0977b-103">Rep-vs</span><span class="sxs-lookup"><span data-stu-id="0977b-103">rep - vs</span></span>

<span data-ttu-id="0977b-104">Iniciar um representante... bloco [endrep](endrep---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="0977b-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="0977b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0977b-105">Syntax</span></span>



| <span data-ttu-id="0977b-106">representante i\#</span><span class="sxs-lookup"><span data-stu-id="0977b-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="0977b-107">onde eu \# é um registro de número inteiro que especifica a contagem de repetições no componente. x.</span><span class="sxs-lookup"><span data-stu-id="0977b-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="0977b-108">Consulte [o registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="0977b-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0977b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0977b-109">Remarks</span></span>



| <span data-ttu-id="0977b-110">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="0977b-110">Vertex shader versions</span></span> | <span data-ttu-id="0977b-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="0977b-111">1\_1</span></span> | <span data-ttu-id="0977b-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0977b-112">2\_0</span></span> | <span data-ttu-id="0977b-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0977b-113">2\_x</span></span> | <span data-ttu-id="0977b-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0977b-114">2\_sw</span></span> | <span data-ttu-id="0977b-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0977b-115">3\_0</span></span> | <span data-ttu-id="0977b-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0977b-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0977b-117">representante</span><span class="sxs-lookup"><span data-stu-id="0977b-117">rep</span></span>                    |      | <span data-ttu-id="0977b-118">x</span><span class="sxs-lookup"><span data-stu-id="0977b-118">x</span></span>    | <span data-ttu-id="0977b-119">x</span><span class="sxs-lookup"><span data-stu-id="0977b-119">x</span></span>    | <span data-ttu-id="0977b-120">x</span><span class="sxs-lookup"><span data-stu-id="0977b-120">x</span></span>     | <span data-ttu-id="0977b-121">x</span><span class="sxs-lookup"><span data-stu-id="0977b-121">x</span></span>    | <span data-ttu-id="0977b-122">x</span><span class="sxs-lookup"><span data-stu-id="0977b-122">x</span></span>     |



 

-   <span data-ttu-id="0977b-123">i \# . x especifica a contagem de iteração.</span><span class="sxs-lookup"><span data-stu-id="0977b-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="0977b-124">O intervalo legal é \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="0977b-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="0977b-125">Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="0977b-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="0977b-126">i \# . yzw não são usadas pelo bloco REPEAT.</span><span class="sxs-lookup"><span data-stu-id="0977b-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="0977b-127">Os blocos de repetição podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="0977b-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="0977b-128">Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="0977b-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="0977b-129">Os blocos de repetição podem estar completamente dentro de um \* bloco If ou completamente em torno dele.</span><span class="sxs-lookup"><span data-stu-id="0977b-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="0977b-130">Não é permitido ampliar.</span><span class="sxs-lookup"><span data-stu-id="0977b-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="0977b-131">O uso do mesmo i \# para instruções de representante diferentes ou aninhadas é bem-cada loop será iterado com base na contagem especificada.</span><span class="sxs-lookup"><span data-stu-id="0977b-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="0977b-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0977b-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="0977b-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0977b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0977b-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="0977b-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




