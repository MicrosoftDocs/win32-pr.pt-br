---
title: ps_2_0
description: Saiba mais ps_2_0, um sombreador de pixel programável, que é feito de um conjunto de instruções que operam em dados de pixel.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010979"
---
# <a name="ps_2_0"></a><span data-ttu-id="306ba-103">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="306ba-103">ps\_2\_0</span></span>

<span data-ttu-id="306ba-104">Um sombreador de pixel programável é feito de um conjunto de instruções que operam em dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="306ba-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="306ba-105">Registra dados de transferência dentro e fora do ALU.</span><span class="sxs-lookup"><span data-stu-id="306ba-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="306ba-106">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="306ba-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="306ba-107">[ps \_ 2 \_ 0 Instruções](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contém uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="306ba-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="306ba-108">[ps \_ 2 \_ 0 Registra lista](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="306ba-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="306ba-109">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="306ba-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="306ba-110">[A Máscara de Gravação do Registro de](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) Destino determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="306ba-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="306ba-111">[Modificadores de Registro de Origem do Sombreador de Pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados do registro de origem antes da instrução ser executado.</span><span class="sxs-lookup"><span data-stu-id="306ba-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="306ba-112">[O Swizzling do Registro de Origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="306ba-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="306ba-113">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="306ba-113">Instruction Count</span></span>

<span data-ttu-id="306ba-114">Os sombreadores têm restrições para contagens máximas de instruções.</span><span class="sxs-lookup"><span data-stu-id="306ba-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="306ba-115">Total de slots de instrução: 96 (aritmética de 64 e 32 textura).</span><span class="sxs-lookup"><span data-stu-id="306ba-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="306ba-116">Contagem de amostras</span><span class="sxs-lookup"><span data-stu-id="306ba-116">Sampler Count</span></span>

<span data-ttu-id="306ba-117">O número de amostras de textura disponíveis é 16.</span><span class="sxs-lookup"><span data-stu-id="306ba-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="306ba-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="306ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="306ba-119">Sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="306ba-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




