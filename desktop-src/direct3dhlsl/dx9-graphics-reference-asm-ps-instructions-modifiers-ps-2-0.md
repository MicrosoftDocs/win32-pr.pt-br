---
title: Modificadores para ps_2_0 e superior
description: Modificadores de instrução afetam o resultado da instrução antes de ser gravado no registro de destino. Saiba mais sobre modificadores para ps_2_0 e acima.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989281"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="399e7-104">Modificadores para ps \_ 2 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="399e7-104">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="399e7-105">Modificadores de instrução afetam o resultado da instrução antes de ser gravado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="399e7-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="399e7-106">Esta seção contém informações de referência para os modificadores de instrução implementados pelo sombreador de pixel versão \_ 2 0 e superior.</span><span class="sxs-lookup"><span data-stu-id="399e7-106">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="399e7-107">Name</span><span class="sxs-lookup"><span data-stu-id="399e7-107">Name</span></span>                                     | <span data-ttu-id="399e7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="399e7-108">Syntax</span></span>     | <span data-ttu-id="399e7-109">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="399e7-109">2\_0</span></span> | <span data-ttu-id="399e7-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="399e7-110">2\_x</span></span> | <span data-ttu-id="399e7-111">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="399e7-111">2\_sw</span></span> | <span data-ttu-id="399e7-112">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="399e7-112">3\_0</span></span> | <span data-ttu-id="399e7-113">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="399e7-113">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="399e7-114">Centróide</span><span class="sxs-lookup"><span data-stu-id="399e7-114">Centroid</span></span>](#centroid)                    | <span data-ttu-id="399e7-115">\_Centróide</span><span class="sxs-lookup"><span data-stu-id="399e7-115">\_centroid</span></span> | <span data-ttu-id="399e7-116">x</span><span class="sxs-lookup"><span data-stu-id="399e7-116">x</span></span>    | <span data-ttu-id="399e7-117">x</span><span class="sxs-lookup"><span data-stu-id="399e7-117">x</span></span>    | <span data-ttu-id="399e7-118">x</span><span class="sxs-lookup"><span data-stu-id="399e7-118">x</span></span>     | <span data-ttu-id="399e7-119">x</span><span class="sxs-lookup"><span data-stu-id="399e7-119">x</span></span>    | <span data-ttu-id="399e7-120">x</span><span class="sxs-lookup"><span data-stu-id="399e7-120">x</span></span>     |
| [<span data-ttu-id="399e7-121">Precisão \_ parcial</span><span class="sxs-lookup"><span data-stu-id="399e7-121">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="399e7-122">\_Pp</span><span class="sxs-lookup"><span data-stu-id="399e7-122">\_pp</span></span>       | <span data-ttu-id="399e7-123">x</span><span class="sxs-lookup"><span data-stu-id="399e7-123">x</span></span>    | <span data-ttu-id="399e7-124">x</span><span class="sxs-lookup"><span data-stu-id="399e7-124">x</span></span>    | <span data-ttu-id="399e7-125">x</span><span class="sxs-lookup"><span data-stu-id="399e7-125">x</span></span>     | <span data-ttu-id="399e7-126">x</span><span class="sxs-lookup"><span data-stu-id="399e7-126">x</span></span>    | <span data-ttu-id="399e7-127">x</span><span class="sxs-lookup"><span data-stu-id="399e7-127">x</span></span>     |
| [<span data-ttu-id="399e7-128">Saturar</span><span class="sxs-lookup"><span data-stu-id="399e7-128">Saturate</span></span>](#saturate)                    | <span data-ttu-id="399e7-129">\_Sentado</span><span class="sxs-lookup"><span data-stu-id="399e7-129">\_sat</span></span>      | <span data-ttu-id="399e7-130">x</span><span class="sxs-lookup"><span data-stu-id="399e7-130">x</span></span>    | <span data-ttu-id="399e7-131">x</span><span class="sxs-lookup"><span data-stu-id="399e7-131">x</span></span>    | <span data-ttu-id="399e7-132">x</span><span class="sxs-lookup"><span data-stu-id="399e7-132">x</span></span>     | <span data-ttu-id="399e7-133">x</span><span class="sxs-lookup"><span data-stu-id="399e7-133">x</span></span>    | <span data-ttu-id="399e7-134">x</span><span class="sxs-lookup"><span data-stu-id="399e7-134">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="399e7-135">Centróide</span><span class="sxs-lookup"><span data-stu-id="399e7-135">Centroid</span></span>

<span data-ttu-id="399e7-136">O modificador centroide é um modificador opcional que fixa a interpolação de atributo dentro do intervalo do primitivo quando um centro de pixels multisamplo não é coberto pelo primitivo.</span><span class="sxs-lookup"><span data-stu-id="399e7-136">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="399e7-137">Isso pode ser visto em [Amostragem centroide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="399e7-137">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="399e7-138">Você pode aplicar o modificador de centroide a uma instrução de assembly, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="399e7-138">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="399e7-139">Você também pode aplicar o modificador de centroide a uma semântica, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="399e7-139">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="399e7-140">Além disso, qualquer [Registro de Cor de](dx9-graphics-reference-asm-ps-registers-input-color.md) Entrada (v ) declarado com uma semântica de cor terá \# automaticamente o centroide aplicado.</span><span class="sxs-lookup"><span data-stu-id="399e7-140">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="399e7-141">Gradientes computados de atributos que são amostrados por centroide não têm garantia de serem precisos.</span><span class="sxs-lookup"><span data-stu-id="399e7-141">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="399e7-142">Precisão parcial</span><span class="sxs-lookup"><span data-stu-id="399e7-142">Partial Precision</span></span>

<span data-ttu-id="399e7-143">O modificador de instrução de precisão parcial ( pp) indica áreas em que a precisão parcial é aceitável, desde que \_ a implementação subjacente seja compatível com ela.</span><span class="sxs-lookup"><span data-stu-id="399e7-143">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="399e7-144">As implementações são sempre livres para ignorar o modificador e executar as operações afetadas com precisão total.</span><span class="sxs-lookup"><span data-stu-id="399e7-144">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="399e7-145">O \_ modificador pp pode ocorrer em dois contextos:</span><span class="sxs-lookup"><span data-stu-id="399e7-145">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="399e7-146">Em uma declaração de coordenada de textura para habilitar a passagem de coordenadas de textura para o sombreador de pixel em formato de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="399e7-146">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="399e7-147">Isso permite, por exemplo, o uso de coordenadas de textura para retransmitir dados de cor para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações.</span><span class="sxs-lookup"><span data-stu-id="399e7-147">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="399e7-148">Na ausência desse modificador, as coordenadas de textura devem ser passadas com precisão total.</span><span class="sxs-lookup"><span data-stu-id="399e7-148">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="399e7-149">Em qualquer instrução, incluindo instruções de carregamento de textura.</span><span class="sxs-lookup"><span data-stu-id="399e7-149">On any instruction including texture load instructions.</span></span> <span data-ttu-id="399e7-150">Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="399e7-150">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="399e7-151">Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão de entrada).</span><span class="sxs-lookup"><span data-stu-id="399e7-151">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="399e7-152">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="399e7-152">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="399e7-153">Saturar</span><span class="sxs-lookup"><span data-stu-id="399e7-153">Saturate</span></span>

<span data-ttu-id="399e7-154">O modificador de instrução saturado (sáb) satura (ou fixa) o resultado da instrução para o intervalo 0, 1 antes de escrever \_ \[ no registro de \] destino.</span><span class="sxs-lookup"><span data-stu-id="399e7-154">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="399e7-155">O modificador de instrução sáb pode ser usado com qualquer instrução, exceto \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)e qualquer instrução de \* tex.</span><span class="sxs-lookup"><span data-stu-id="399e7-155">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="399e7-156">Para ps \_ 2 \_ 0, ps 2 x e \_ \_ ps \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)o modificador de instrução sáb não pode ser usado com instruções escritas em qualquer registro de saída (Registro de Cor de Saída ou Registro de Profundidade de Saída ).</span><span class="sxs-lookup"><span data-stu-id="399e7-156">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="399e7-157">Essa restrição não se aplica a ps \_ 3 \_ 0 e superior.</span><span class="sxs-lookup"><span data-stu-id="399e7-157">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="399e7-158">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="399e7-158">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="399e7-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="399e7-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="399e7-160">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="399e7-160">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




