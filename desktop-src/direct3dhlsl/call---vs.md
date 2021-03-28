---
title: Call-vs
description: Executa uma chamada de função para a instrução marcada com o rótulo fornecido. | Call-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930520"
---
# <a name="call---vs"></a><span data-ttu-id="a1c9b-104">Call-vs</span><span class="sxs-lookup"><span data-stu-id="a1c9b-104">call - vs</span></span>

<span data-ttu-id="a1c9b-105">Executa uma chamada de função para a instrução marcada com o rótulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1c9b-106">Syntax</span></span>



| <span data-ttu-id="a1c9b-107">chamar l\#</span><span class="sxs-lookup"><span data-stu-id="a1c9b-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="a1c9b-108">Onde l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1c9b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1c9b-109">Remarks</span></span>



| <span data-ttu-id="a1c9b-110">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a1c9b-110">Vertex shader versions</span></span> | <span data-ttu-id="a1c9b-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1c9b-111">1\_1</span></span> | <span data-ttu-id="a1c9b-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1c9b-112">2\_0</span></span> | <span data-ttu-id="a1c9b-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-113">2\_x</span></span> | <span data-ttu-id="a1c9b-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1c9b-114">2\_sw</span></span> | <span data-ttu-id="a1c9b-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1c9b-115">3\_0</span></span> | <span data-ttu-id="a1c9b-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1c9b-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1c9b-117">chamada</span><span class="sxs-lookup"><span data-stu-id="a1c9b-117">call</span></span>                   |      | <span data-ttu-id="a1c9b-118">x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-118">x</span></span>    | <span data-ttu-id="a1c9b-119">x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-119">x</span></span>    | <span data-ttu-id="a1c9b-120">x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-120">x</span></span>     | <span data-ttu-id="a1c9b-121">x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-121">x</span></span>    | <span data-ttu-id="a1c9b-122">x</span><span class="sxs-lookup"><span data-stu-id="a1c9b-122">x</span></span>     |



 

<span data-ttu-id="a1c9b-123">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a1c9b-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="a1c9b-124">Endereço de push da próxima instrução para a pilha de endereços de retorno.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="a1c9b-125">Continue a execução da instrução marcada pelo rótulo.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="a1c9b-126">No sombreador de vértice 2 \_ 0, não são permitidas chamadas de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="a1c9b-127">No sombreador de vértice 2 \_ x, a profundidade de aninhamento é limitada pelo elemento StaticFlowControlDepth da estrutura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) .</span><span class="sxs-lookup"><span data-stu-id="a1c9b-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="a1c9b-128">Para obter mais informações, consulte [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="a1c9b-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="a1c9b-129">No sombreador de vértice 3 \_ 0, são permitidos quatro níveis de aninhamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="a1c9b-130">Somente chamadas de encaminhamento são permitidas.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-130">Only forward calls are allowed.</span></span> <span data-ttu-id="a1c9b-131">Isso significa que o local do rótulo dentro do sombreador de vértice deve ser após a instrução Call que faz referência a ele.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="a1c9b-132">Se uma instrução Call for invocada dentro do [loop](loop---vs.md)... bloco [ENDLOOP](endloop---vs.md) , o valor do [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) é acessível dentro da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="a1c9b-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="a1c9b-133">Se uma sub-rotina fizer referência ao [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) localizado fora da sub-rotina, cada instância da chamada para essa sub-rotina deverá ser circundada por um [loop](loop---vs.md)... bloco [ENDLOOP](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c9b-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c9b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1c9b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c9b-135">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a1c9b-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
