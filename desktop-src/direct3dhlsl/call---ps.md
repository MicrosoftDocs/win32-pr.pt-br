---
title: Call-PS
description: Executa uma chamada de função para a instrução marcada com o rótulo fornecido. | Call-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989186"
---
# <a name="call---ps"></a><span data-ttu-id="41d38-104">Call-PS</span><span class="sxs-lookup"><span data-stu-id="41d38-104">call - ps</span></span>

<span data-ttu-id="41d38-105">Executa uma chamada de função para a instrução marcada com o rótulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="41d38-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d38-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41d38-106">Syntax</span></span>



| <span data-ttu-id="41d38-107">chamar l\#</span><span class="sxs-lookup"><span data-stu-id="41d38-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="41d38-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="41d38-108">Where:</span></span>

-   <span data-ttu-id="41d38-109">l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="41d38-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d38-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="41d38-110">Remarks</span></span>



| <span data-ttu-id="41d38-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="41d38-111">Pixel shader versions</span></span> | <span data-ttu-id="41d38-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="41d38-112">1\_1</span></span> | <span data-ttu-id="41d38-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="41d38-113">1\_2</span></span> | <span data-ttu-id="41d38-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="41d38-114">1\_3</span></span> | <span data-ttu-id="41d38-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="41d38-115">1\_4</span></span> | <span data-ttu-id="41d38-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41d38-116">2\_0</span></span> | <span data-ttu-id="41d38-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="41d38-117">2\_x</span></span> | <span data-ttu-id="41d38-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41d38-118">2\_sw</span></span> | <span data-ttu-id="41d38-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41d38-119">3\_0</span></span> | <span data-ttu-id="41d38-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41d38-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="41d38-121">chamada</span><span class="sxs-lookup"><span data-stu-id="41d38-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="41d38-122">x</span><span class="sxs-lookup"><span data-stu-id="41d38-122">x</span></span>    | <span data-ttu-id="41d38-123">x</span><span class="sxs-lookup"><span data-stu-id="41d38-123">x</span></span>     | <span data-ttu-id="41d38-124">x</span><span class="sxs-lookup"><span data-stu-id="41d38-124">x</span></span>    | <span data-ttu-id="41d38-125">x</span><span class="sxs-lookup"><span data-stu-id="41d38-125">x</span></span>     |



 

<span data-ttu-id="41d38-126">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="41d38-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="41d38-127">Endereço de push da próxima instrução para a pilha de endereços de retorno.</span><span class="sxs-lookup"><span data-stu-id="41d38-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="41d38-128">Continue a execução da instrução marcada pelo rótulo.</span><span class="sxs-lookup"><span data-stu-id="41d38-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41d38-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41d38-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41d38-130">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="41d38-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




