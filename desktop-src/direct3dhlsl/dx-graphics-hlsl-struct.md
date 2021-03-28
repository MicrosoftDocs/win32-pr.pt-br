---
title: Tipo de struct
description: Tipo de struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo de struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104988539"
---
# <a name="struct-type"></a><span data-ttu-id="6d1ee-104">Tipo de struct</span><span class="sxs-lookup"><span data-stu-id="6d1ee-104">Struct Type</span></span>

<span data-ttu-id="6d1ee-105">Use a sintaxe a seguir para declarar uma estrutura usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-105">Use the following syntax to declare a structure using HLSL.</span></span>



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1ee-106">*nome* do struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="6d1ee-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6d1ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d1ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d1ee-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="6d1ee-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="6d1ee-109">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da estrutura.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="6d1ee-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="6d1ee-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1ee-111">Modificador opcional que especifica um tipo de interpolação.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="6d1ee-112">Consulte [Comentários](#remarks) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="6d1ee-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ de *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="6d1ee-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1ee-114">O tipo de membro com um tamanho de matriz de coluna (*C*) de linha opcional (*R*) x.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="6d1ee-115">Uma estrutura contém pelo menos um elemento; Se ele contiver mais de um elemento, os elementos serão todos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="6d1ee-116">O número de linhas e colunas são inteiros sem sinal entre 1 e 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="6d1ee-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span><span class="sxs-lookup"><span data-stu-id="6d1ee-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="6d1ee-118">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome do membro.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d1ee-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d1ee-119">Remarks</span></span>

<span data-ttu-id="6d1ee-120">Um modificador de interpolação pode ser especificado em qualquer membro da estrutura ou em um argumento para uma função de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="6d1ee-121">Se um modificador aparecer em ambos os locais, o modificador externo (o modificador de argumento do sombreador de pixel) ultrapassará o modificador interno (o modificador de estrutura).</span><span class="sxs-lookup"><span data-stu-id="6d1ee-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="6d1ee-122">Ao compilar um sombreador ou um efeito, o compilador do sombreador empacota os membros da estrutura de acordo com [as regras de empacotamento HLSL](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="6d1ee-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="6d1ee-123">Modificadores de interpolação introduzidos no modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6d1ee-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="6d1ee-124">As saídas de sombreador de vértice que são usadas para entradas de sombreador de pixel são interpoladas linearmente para obter valores por pixel durante a rasterização.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="6d1ee-125">Para definir o método de interpolação, use qualquer um dos valores a seguir, que têm suporte no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="6d1ee-126">O modificador é ignorado em qualquer saída de sombreador de vértice que não seja usada como entrada de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="6d1ee-127">Modificador de interpolação</span><span class="sxs-lookup"><span data-stu-id="6d1ee-127">Interpolation Modifier</span></span> | <span data-ttu-id="6d1ee-128">Description</span><span class="sxs-lookup"><span data-stu-id="6d1ee-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1ee-129">**linear**</span><span class="sxs-lookup"><span data-stu-id="6d1ee-129">**linear**</span></span>             | <span data-ttu-id="6d1ee-130">Interpolação entre entradas de sombreador; **linear** é o valor padrão se nenhum modificador de interpolação for especificado.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6d1ee-131">**centróide**</span><span class="sxs-lookup"><span data-stu-id="6d1ee-131">**centroid**</span></span>           | <span data-ttu-id="6d1ee-132">Interpolação entre exemplos que estão em algum lugar dentro da área coberta do pixel (isso pode exigir extrapolação de pontos de extremidade de um centro de pixel).</span><span class="sxs-lookup"><span data-stu-id="6d1ee-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="6d1ee-133">A amostragem de centróide pode melhorar a suavização se um pixel for parcialmente coberto (mesmo que o pixel Center não esteja coberto).</span><span class="sxs-lookup"><span data-stu-id="6d1ee-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="6d1ee-134">O modificador de **centróide** deve ser combinado com o modificador **linear** ou **noperspective** .</span><span class="sxs-lookup"><span data-stu-id="6d1ee-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6d1ee-135">**nointerpolação**</span><span class="sxs-lookup"><span data-stu-id="6d1ee-135">**nointerpolation**</span></span>    | <span data-ttu-id="6d1ee-136">Não interpolar.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="6d1ee-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="6d1ee-137">**noperspective**</span></span>      | <span data-ttu-id="6d1ee-138">Não execute a correção de perspectiva durante a interpolação.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="6d1ee-139">O modificador **noperspective** pode ser combinado com o modificador de **centróide** .</span><span class="sxs-lookup"><span data-stu-id="6d1ee-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6d1ee-140">**Nova**</span><span class="sxs-lookup"><span data-stu-id="6d1ee-140">**sample**</span></span>             | <span data-ttu-id="6d1ee-141">**Disponível no modelo do sombreador 4,1 e posterior** Interpolação no local de exemplo em vez de no pixel Center.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="6d1ee-142">Isso faz com que o sombreador de pixel seja executado por amostra em vez de por pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="6d1ee-143">Outra maneira de fazer com que a execução por amostra seja ter uma entrada com [ \_ SAMPLEINDEX de VA semântica](dx-graphics-hlsl-semantics.md), que indica o exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="6d1ee-144">Somente as entradas com **amostra** especificada (ou entrada de SAMPLEINDEX de VA \_ ) diferem entre invocações de sombreador no pixel, enquanto outras entradas que não especificam modificadores (por exemplo, se você misturar modificadores em diferentes entradas) ainda são interpoladas no pixel Center.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="6d1ee-145">A invocação do sombreador de pixel e o teste de profundidade/estêncil ocorrem para cada amostra coberta no pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="6d1ee-146">Isso às vezes é conhecido como *Superamostragem*.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="6d1ee-147">Por outro lado, na ausência de invocação de frequência de exemplo, conhecida como *multiamostral*, o sombreador de pixel é invocado uma vez por pixel, independentemente de quantas amostras são cobertas, enquanto o teste de profundidade/estêncil ocorre na frequência de amostragem.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="6d1ee-148">Ambos os modos fornecem anti-aliasing de borda equivalente.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="6d1ee-149">No entanto, a Superamostragem fornece melhor qualidade de sombreamento invocando o sombreador de pixel com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="6d1ee-150">1. Ao usar um tipo int/uint, a única opção válida é **nointerpolation**.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="6d1ee-151">Os modificadores de interpolação podem ser aplicados aos membros da estrutura ou aos [argumentos da função](dx-graphics-hlsl-function-parameters.md), ou ambos.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="6d1ee-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d1ee-152">Examples</span></span>

<span data-ttu-id="6d1ee-153">Aqui estão algumas declarações de estrutura de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="6d1ee-154">Essa declaração inclui uma matriz.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="6d1ee-155">Essa declaração inclui um modificador de interpolação.</span><span class="sxs-lookup"><span data-stu-id="6d1ee-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="6d1ee-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d1ee-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1ee-157">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d1ee-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





