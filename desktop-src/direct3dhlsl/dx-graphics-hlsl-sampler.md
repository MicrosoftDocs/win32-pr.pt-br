---
title: Tipo de amostra
description: Use a sintaxe a seguir para declarar o estado de amostra, bem como o estado de comparação de amostra.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo de amostra HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007574"
---
# <a name="sampler-type"></a><span data-ttu-id="27ff2-104">Tipo de amostra</span><span class="sxs-lookup"><span data-stu-id="27ff2-104">Sampler Type</span></span>

<span data-ttu-id="27ff2-105">Use a sintaxe a seguir para declarar o estado de amostra, bem como o estado de comparação de amostra.</span><span class="sxs-lookup"><span data-stu-id="27ff2-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ff2-106">Diferenças entre o Direct3D 9 e o Direct3D 10 e posterior:</span><span class="sxs-lookup"><span data-stu-id="27ff2-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="27ff2-107">Aqui está a sintaxe de uma amostra no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="27ff2-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ff2-108"><em>nome</em>do classificador  =  <em>SampleType</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="27ff2-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="27ff2-109">A sintaxe de uma amostra no Direct3D 10 e posterior é ligeiramente alterada para dar suporte a objetos de textura e matrizes de amostra.</span><span class="sxs-lookup"><span data-stu-id="27ff2-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ff2-110"><em>Nome do classificador [índice]</em>{[<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="27ff2-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="27ff2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27ff2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27ff2-112"><span id="sampler"></span><span id="SAMPLER"></span>cores</span><span class="sxs-lookup"><span data-stu-id="27ff2-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-113">Somente Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="27ff2-113">Direct3D 9 only.</span></span> <span data-ttu-id="27ff2-114">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="27ff2-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="27ff2-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="27ff2-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-116">Cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de amostra.</span><span class="sxs-lookup"><span data-stu-id="27ff2-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="27ff2-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span><span class="sxs-lookup"><span data-stu-id="27ff2-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-118">Direct3D 10 e posterior somente.</span><span class="sxs-lookup"><span data-stu-id="27ff2-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="27ff2-119">Tamanho opcional da matriz; um inteiro positivo maior ou igual a 1.</span><span class="sxs-lookup"><span data-stu-id="27ff2-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="27ff2-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SampleType*</span><span class="sxs-lookup"><span data-stu-id="27ff2-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-121">\[no \] tipo de amostra, que é um dos seguintes: *amostra*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *\_ estado de amostra*, *samplestate*.</span><span class="sxs-lookup"><span data-stu-id="27ff2-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ff2-122">Diferenças entre o Direct3D 9 e o Direct3D 10 e posterior:</span><span class="sxs-lookup"><span data-stu-id="27ff2-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="27ff2-123">O Direct3D 10 e posterior dá suporte a um tipo de amostra adicional: *SamplerComparisonState*.</span><span class="sxs-lookup"><span data-stu-id="27ff2-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="27ff2-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*\_ variável de textura*>;</span><span class="sxs-lookup"><span data-stu-id="27ff2-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-125">Somente Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="27ff2-125">Direct3D 9 only.</span></span> <span data-ttu-id="27ff2-126">Uma variável de textura.</span><span class="sxs-lookup"><span data-stu-id="27ff2-126">A texture variable.</span></span> <span data-ttu-id="27ff2-127">A palavra-chave *Texture* é necessária no lado esquerdo; o nome da variável pertence ao lado direito da expressão dentro dos colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="27ff2-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="27ff2-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*nome do estado \_ = \_ valor do estado*</span><span class="sxs-lookup"><span data-stu-id="27ff2-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="27ff2-129">\[na \] (s) atribuição (ões) de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="27ff2-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="27ff2-130">O lado esquerdo de uma atribuição é um nome de estado, o lado direito é o valor de estado.</span><span class="sxs-lookup"><span data-stu-id="27ff2-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="27ff2-131">Todas as atribuições de estado devem aparecer dentro de um bloco de instruções (entre chaves).</span><span class="sxs-lookup"><span data-stu-id="27ff2-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="27ff2-132">Cada instrução é separada com um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="27ff2-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="27ff2-133">A tabela a seguir lista os possíveis nomes de estado.</span><span class="sxs-lookup"><span data-stu-id="27ff2-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="27ff2-134">O lado direito de cada expressão é o valor atribuído a cada Estado.</span><span class="sxs-lookup"><span data-stu-id="27ff2-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="27ff2-135">Consulte a [**estrutura \_ \_ desc de amostra D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) para obter os valores de estado possíveis para o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="27ff2-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="27ff2-136">Há uma relação de 1 a 1 entre os nomes de estado e os membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="27ff2-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="27ff2-137">Veja o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="27ff2-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27ff2-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="27ff2-138">Remarks</span></span>

<span data-ttu-id="27ff2-139">Quando você implementa um efeito, o estado de amostra é um dos vários tipos de estado que talvez você precise configurar no pipeline para renderização.</span><span class="sxs-lookup"><span data-stu-id="27ff2-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="27ff2-140">Para obter uma lista de todos os Estados possíveis que podem ser definidos em um efeito, consulte:</span><span class="sxs-lookup"><span data-stu-id="27ff2-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="27ff2-141">O Direct3D 10 usa [grupos de Estados](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="27ff2-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="27ff2-142">O Direct3D 9 usa [Estados](/windows/desktop/direct3d9/effect-states)individuais.</span><span class="sxs-lookup"><span data-stu-id="27ff2-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="27ff2-143">Exemplo</span><span class="sxs-lookup"><span data-stu-id="27ff2-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ff2-144">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="27ff2-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="27ff2-145">Aqui está um exemplo parcial de uma amostra do Direct3D 9 do <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">exemplo BasicHLSL</a>.</span><span class="sxs-lookup"><span data-stu-id="27ff2-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="27ff2-146">Aqui está um exemplo parcial de uma amostra do Direct3D 10 do <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">exemplo BasicHLSL10</a>.</span><span class="sxs-lookup"><span data-stu-id="27ff2-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="27ff2-147">Aqui está um exemplo parcial de declaração do estado de comparação de amostra e chamada de uma amostra de comparação no Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="27ff2-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="27ff2-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="27ff2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ff2-149">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27ff2-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

