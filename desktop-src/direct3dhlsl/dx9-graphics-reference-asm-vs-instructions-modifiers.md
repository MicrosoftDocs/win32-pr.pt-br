---
title: Modificadores de instrução (referência de HLSL VS)
description: Modificadores de instrução
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104453804"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="885a0-103">Modificadores de instrução (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="885a0-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="885a0-104">Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="885a0-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="885a0-105">\_saturação</span><span class="sxs-lookup"><span data-stu-id="885a0-105">\_sat</span></span>

<span data-ttu-id="885a0-106">Satura (ou coloca) o resultado da instrução para \[ 0, 1 \] intervalo antes de gravar no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="885a0-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="885a0-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="885a0-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="885a0-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="885a0-108">Where:</span></span>

<span data-ttu-id="885a0-109">DST = fixe \_ entre \_ 0 \_ e \_ 1 (src0 + src1)</span><span class="sxs-lookup"><span data-stu-id="885a0-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="885a0-110">O \_ modificador de instrução SAT não custa nenhum slot de instrução adicional.</span><span class="sxs-lookup"><span data-stu-id="885a0-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="885a0-111">Se houver suporte, o \_ modificador de instrução SAT pode ser usado com qualquer instrução, exceto: [FRC-vs](frc---vs.md), [Sincos-vs](sincos---vs.md)e [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="885a0-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="885a0-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="885a0-112">Vertex shader versions</span></span> | <span data-ttu-id="885a0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="885a0-113">1\_1</span></span> | <span data-ttu-id="885a0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="885a0-114">2\_0</span></span> | <span data-ttu-id="885a0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="885a0-115">2\_x</span></span> | <span data-ttu-id="885a0-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="885a0-116">2\_sw</span></span> | <span data-ttu-id="885a0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="885a0-117">3\_0</span></span> | <span data-ttu-id="885a0-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="885a0-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="885a0-119">\_saturação</span><span class="sxs-lookup"><span data-stu-id="885a0-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="885a0-120">x</span><span class="sxs-lookup"><span data-stu-id="885a0-120">x</span></span>    | <span data-ttu-id="885a0-121">x</span><span class="sxs-lookup"><span data-stu-id="885a0-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="885a0-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="885a0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885a0-123">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="885a0-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




