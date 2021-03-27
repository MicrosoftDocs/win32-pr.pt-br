---
title: vs_2_0
description: Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967049"
---
# <a name="vs_2_0"></a><span data-ttu-id="7fd53-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7fd53-105">vs\_2\_0</span></span>

<span data-ttu-id="7fd53-106">Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="7fd53-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="7fd53-107">Registra dados de transferência dentro e fora da ALU.</span><span class="sxs-lookup"><span data-stu-id="7fd53-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="7fd53-108">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="7fd53-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="7fd53-109">[Instruções-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contém uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7fd53-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="7fd53-110">[Registros-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="7fd53-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="7fd53-111">Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="7fd53-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="7fd53-112">[Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="7fd53-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="7fd53-113">[O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="7fd53-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="7fd53-114">O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="7fd53-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="7fd53-115">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="7fd53-115">Instruction Count</span></span>

<span data-ttu-id="7fd53-116">Cada sombreador de vértice pode ter até 256 instruções armazenadas.</span><span class="sxs-lookup"><span data-stu-id="7fd53-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="7fd53-117">O número de instruções executadas pode ser muito maior (devido ao suporte de loop/Rep) e é limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que deve ser pelo menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="7fd53-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fd53-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fd53-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd53-119">Sombreadores de vértice</span><span class="sxs-lookup"><span data-stu-id="7fd53-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




