---
title: Modificadores para ps_2_0 e acima
description: Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823052"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="87cbb-103">Modificadores para PS \_ 2 \_ 0 e acima</span><span class="sxs-lookup"><span data-stu-id="87cbb-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="87cbb-104">Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="87cbb-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="87cbb-105">Esta seção contém informações de referência para os modificadores de instrução implementados pelo pixel shader versão 2 \_ 0 e superior.</span><span class="sxs-lookup"><span data-stu-id="87cbb-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="87cbb-106">Name</span><span class="sxs-lookup"><span data-stu-id="87cbb-106">Name</span></span>                                     | <span data-ttu-id="87cbb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87cbb-107">Syntax</span></span>     | <span data-ttu-id="87cbb-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="87cbb-108">2\_0</span></span> | <span data-ttu-id="87cbb-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="87cbb-109">2\_x</span></span> | <span data-ttu-id="87cbb-110">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="87cbb-110">2\_sw</span></span> | <span data-ttu-id="87cbb-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="87cbb-111">3\_0</span></span> | <span data-ttu-id="87cbb-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="87cbb-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="87cbb-113">Centróide</span><span class="sxs-lookup"><span data-stu-id="87cbb-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="87cbb-114">\_centróide</span><span class="sxs-lookup"><span data-stu-id="87cbb-114">\_centroid</span></span> | <span data-ttu-id="87cbb-115">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-115">x</span></span>    | <span data-ttu-id="87cbb-116">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-116">x</span></span>    | <span data-ttu-id="87cbb-117">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-117">x</span></span>     | <span data-ttu-id="87cbb-118">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-118">x</span></span>    | <span data-ttu-id="87cbb-119">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-119">x</span></span>     |
| [<span data-ttu-id="87cbb-120">\_Precisão parcial</span><span class="sxs-lookup"><span data-stu-id="87cbb-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="87cbb-121">\_PP</span><span class="sxs-lookup"><span data-stu-id="87cbb-121">\_pp</span></span>       | <span data-ttu-id="87cbb-122">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-122">x</span></span>    | <span data-ttu-id="87cbb-123">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-123">x</span></span>    | <span data-ttu-id="87cbb-124">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-124">x</span></span>     | <span data-ttu-id="87cbb-125">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-125">x</span></span>    | <span data-ttu-id="87cbb-126">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-126">x</span></span>     |
| [<span data-ttu-id="87cbb-127">Saturar</span><span class="sxs-lookup"><span data-stu-id="87cbb-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="87cbb-128">\_saturação</span><span class="sxs-lookup"><span data-stu-id="87cbb-128">\_sat</span></span>      | <span data-ttu-id="87cbb-129">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-129">x</span></span>    | <span data-ttu-id="87cbb-130">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-130">x</span></span>    | <span data-ttu-id="87cbb-131">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-131">x</span></span>     | <span data-ttu-id="87cbb-132">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-132">x</span></span>    | <span data-ttu-id="87cbb-133">x</span><span class="sxs-lookup"><span data-stu-id="87cbb-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="87cbb-134">Centróide</span><span class="sxs-lookup"><span data-stu-id="87cbb-134">Centroid</span></span>

<span data-ttu-id="87cbb-135">O modificador de centróide é um modificador opcional que coloca a interpolação de atributo dentro do intervalo do primitivo quando um centro de pixel com várias amostras não é coberto pelo primitivo.</span><span class="sxs-lookup"><span data-stu-id="87cbb-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="87cbb-136">Isso pode ser visto em [amostragem de centróide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="87cbb-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="87cbb-137">Você pode aplicar o modificador de centróide a uma instrução de assembly, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="87cbb-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="87cbb-138">Você também pode aplicar o modificador de centróide a uma semântica, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="87cbb-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="87cbb-139">Além disso, qualquer [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) declarado com uma semântica de cor terá automaticamente a centróide aplicada.</span><span class="sxs-lookup"><span data-stu-id="87cbb-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="87cbb-140">Gradientes computados de atributos que são de exemplo de centróide não têm garantia de serem precisas.</span><span class="sxs-lookup"><span data-stu-id="87cbb-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="87cbb-141">Precisão parcial</span><span class="sxs-lookup"><span data-stu-id="87cbb-141">Partial Precision</span></span>

<span data-ttu-id="87cbb-142">O modificador de instrução de precisão parcial ( \_ PP) indica áreas em que a precisão parcial é aceitável, desde que a implementação subjacente ofereça suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="87cbb-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="87cbb-143">As implementações sempre são gratuitas para ignorar o modificador e executar as operações afetadas com precisão total.</span><span class="sxs-lookup"><span data-stu-id="87cbb-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="87cbb-144">O \_ modificador PP pode ocorrer em dois contextos:</span><span class="sxs-lookup"><span data-stu-id="87cbb-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="87cbb-145">Em uma declaração de coordenada de textura para habilitar a passagem de coordenadas de textura para o sombreador de pixel em formato de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="87cbb-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="87cbb-146">Isso permite, por exemplo, o uso de coordenadas de textura para retransmitir dados de cores para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações.</span><span class="sxs-lookup"><span data-stu-id="87cbb-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="87cbb-147">Na ausência desse modificador, as coordenadas de textura devem ser passadas com precisão total.</span><span class="sxs-lookup"><span data-stu-id="87cbb-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="87cbb-148">Em qualquer instrução, incluindo instruções de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="87cbb-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="87cbb-149">Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="87cbb-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="87cbb-150">Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão de entrada).</span><span class="sxs-lookup"><span data-stu-id="87cbb-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="87cbb-151">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="87cbb-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="87cbb-152">Saturar</span><span class="sxs-lookup"><span data-stu-id="87cbb-152">Saturate</span></span>

<span data-ttu-id="87cbb-153">O modificador de instrução saturação ( \_ SAT) satura (ou coloca) o resultado da instrução para o intervalo de \[ 0, 1 \] antes de gravar no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="87cbb-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="87cbb-154">O \_ modificador de instrução SAT pode ser usado com qualquer instrução, exceto [FRC-PS](frc---ps.md), [Sincos-PS](sincos---ps.md)e quaisquer \* instruções Tex.</span><span class="sxs-lookup"><span data-stu-id="87cbb-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="87cbb-155">Para \_ \_ o software PS 2 0, PS \_ 2 \_ x e PS \_ 2 \_ SW, o \_ modificador de instrução SAT não pode ser usado com instruções de gravação em qualquer registro de saída (registro de cor de[saída](dx9-graphics-reference-asm-ps-registers-output-color.md) ou registro de profundidade de [saída](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="87cbb-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="87cbb-156">Essa restrição não se aplica ao PS \_ 3 \_ 0 e acima.</span><span class="sxs-lookup"><span data-stu-id="87cbb-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="87cbb-157">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="87cbb-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="87cbb-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87cbb-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87cbb-159">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="87cbb-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




