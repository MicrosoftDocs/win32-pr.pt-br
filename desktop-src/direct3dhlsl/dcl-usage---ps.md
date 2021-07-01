---
title: dcl_semantics (sm3 – ps asm)
description: Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129703"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="0f2c6-103">\_semântica dcl (sm3 – ps asm)</span><span class="sxs-lookup"><span data-stu-id="0f2c6-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="0f2c6-104">Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f2c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f2c6-105">Syntax</span></span>

<span data-ttu-id="0f2c6-106">dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="0f2c6-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span>



 

<span data-ttu-id="0f2c6-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="0f2c6-107">Where:</span></span>

-   <span data-ttu-id="0f2c6-108">\_semantics: identifica o uso de dados pretendido e pode ser qualquer um dos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sem o prefixo D3DDECLUSAGE). \_</span><span class="sxs-lookup"><span data-stu-id="0f2c6-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="0f2c6-109">Além disso, um índice inteiro pode ser anexado à semântica para distinguir parâmetros que usam semântica semelhante.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="0f2c6-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] é um modificador de instrução opcional.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="0f2c6-111">Há suporte para ele nas instruções de uso de dcl que declaram os registros de entrada e as instruções de \_ lookup de textura.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="0f2c6-112">O centroide é anexado sem espaço.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="0f2c6-113">dst: registro de destino.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-113">dst: destination register.</span></span> <span data-ttu-id="0f2c6-114">Consulte [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="0f2c6-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="0f2c6-115">máscara de gravação: o mesmo registro de saída pode ser declarado várias vezes, cada vez com uma máscara de gravação exclusiva (para que uma semântica diferente possa ser \_ aplicada a componentes individuais).</span><span class="sxs-lookup"><span data-stu-id="0f2c6-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="0f2c6-116">No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="0f2c6-117">Isso significa que os vetores devem ser quatro componentes ou menos e não podem passar pelos limites de registro de quatro componentes (registros de saída individuais).</span><span class="sxs-lookup"><span data-stu-id="0f2c6-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="0f2c6-118">Quando a \_ semântica de psize é usada, ela deve ter uma máscara de gravação completa porque é considerada escalar.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="0f2c6-119">Quando a \_ semântica de posição é usada, ela deve ter máscara de gravação completa porque todos os quatro componentes devem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f2c6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f2c6-120">Remarks</span></span>



| <span data-ttu-id="0f2c6-121">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0f2c6-121">Pixel shader versions</span></span> | <span data-ttu-id="0f2c6-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="0f2c6-122">1\_1</span></span> | <span data-ttu-id="0f2c6-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="0f2c6-123">1\_2</span></span> | <span data-ttu-id="0f2c6-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0f2c6-124">1\_3</span></span> | <span data-ttu-id="0f2c6-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="0f2c6-125">1\_4</span></span> | <span data-ttu-id="0f2c6-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f2c6-126">2\_0</span></span> | <span data-ttu-id="0f2c6-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0f2c6-127">2\_x</span></span> | <span data-ttu-id="0f2c6-128">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="0f2c6-128">2\_sw</span></span> | <span data-ttu-id="0f2c6-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f2c6-129">3\_0</span></span> | <span data-ttu-id="0f2c6-130">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="0f2c6-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0f2c6-131">uso \_ de dcl</span><span class="sxs-lookup"><span data-stu-id="0f2c6-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="0f2c6-132">x</span><span class="sxs-lookup"><span data-stu-id="0f2c6-132">x</span></span>    | <span data-ttu-id="0f2c6-133">x</span><span class="sxs-lookup"><span data-stu-id="0f2c6-133">x</span></span>     |



 

<span data-ttu-id="0f2c6-134">Todas as instruções de uso de dcl \_ devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="0f2c6-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="0f2c6-135">Exemplos de declaração</span><span class="sxs-lookup"><span data-stu-id="0f2c6-135">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0f2c6-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f2c6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2c6-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0f2c6-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="0f2c6-138">[Exemplo de antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0f2c6-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
