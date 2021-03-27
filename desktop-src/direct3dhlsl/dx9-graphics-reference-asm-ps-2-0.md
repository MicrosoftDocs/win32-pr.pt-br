---
title: ps_2_0
description: Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104966989"
---
# <a name="ps_2_0"></a><span data-ttu-id="44c37-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="44c37-105">ps\_2\_0</span></span>

<span data-ttu-id="44c37-106">Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="44c37-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="44c37-107">Registra dados de transferência dentro e fora da ALU.</span><span class="sxs-lookup"><span data-stu-id="44c37-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="44c37-108">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="44c37-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="44c37-109">[as \_ instruções do PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contêm uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="44c37-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="44c37-110">[os \_ registros PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="44c37-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="44c37-111">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="44c37-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="44c37-112">A [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="44c37-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="44c37-113">[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="44c37-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="44c37-114">[O Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="44c37-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="44c37-115">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="44c37-115">Instruction Count</span></span>

<span data-ttu-id="44c37-116">Os sombreadores têm restrições para contagens de instrução máximas.</span><span class="sxs-lookup"><span data-stu-id="44c37-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="44c37-117">Slots de instrução total: 96 (64 aritmética e 32 Texture).</span><span class="sxs-lookup"><span data-stu-id="44c37-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="44c37-118">Contagem de amostras</span><span class="sxs-lookup"><span data-stu-id="44c37-118">Sampler Count</span></span>

<span data-ttu-id="44c37-119">O número de amostragens de textura disponíveis é 16.</span><span class="sxs-lookup"><span data-stu-id="44c37-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c37-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44c37-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c37-121">Sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="44c37-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




