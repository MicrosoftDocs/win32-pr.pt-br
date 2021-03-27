---
title: Registro de contador de loop (referência do HLSL PS)
description: O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638915"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="0170d-103">Registro de contador de loop (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="0170d-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="0170d-104">O único registro nesse banco é o registro do contador de loops atual (aL).</span><span class="sxs-lookup"><span data-stu-id="0170d-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="0170d-105">Ele é incrementado automaticamente em cada execução do bloco de [bits do loop PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0170d-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="0170d-106">Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.</span><span class="sxs-lookup"><span data-stu-id="0170d-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="0170d-107">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0170d-107">Pixel shader versions</span></span> | <span data-ttu-id="0170d-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="0170d-108">1\_1</span></span> | <span data-ttu-id="0170d-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="0170d-109">1\_2</span></span> | <span data-ttu-id="0170d-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0170d-110">1\_3</span></span> | <span data-ttu-id="0170d-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="0170d-111">1\_4</span></span> | <span data-ttu-id="0170d-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0170d-112">2\_0</span></span> | <span data-ttu-id="0170d-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0170d-113">2\_sw</span></span> | <span data-ttu-id="0170d-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0170d-114">2\_x</span></span> | <span data-ttu-id="0170d-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0170d-115">3\_0</span></span> | <span data-ttu-id="0170d-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0170d-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="0170d-117">Registro de contador de loop</span><span class="sxs-lookup"><span data-stu-id="0170d-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="0170d-118">x</span><span class="sxs-lookup"><span data-stu-id="0170d-118">x</span></span>    | <span data-ttu-id="0170d-119">x</span><span class="sxs-lookup"><span data-stu-id="0170d-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="0170d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0170d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0170d-121">Register</span><span class="sxs-lookup"><span data-stu-id="0170d-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




