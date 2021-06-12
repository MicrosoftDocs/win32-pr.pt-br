---
title: vs_2_0
description: Saiba mais vs_2_0, um sombreador de vértice programável, que é feito de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010849"
---
# <a name="vs_2_0"></a><span data-ttu-id="172c0-103">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="172c0-103">vs\_2\_0</span></span>

<span data-ttu-id="172c0-104">Um sombreador de vértice programável é feito de um conjunto de instruções que operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="172c0-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="172c0-105">Registra dados de transferência dentro e fora do ALU.</span><span class="sxs-lookup"><span data-stu-id="172c0-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="172c0-106">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="172c0-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="172c0-107">[Instruções – vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contém uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="172c0-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="172c0-108">[Registros – vs \_ 2 \_ 0 lista](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="172c0-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="172c0-109">[Modificadores de registro de sombreador de](dx9-graphics-reference-asm-vs-registers-modifiers.md) vértice são usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="172c0-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="172c0-110">[Modificadores de Registro de Origem do Sombreador de Vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da instrução ser executado.</span><span class="sxs-lookup"><span data-stu-id="172c0-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="172c0-111">[O Swizzling do Registro de Origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="172c0-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="172c0-112">[O Mascaramento do Registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) Destino determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="172c0-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="172c0-113">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="172c0-113">Instruction Count</span></span>

<span data-ttu-id="172c0-114">Cada sombreador de vértice pode ter até 256 instruções armazenadas.</span><span class="sxs-lookup"><span data-stu-id="172c0-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="172c0-115">O número de instruções executados pode ser muito maior (devido ao suporte de loop/rep) e é limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que deve ser pelo menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="172c0-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="172c0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="172c0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172c0-117">Sombreadores de vértice</span><span class="sxs-lookup"><span data-stu-id="172c0-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




