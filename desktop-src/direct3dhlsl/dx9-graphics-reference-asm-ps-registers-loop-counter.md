---
title: Registro de contador de loop (referência de PS HLSL)
description: Leia sobre o registro do contador de loop para sombreadores de pixel. O único registro nesse banco é o registro do contador de loop atual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405509"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="3a7f7-104">Registro de contador de loop (referência de PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a7f7-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="3a7f7-105">O único registro nesse banco é o registro do contador de loop atual (aL).</span><span class="sxs-lookup"><span data-stu-id="3a7f7-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="3a7f7-106">Ele é incrementado automaticamente em cada execução do [loop – ps](loop---ps.md) / [endloop – bloco ps.](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="3a7f7-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="3a7f7-107">Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e é inválido para usá-lo fora do loop.</span><span class="sxs-lookup"><span data-stu-id="3a7f7-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="3a7f7-108">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3a7f7-108">Pixel shader versions</span></span> | <span data-ttu-id="3a7f7-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="3a7f7-109">1\_1</span></span> | <span data-ttu-id="3a7f7-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="3a7f7-110">1\_2</span></span> | <span data-ttu-id="3a7f7-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3a7f7-111">1\_3</span></span> | <span data-ttu-id="3a7f7-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="3a7f7-112">1\_4</span></span> | <span data-ttu-id="3a7f7-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a7f7-113">2\_0</span></span> | <span data-ttu-id="3a7f7-114">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3a7f7-114">2\_sw</span></span> | <span data-ttu-id="3a7f7-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3a7f7-115">2\_x</span></span> | <span data-ttu-id="3a7f7-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a7f7-116">3\_0</span></span> | <span data-ttu-id="3a7f7-117">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3a7f7-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="3a7f7-118">Registro de contador de loop</span><span class="sxs-lookup"><span data-stu-id="3a7f7-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="3a7f7-119">x</span><span class="sxs-lookup"><span data-stu-id="3a7f7-119">x</span></span>    | <span data-ttu-id="3a7f7-120">x</span><span class="sxs-lookup"><span data-stu-id="3a7f7-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="3a7f7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a7f7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a7f7-122">Registros</span><span class="sxs-lookup"><span data-stu-id="3a7f7-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




