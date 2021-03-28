---
title: DSX-PS
description: Calcule a taxa de alteração na direção x do destino de renderização.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916883"
---
# <a name="dsx---ps"></a><span data-ttu-id="9c802-103">DSX-PS</span><span class="sxs-lookup"><span data-stu-id="9c802-103">dsx - ps</span></span>

<span data-ttu-id="9c802-104">Calcule a taxa de alteração na direção x do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9c802-104">Compute the rate of change in the render target's x-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c802-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c802-105">Syntax</span></span>



| <span data-ttu-id="9c802-106">DSX DST, src</span><span class="sxs-lookup"><span data-stu-id="9c802-106">dsx dst, src</span></span> |
|--------------|



 

<span data-ttu-id="9c802-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="9c802-107">Where:</span></span>

-   <span data-ttu-id="9c802-108">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9c802-108">dst is a destination register.</span></span>
-   <span data-ttu-id="9c802-109">src é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c802-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c802-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c802-110">Remarks</span></span>



| <span data-ttu-id="9c802-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9c802-111">Pixel shader versions</span></span> | <span data-ttu-id="9c802-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="9c802-112">1\_1</span></span> | <span data-ttu-id="9c802-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="9c802-113">1\_2</span></span> | <span data-ttu-id="9c802-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9c802-114">1\_3</span></span> | <span data-ttu-id="9c802-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="9c802-115">1\_4</span></span> | <span data-ttu-id="9c802-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c802-116">2\_0</span></span> | <span data-ttu-id="9c802-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9c802-117">2\_x</span></span> | <span data-ttu-id="9c802-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c802-118">2\_sw</span></span> | <span data-ttu-id="9c802-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c802-119">3\_0</span></span> | <span data-ttu-id="9c802-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c802-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9c802-121">dsx</span><span class="sxs-lookup"><span data-stu-id="9c802-121">dsx</span></span>                   |      |      |      |      |      | <span data-ttu-id="9c802-122">x</span><span class="sxs-lookup"><span data-stu-id="9c802-122">x</span></span>    | <span data-ttu-id="9c802-123">x</span><span class="sxs-lookup"><span data-stu-id="9c802-123">x</span></span>     | <span data-ttu-id="9c802-124">x</span><span class="sxs-lookup"><span data-stu-id="9c802-124">x</span></span>    | <span data-ttu-id="9c802-125">x</span><span class="sxs-lookup"><span data-stu-id="9c802-125">x</span></span>     |



 

<span data-ttu-id="9c802-126">A taxa de alterações computadas do registro de origem é uma aproximação no conteúdo do mesmo registro em pixels adjacentes que executam o sombreador de pixel na etapa de bloqueio com o pixel atual.</span><span class="sxs-lookup"><span data-stu-id="9c802-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="9c802-127">As instruções DSX e [DSY](dsy---ps.md) calculam o resultado examinando o conteúdo atual do registro de origem (por componente) para os vários pixels na área local em execução na etapa de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9c802-127">The dsx And [dsy](dsy---ps.md) instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="9c802-128">A fórmula exata usada para computar o gradiente varia de acordo com o hardware, mas deve ser consistente com a maneira como o hardware faz as mesmas operações como parte do processo de cálculo de nível de detalhe para amostragem de textura.</span><span class="sxs-lookup"><span data-stu-id="9c802-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c802-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c802-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c802-130">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9c802-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="9c802-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="9c802-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




