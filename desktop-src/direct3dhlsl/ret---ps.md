---
title: RET-PS
description: Pega o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela. No caso da função main, essa instrução interrompe a execução do sombreador.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967099"
---
# <a name="ret---ps"></a><span data-ttu-id="74811-104">RET-PS</span><span class="sxs-lookup"><span data-stu-id="74811-104">ret - ps</span></span>

<span data-ttu-id="74811-105">Pega o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela.</span><span class="sxs-lookup"><span data-stu-id="74811-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="74811-106">No caso da função main, essa instrução interrompe a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="74811-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="74811-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74811-107">Syntax</span></span>



| <span data-ttu-id="74811-108">RET</span><span class="sxs-lookup"><span data-stu-id="74811-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="74811-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="74811-109">Remarks</span></span>



| <span data-ttu-id="74811-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="74811-110">Pixel shader versions</span></span> | <span data-ttu-id="74811-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="74811-111">1\_1</span></span> | <span data-ttu-id="74811-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="74811-112">1\_2</span></span> | <span data-ttu-id="74811-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="74811-113">1\_3</span></span> | <span data-ttu-id="74811-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="74811-114">1\_4</span></span> | <span data-ttu-id="74811-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74811-115">2\_0</span></span> | <span data-ttu-id="74811-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="74811-116">2\_x</span></span> | <span data-ttu-id="74811-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="74811-117">2\_sw</span></span> | <span data-ttu-id="74811-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74811-118">3\_0</span></span> | <span data-ttu-id="74811-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="74811-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="74811-120">RET</span><span class="sxs-lookup"><span data-stu-id="74811-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="74811-121">x</span><span class="sxs-lookup"><span data-stu-id="74811-121">x</span></span>    | <span data-ttu-id="74811-122">x</span><span class="sxs-lookup"><span data-stu-id="74811-122">x</span></span>     | <span data-ttu-id="74811-123">x</span><span class="sxs-lookup"><span data-stu-id="74811-123">x</span></span>    | <span data-ttu-id="74811-124">x</span><span class="sxs-lookup"><span data-stu-id="74811-124">x</span></span>     |



 

<span data-ttu-id="74811-125">Essa instrução usa o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela.</span><span class="sxs-lookup"><span data-stu-id="74811-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="74811-126">No caso da função main, essa instrução interrompe a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="74811-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="74811-127">A instrução RET consome um slot de instrução de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="74811-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="74811-128">Se um sombreador não contiver nenhuma sub-rotina, o uso de RET no final do programa principal será opcional.</span><span class="sxs-lookup"><span data-stu-id="74811-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="74811-129">Várias instruções de retorno não são permitidas no programa principal ou em qualquer sub-rotina, a primeira instrução de retorno é tratada como o fim do programa principal ou da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="74811-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74811-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74811-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74811-131">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="74811-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




