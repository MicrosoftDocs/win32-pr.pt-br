---
title: DSY-PS
description: Calcule a taxa de alteração na direção y do destino de renderização.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365207"
---
# <a name="dsy---ps"></a><span data-ttu-id="31523-103">DSY-PS</span><span class="sxs-lookup"><span data-stu-id="31523-103">dsy - ps</span></span>

<span data-ttu-id="31523-104">Calcule a taxa de alteração na direção y do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="31523-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="31523-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31523-105">Syntax</span></span>



| <span data-ttu-id="31523-106">DSY DST, src</span><span class="sxs-lookup"><span data-stu-id="31523-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="31523-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="31523-107">Where:</span></span>

-   <span data-ttu-id="31523-108">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="31523-108">dst is a destination register.</span></span>
-   <span data-ttu-id="31523-109">src é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="31523-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="31523-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="31523-110">Remarks</span></span>



| <span data-ttu-id="31523-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="31523-111">Pixel shader versions</span></span> | <span data-ttu-id="31523-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="31523-112">1\_1</span></span> | <span data-ttu-id="31523-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="31523-113">1\_2</span></span> | <span data-ttu-id="31523-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="31523-114">1\_3</span></span> | <span data-ttu-id="31523-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="31523-115">1\_4</span></span> | <span data-ttu-id="31523-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31523-116">2\_0</span></span> | <span data-ttu-id="31523-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31523-117">2\_x</span></span> | <span data-ttu-id="31523-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31523-118">2\_sw</span></span> | <span data-ttu-id="31523-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31523-119">3\_0</span></span> | <span data-ttu-id="31523-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31523-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="31523-121">dsy</span><span class="sxs-lookup"><span data-stu-id="31523-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="31523-122">x</span><span class="sxs-lookup"><span data-stu-id="31523-122">x</span></span>    | <span data-ttu-id="31523-123">x</span><span class="sxs-lookup"><span data-stu-id="31523-123">x</span></span>     | <span data-ttu-id="31523-124">x</span><span class="sxs-lookup"><span data-stu-id="31523-124">x</span></span>    | <span data-ttu-id="31523-125">x</span><span class="sxs-lookup"><span data-stu-id="31523-125">x</span></span>     |



 

<span data-ttu-id="31523-126">A taxa de alterações computadas do registro de origem é uma aproximação no conteúdo do mesmo registro em pixels adjacentes que executam o sombreador de pixel na etapa de bloqueio com o pixel atual.</span><span class="sxs-lookup"><span data-stu-id="31523-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="31523-127">As instruções [DSX](dsx---ps.md) e DSY calculam o resultado examinando o conteúdo atual do registro de origem (por componente) para os vários pixels na área local em execução na etapa de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="31523-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="31523-128">A fórmula exata usada para computar o gradiente varia de acordo com o hardware, mas deve ser consistente com a maneira como o hardware faz as mesmas operações como parte do processo de cálculo de nível de detalhe para amostragem de textura.</span><span class="sxs-lookup"><span data-stu-id="31523-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31523-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31523-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31523-130">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="31523-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="31523-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="31523-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




