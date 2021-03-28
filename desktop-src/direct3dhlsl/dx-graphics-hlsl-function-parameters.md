---
title: Argumentos da função
description: Uma função usa um ou mais argumentos de entrada; Use a sintaxe a seguir para declarar cada argumento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365490"
---
# <a name="function-arguments"></a><span data-ttu-id="19cae-103">Argumentos da função</span><span class="sxs-lookup"><span data-stu-id="19cae-103">Function Arguments</span></span>

<span data-ttu-id="19cae-104">Uma função usa um ou mais argumentos de entrada; Use a sintaxe a seguir para declarar cada argumento.</span><span class="sxs-lookup"><span data-stu-id="19cae-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cae-105">**\[\]Nome do tipo InputModifier \[ : Semantic \] \[ InterpolationModifier \] \[ = inicializadores\]**</span><span class="sxs-lookup"><span data-stu-id="19cae-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="19cae-106">\[Tipo de modificador \] nome \[ : semântica \] \[ : modificador de interpolação \] \[ = inicializador (s)\]</span><span class="sxs-lookup"><span data-stu-id="19cae-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="19cae-107">Se houver vários argumentos de função, eles serão separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="19cae-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="19cae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19cae-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19cae-109">Item</span><span class="sxs-lookup"><span data-stu-id="19cae-109">Item</span></span></th>
<th><span data-ttu-id="19cae-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="19cae-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19cae-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="19cae-112">Termo opcional que identifica um argumento como uma entrada, uma saída ou ambos.</span><span class="sxs-lookup"><span data-stu-id="19cae-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19cae-113">Valor</span><span class="sxs-lookup"><span data-stu-id="19cae-113">Value</span></span></td>
<td><span data-ttu-id="19cae-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="19cae-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19cae-115"><strong>Em</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="19cae-116">Somente entrada</span><span class="sxs-lookup"><span data-stu-id="19cae-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19cae-117"><strong>InOut</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="19cae-118">Entrada e uma saída</span><span class="sxs-lookup"><span data-stu-id="19cae-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19cae-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="19cae-120">Somente saída</span><span class="sxs-lookup"><span data-stu-id="19cae-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19cae-121"><strong>universal</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="19cae-122">Inserir somente dados constantes</span><span class="sxs-lookup"><span data-stu-id="19cae-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="19cae-123">Os parâmetros são sempre passados por valor.</span><span class="sxs-lookup"><span data-stu-id="19cae-123">Parameters are always passed by value.</span></span> <span data-ttu-id="19cae-124">no indica que o valor do parâmetro deve ser copiado do aplicativo de chamada antes que a função comece.</span><span class="sxs-lookup"><span data-stu-id="19cae-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="19cae-125">out indica que o último valor do parâmetro deve ser copiado e retornado ao aplicativo de chamada quando a função retornar.</span><span class="sxs-lookup"><span data-stu-id="19cae-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="19cae-126">Inout é uma abreviação para especificar ambos.</span><span class="sxs-lookup"><span data-stu-id="19cae-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="19cae-127">Um valor uniforme vem de um registro constante; cada invocação do sombreador de vértice ou de sombreador de pixel vê o mesmo valor inicial para uma variável uniforme.</span><span class="sxs-lookup"><span data-stu-id="19cae-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="19cae-128">As variáveis globais são tratadas como se fossem declaradas uniformes.</span><span class="sxs-lookup"><span data-stu-id="19cae-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="19cae-129">Para funções não de nível superior, uniforme é sinônimo de <strong>in</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cae-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="19cae-130">Se nenhum uso de parâmetro for especificado, o uso do parâmetro será considerado <strong>em</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cae-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19cae-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Escreva</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="19cae-132">O tipo de argumento; pode ser qualquer <a href="dx-graphics-hlsl-data-types.md">tipo</a>de HLSL válido.</span><span class="sxs-lookup"><span data-stu-id="19cae-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19cae-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nomes</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="19cae-134">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="19cae-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19cae-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semântico</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="19cae-136">Cadeia de caracteres opcional que identifica o uso pretendido dos dados (consulte a <a href="dx-graphics-hlsl-semantics.md">semântica (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="19cae-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19cae-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="19cae-138"><a href="dx-graphics-hlsl-struct.md">Modificador de interpolação</a> opcional que permite que um sombreador determine o método de interpolação.</span><span class="sxs-lookup"><span data-stu-id="19cae-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="19cae-139">Um modificador de interpolação em um argumento de função se aplica apenas a um argumento usado como uma entrada para uma função de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="19cae-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19cae-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inicializadores</strong></span><span class="sxs-lookup"><span data-stu-id="19cae-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="19cae-141">Valores opcionais para inicialização; vários valores são necessários para inicializar tipos de dados de vários componentes.</span><span class="sxs-lookup"><span data-stu-id="19cae-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="19cae-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="19cae-142">Remarks</span></span>

<span data-ttu-id="19cae-143">Os argumentos de função são listados em uma lista de argumentos separados por vírgula em uma declaração de função.</span><span class="sxs-lookup"><span data-stu-id="19cae-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="19cae-144">Como nas funções de C, cada argumento deve ter um nome de parâmetro e tipo declarado; um argumento para uma função HLSL opcionalmente pode incluir uma semântica, um valor inicial e uma entrada de sombreador de pixel pode incluir um tipo de interpolação.</span><span class="sxs-lookup"><span data-stu-id="19cae-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="19cae-145">O *tipo* de um argumento de função pode ser uma estrutura, que poderia incluir um modificador de interpolação por membro.</span><span class="sxs-lookup"><span data-stu-id="19cae-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="19cae-146">Se o argumento de função também tiver um modificador de interpolação, o modificador de argumento de função substituirá modificadores de interpolação declarados no tipo.</span><span class="sxs-lookup"><span data-stu-id="19cae-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="19cae-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19cae-147">Examples</span></span>

<span data-ttu-id="19cae-148">Este exemplo (do [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) ilustra entradas uniformes e não uniformes para uma função de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="19cae-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="19cae-149">Este exemplo (do [exemplo ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) usa uma estrutura de entrada para passar argumentos para uma função de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="19cae-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="19cae-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19cae-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19cae-151">Funções (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19cae-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





