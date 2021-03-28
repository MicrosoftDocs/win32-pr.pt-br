---
title: ps_1_1, ps_1_2, ps_1_3 ps_1_4
description: O Assembler do pixel shader é composto de um conjunto de instruções que operam em dados de pixel contidos em registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159280"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="9c628-103">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9c628-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="9c628-104">O Assembler do pixel shader é composto de um conjunto de instruções que operam em dados de pixel contidos em registros.</span><span class="sxs-lookup"><span data-stu-id="9c628-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="9c628-105">As operações são expressas como instruções compostas de um operador e um ou mais operandos.</span><span class="sxs-lookup"><span data-stu-id="9c628-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="9c628-106">As instruções usam registros para transferir dados para dentro e fora da ALU do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9c628-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="9c628-107">Os registros também podem ser usados por algumas instruções para manter resultados temporários.</span><span class="sxs-lookup"><span data-stu-id="9c628-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="9c628-108">O suporte do HLSL para o pixel shader 1. x foi preterido.</span><span class="sxs-lookup"><span data-stu-id="9c628-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="9c628-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="9c628-109">Instructions</span></span>

<span data-ttu-id="9c628-110">Há duas categorias principais de instruções de sombreador de pixel: instruções aritméticas e instruções de endereçamento de textura.</span><span class="sxs-lookup"><span data-stu-id="9c628-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="9c628-111">As instruções aritméticas modificam os dados de cores.</span><span class="sxs-lookup"><span data-stu-id="9c628-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="9c628-112">As operações de endereçamento de textura processam dados de coordenadas de textura e, na maioria dos casos, um exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="9c628-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="9c628-113">As instruções do sombreador de pixel são executadas em uma base por pixel; ou seja, eles não têm nenhum conhecimento de outros pixels no pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c628-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="9c628-114">As instruções de endereçamento de textura consomem um slot, mas as instruções aritméticas podem ser emparelhadas para habilitar os componentes de cor (RGB) e uma instrução de componente alfa em um único slot.</span><span class="sxs-lookup"><span data-stu-id="9c628-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="9c628-115">[as \_ instruções PS 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contêm uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9c628-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="9c628-116">Quando a multiamostragem está habilitada, os sombreadores de pixel só são executados uma vez por pixel, não uma vez para cada subpixel.</span><span class="sxs-lookup"><span data-stu-id="9c628-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="9c628-117">A multiamostração aumenta apenas a resolução das bordas do polígono, bem como os testes de profundidade e de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9c628-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="9c628-118">Por exemplo, se a multiamostragem 3x3 estiver habilitada e um triângulo sendo rasterizado for encontrado para cobrir cinco dos nove subpixels para um pixel específico, o sombreador de pixel será executado uma vez e o mesmo resultado de cor é aplicado a todos os cinco subpixels.</span><span class="sxs-lookup"><span data-stu-id="9c628-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="9c628-119">Registros</span><span class="sxs-lookup"><span data-stu-id="9c628-119">Registers</span></span>

<span data-ttu-id="9c628-120">[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lista os diferentes registros usados pela alu do sombreador.</span><span class="sxs-lookup"><span data-stu-id="9c628-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="9c628-121">Modificadores</span><span class="sxs-lookup"><span data-stu-id="9c628-121">Modifiers</span></span>

<span data-ttu-id="9c628-122">Os [modificadores para PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) podem ser usados para alterar a funcionalidade de uma instrução ou os dados lidos ou gravados em um registro.</span><span class="sxs-lookup"><span data-stu-id="9c628-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="9c628-123">O Direct3D 9 requer cálculos intermediários para manter pelo menos a precisão de 8 bits para todos os formatos de superfície.</span><span class="sxs-lookup"><span data-stu-id="9c628-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="9c628-124">É recomendável uma precisão mais alta (12 bits) para matemática em etapas e saturação para 8 bits entre estágios de textura.</span><span class="sxs-lookup"><span data-stu-id="9c628-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="9c628-125">Não há suporte para modos ou exceções de arredondamento modificáveis.</span><span class="sxs-lookup"><span data-stu-id="9c628-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="9c628-126">A multiplicação deve ser suportada com uma precisão de Round-to-mais próximo para manter o mínimo de perda de precisão.</span><span class="sxs-lookup"><span data-stu-id="9c628-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="9c628-127">Contagem de amostras</span><span class="sxs-lookup"><span data-stu-id="9c628-127">Sampler Count</span></span>

<span data-ttu-id="9c628-128">O número de amostragens de textura disponíveis é:</span><span class="sxs-lookup"><span data-stu-id="9c628-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="9c628-129">Para \_ o PS 1 \_ 0-PS \_ 1 \_ 3, o máximo é 4.</span><span class="sxs-lookup"><span data-stu-id="9c628-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="9c628-130">Para \_ o PS 1 \_ 4, o máximo é 6.</span><span class="sxs-lookup"><span data-stu-id="9c628-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c628-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c628-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c628-132">Sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="9c628-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




