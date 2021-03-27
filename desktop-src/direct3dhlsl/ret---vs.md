---
title: RET-vs
description: Retornar de uma sub-rotina ou de uma função main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293563"
---
# <a name="ret---vs"></a><span data-ttu-id="2836f-103">RET-vs</span><span class="sxs-lookup"><span data-stu-id="2836f-103">ret - vs</span></span>

<span data-ttu-id="2836f-104">Retornar de uma sub-rotina ou de uma função main.</span><span class="sxs-lookup"><span data-stu-id="2836f-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2836f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2836f-105">Syntax</span></span>



| <span data-ttu-id="2836f-106">RET</span><span class="sxs-lookup"><span data-stu-id="2836f-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="2836f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2836f-107">Remarks</span></span>



| <span data-ttu-id="2836f-108">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="2836f-108">Vertex shader versions</span></span> | <span data-ttu-id="2836f-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="2836f-109">1\_1</span></span> | <span data-ttu-id="2836f-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2836f-110">2\_0</span></span> | <span data-ttu-id="2836f-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2836f-111">2\_x</span></span> | <span data-ttu-id="2836f-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2836f-112">2\_sw</span></span> | <span data-ttu-id="2836f-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2836f-113">3\_0</span></span> | <span data-ttu-id="2836f-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2836f-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2836f-115">RET</span><span class="sxs-lookup"><span data-stu-id="2836f-115">ret</span></span>                    |      | <span data-ttu-id="2836f-116">x</span><span class="sxs-lookup"><span data-stu-id="2836f-116">x</span></span>    | <span data-ttu-id="2836f-117">x</span><span class="sxs-lookup"><span data-stu-id="2836f-117">x</span></span>    | <span data-ttu-id="2836f-118">x</span><span class="sxs-lookup"><span data-stu-id="2836f-118">x</span></span>     | <span data-ttu-id="2836f-119">x</span><span class="sxs-lookup"><span data-stu-id="2836f-119">x</span></span>    | <span data-ttu-id="2836f-120">x</span><span class="sxs-lookup"><span data-stu-id="2836f-120">x</span></span>     |



 

<span data-ttu-id="2836f-121">Essa instrução usa o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela.</span><span class="sxs-lookup"><span data-stu-id="2836f-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="2836f-122">No caso da função main, essa instrução interrompe a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="2836f-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="2836f-123">A instrução RET consome um slot de instrução de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="2836f-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="2836f-124">Se um sombreador não contiver nenhuma sub-rotina, o uso de RET no final do programa principal será opcional.</span><span class="sxs-lookup"><span data-stu-id="2836f-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="2836f-125">Várias instruções de retorno não são permitidas no programa principal ou em qualquer sub-rotina, a primeira instrução de retorno é tratada como o fim do programa principal ou da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="2836f-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2836f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2836f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2836f-127">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="2836f-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




