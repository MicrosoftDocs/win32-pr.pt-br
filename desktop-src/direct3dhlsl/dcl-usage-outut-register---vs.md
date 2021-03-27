---
title: saída de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Os vários tipos de registros de saída foram recolhidos em doze registros de saída (dois para cor, oito para textura, um para posição e outro para sombra e tamanho de ponto).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988694"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="47c74-103">\_saída de uso de DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="47c74-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="47c74-104">Os vários tipos de registros de saída foram recolhidos em doze registros de saída (dois para cor, oito para textura, um para posição e outro para sombra e tamanho de ponto).</span><span class="sxs-lookup"><span data-stu-id="47c74-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="47c74-105">Eles podem ser usados para qualquer coisa que o usuário queira interpolar para o sombreador de pixel: coordenadas de textura, cores, neblina e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="47c74-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="47c74-106">Os registros de saída exigem declarações que incluem semânticas.</span><span class="sxs-lookup"><span data-stu-id="47c74-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="47c74-107">Por exemplo, os registros de posição antiga e de tamanho de ponto são substituídos por meio da declaração de um registro de saída com uma semântica de posição ou de tamanho de ponto.</span><span class="sxs-lookup"><span data-stu-id="47c74-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="47c74-108">Dos doze registros de saída, quaisquer dez (não necessariamente o0 a O9) têm quatro componentes (xyzw), outro deve ser declarado como posição (e também deve incluir todos os quatro componentes) e, opcionalmente, mais um pode ser um tamanho de ponto escalar.</span><span class="sxs-lookup"><span data-stu-id="47c74-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c74-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c74-109">Syntax</span></span>

<span data-ttu-id="47c74-110">A sintaxe para declarar registros de saída é semelhante às declarações para o registro de entrada:</span><span class="sxs-lookup"><span data-stu-id="47c74-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="47c74-111">a semântica de DCL a \_ \[ . Write \_ Mask\]</span><span class="sxs-lookup"><span data-stu-id="47c74-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="47c74-112">Em que:</span><span class="sxs-lookup"><span data-stu-id="47c74-112">Where:</span></span>

-   <span data-ttu-id="47c74-113">a \_ semântica de DCL pode usar o mesmo conjunto de semânticas para a declaração de entrada.</span><span class="sxs-lookup"><span data-stu-id="47c74-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="47c74-114">Os nomes semânticos vêm de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e são emparelhados com um índice, como position3).</span><span class="sxs-lookup"><span data-stu-id="47c74-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="47c74-115">Sempre deve haver um registro de saída com a semântica positiont0 quando não for usado para processar vértices.</span><span class="sxs-lookup"><span data-stu-id="47c74-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="47c74-116">A semântica positiont0 e a semântica pointsize0 são as únicas que têm significado além de simplesmente permitir a vinculação de vértice a sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="47c74-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="47c74-117">Para sombreadores com controle de fluxo, supõe-se que a pior saída de caso seja declarada.</span><span class="sxs-lookup"><span data-stu-id="47c74-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="47c74-118">Não haverá padrões se um sombreador não gerar realmente o que ele declara (devido ao controle de fluxo).</span><span class="sxs-lookup"><span data-stu-id="47c74-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="47c74-119">o é um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="47c74-119">o is an output register.</span></span> <span data-ttu-id="47c74-120">Consulte [ \_ registros de saída](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="47c74-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="47c74-121">\_a máscara de gravação indica o mesmo registro de saída que pode ser declarado várias vezes (portanto, uma semântica diferente pode ser aplicada a componentes individuais), cada vez com uma máscara de gravação exclusiva.</span><span class="sxs-lookup"><span data-stu-id="47c74-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="47c74-122">No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração.</span><span class="sxs-lookup"><span data-stu-id="47c74-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="47c74-123">Isso significa que os vetores devem ter quatro componentes ou menos, e não podem passar pelos limites de registro de quatro componentes (registros individuais).</span><span class="sxs-lookup"><span data-stu-id="47c74-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="47c74-124">Quando a semântica de tamanho de ponto é usada, ela deve ter uma máscara de gravação completa porque é considerada uma escalar.</span><span class="sxs-lookup"><span data-stu-id="47c74-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="47c74-125">Quando a semântica de posição é usada, ela deve ter uma máscara de gravação completa porque todos os quatro componentes precisam ser escritos.</span><span class="sxs-lookup"><span data-stu-id="47c74-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c74-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c74-126">Remarks</span></span>



| <span data-ttu-id="47c74-127">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="47c74-127">Vertex shader versions</span></span> | <span data-ttu-id="47c74-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="47c74-128">3\_0</span></span> | <span data-ttu-id="47c74-129">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="47c74-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="47c74-130">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="47c74-130">dcl\_usage</span></span>             | <span data-ttu-id="47c74-131">x</span><span class="sxs-lookup"><span data-stu-id="47c74-131">x</span></span>    | <span data-ttu-id="47c74-132">x</span><span class="sxs-lookup"><span data-stu-id="47c74-132">x</span></span>     |



 

<span data-ttu-id="47c74-133">Todas as instruções de [ \_ uso de DCL](dcl-usage-input-register---vs.md) devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="47c74-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="47c74-134">Exemplos de declaração</span><span class="sxs-lookup"><span data-stu-id="47c74-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="47c74-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47c74-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c74-136">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="47c74-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 