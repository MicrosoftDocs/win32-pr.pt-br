---
title: dcl_semantics (SM3-PS ASM)
description: Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084702"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="3a2ab-103">semântica de DCL \_ (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="3a2ab-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="3a2ab-104">Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a2ab-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="3a2ab-106">\_máscara de hora de Verão da semântica DCL \[ \_ centróide \] \[ . Write \_\]</span><span class="sxs-lookup"><span data-stu-id="3a2ab-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="3a2ab-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="3a2ab-107">Where:</span></span>

-   <span data-ttu-id="3a2ab-108">\_semântica: identifica o uso de dados pretendido e pode ser qualquer um dos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sem o \_ prefixo D3DDECLUSAGE).</span><span class="sxs-lookup"><span data-stu-id="3a2ab-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="3a2ab-109">Além disso, um índice inteiro pode ser anexado à semântica para distinguir parâmetros que usam semântica semelhante.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="3a2ab-110">\[\_[Centróide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] é um modificador de instrução opcional.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="3a2ab-111">Há suporte para as instruções de \_ uso do DCL que declaram os registros de entrada e as instruções de pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="3a2ab-112">O centróide é acrescentado sem espaço.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="3a2ab-113">DST: registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-113">dst: destination register.</span></span> <span data-ttu-id="3a2ab-114">Consulte [registros do PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="3a2ab-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="3a2ab-115">\_máscara de gravação: o mesmo registro de saída pode ser declarado várias vezes, cada vez com uma máscara de gravação exclusiva (de modo que uma semântica diferente pode ser aplicada a componentes individuais).</span><span class="sxs-lookup"><span data-stu-id="3a2ab-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="3a2ab-116">No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="3a2ab-117">Isso significa que os vetores devem ter quatro componentes ou menos, e não podem passar pelos limites de registro de quatro componentes (registros de saída individuais).</span><span class="sxs-lookup"><span data-stu-id="3a2ab-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="3a2ab-118">Quando a \_ semântica psize é usada, ela deve ter uma máscara de gravação completa porque é considerada uma escalar.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="3a2ab-119">Quando a \_ semântica de posição é usada, ela deve ter uma máscara de gravação completa porque todos os quatro componentes precisam ser escritos.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2ab-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a2ab-120">Remarks</span></span>



| <span data-ttu-id="3a2ab-121">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3a2ab-121">Pixel shader versions</span></span> | <span data-ttu-id="3a2ab-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="3a2ab-122">1\_1</span></span> | <span data-ttu-id="3a2ab-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="3a2ab-123">1\_2</span></span> | <span data-ttu-id="3a2ab-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3a2ab-124">1\_3</span></span> | <span data-ttu-id="3a2ab-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="3a2ab-125">1\_4</span></span> | <span data-ttu-id="3a2ab-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a2ab-126">2\_0</span></span> | <span data-ttu-id="3a2ab-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3a2ab-127">2\_x</span></span> | <span data-ttu-id="3a2ab-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a2ab-128">2\_sw</span></span> | <span data-ttu-id="3a2ab-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a2ab-129">3\_0</span></span> | <span data-ttu-id="3a2ab-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a2ab-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3a2ab-131">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="3a2ab-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="3a2ab-132">x</span><span class="sxs-lookup"><span data-stu-id="3a2ab-132">x</span></span>    | <span data-ttu-id="3a2ab-133">x</span><span class="sxs-lookup"><span data-stu-id="3a2ab-133">x</span></span>     |



 

<span data-ttu-id="3a2ab-134">Todas as \_ instruções de uso de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="3a2ab-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="3a2ab-135">Exemplos de declaração</span><span class="sxs-lookup"><span data-stu-id="3a2ab-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="3a2ab-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a2ab-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2ab-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3a2ab-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="3a2ab-138">[Exemplo de antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="3a2ab-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 