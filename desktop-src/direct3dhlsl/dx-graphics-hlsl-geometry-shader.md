---
title: Geometry-Shader objeto
description: Um objeto de sombreador de geometria processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto de sombreador de geometria.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120611"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="e19a8-105">Geometry-Shader objeto</span><span class="sxs-lookup"><span data-stu-id="e19a8-105">Geometry-Shader Object</span></span>

<span data-ttu-id="e19a8-106">Um objeto de sombreador de geometria processa primitivos inteiros.</span><span class="sxs-lookup"><span data-stu-id="e19a8-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="e19a8-107">Use a sintaxe a seguir para declarar um objeto de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="e19a8-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="e19a8-108">\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements, \]* inout *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="e19a8-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e19a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e19a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19a8-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a8-111">\[em \] Declaração para o número máximo de vértices a criar.</span><span class="sxs-lookup"><span data-stu-id="e19a8-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="e19a8-112">\[maxvertexcount() \] – palavra-chave necessária; colchetes e parênteses são caracteres necessários para a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="e19a8-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="e19a8-113">*NumVerts* – um número inteiro que representa o número de vértices.</span><span class="sxs-lookup"><span data-stu-id="e19a8-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e19a8-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="e19a8-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="e19a8-115">\[em \] uma cadeia de caracteres ASCII que contém um nome exclusivo para a função geometry-shader.</span><span class="sxs-lookup"><span data-stu-id="e19a8-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="e19a8-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*NumElements de nome primitiveType DataType \[\]*</span><span class="sxs-lookup"><span data-stu-id="e19a8-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="e19a8-117">*PrimitiveType* – tipo primitivo, que determina a ordem dos dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="e19a8-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="e19a8-118">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="e19a8-118">Primitive Type</span></span> | <span data-ttu-id="e19a8-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e19a8-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="e19a8-120">*Ponto*</span><span class="sxs-lookup"><span data-stu-id="e19a8-120">*point*</span></span>        | <span data-ttu-id="e19a8-121">Lista de pontos</span><span class="sxs-lookup"><span data-stu-id="e19a8-121">Point list</span></span>                                                    |
| <span data-ttu-id="e19a8-122">*Linha*</span><span class="sxs-lookup"><span data-stu-id="e19a8-122">*line*</span></span>         | <span data-ttu-id="e19a8-123">Lista de linhas ou faixa de linhas</span><span class="sxs-lookup"><span data-stu-id="e19a8-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="e19a8-124">*Triângulo*</span><span class="sxs-lookup"><span data-stu-id="e19a8-124">*triangle*</span></span>     | <span data-ttu-id="e19a8-125">Lista de triângulos ou faixa de triângulo</span><span class="sxs-lookup"><span data-stu-id="e19a8-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="e19a8-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="e19a8-126">*lineadj*</span></span>      | <span data-ttu-id="e19a8-127">Lista de linhas com adjacency ou faixa de linha com adjacency</span><span class="sxs-lookup"><span data-stu-id="e19a8-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="e19a8-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="e19a8-128">*triangleadj*</span></span>  | <span data-ttu-id="e19a8-129">Lista de triângulos com adjacency ou faixa de triângulo com adjacency</span><span class="sxs-lookup"><span data-stu-id="e19a8-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="e19a8-130">*DataType*  -  \[ em \] Um tipo de dados de entrada; pode ser qualquer tipo de dados [HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="e19a8-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="e19a8-131">*Nome* – Nome do argumento; esta é uma cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="e19a8-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="e19a8-132">*NumElements* – tamanho da matriz da entrada, que depende *do PrimitiveType,* conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e19a8-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="e19a8-133">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="e19a8-133">Primitive Type</span></span> | <span data-ttu-id="e19a8-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="e19a8-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e19a8-135">*Ponto*</span><span class="sxs-lookup"><span data-stu-id="e19a8-135">*point*</span></span>        | <span data-ttu-id="e19a8-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-136">\[1\]</span></span><br/> <span data-ttu-id="e19a8-137">Você opera em apenas um ponto por vez.</span><span class="sxs-lookup"><span data-stu-id="e19a8-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="e19a8-138">*Linha*</span><span class="sxs-lookup"><span data-stu-id="e19a8-138">*line*</span></span>         | <span data-ttu-id="e19a8-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-139">\[2\]</span></span><br/> <span data-ttu-id="e19a8-140">Uma linha requer dois vértices.</span><span class="sxs-lookup"><span data-stu-id="e19a8-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="e19a8-141">*Triângulo*</span><span class="sxs-lookup"><span data-stu-id="e19a8-141">*triangle*</span></span>     | <span data-ttu-id="e19a8-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-142">\[3\]</span></span><br/> <span data-ttu-id="e19a8-143">Um triângulo requer três vértices.</span><span class="sxs-lookup"><span data-stu-id="e19a8-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="e19a8-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="e19a8-144">*lineadj*</span></span>      | <span data-ttu-id="e19a8-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-145">\[4\]</span></span><br/> <span data-ttu-id="e19a8-146">Um lineadj tem duas extremidades; portanto, ele requer quatro vértices.</span><span class="sxs-lookup"><span data-stu-id="e19a8-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="e19a8-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="e19a8-147">*triangleadj*</span></span>  | <span data-ttu-id="e19a8-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="e19a8-148">\[6\]</span></span><br/> <span data-ttu-id="e19a8-149">Um triânguloadj faz a bordas de mais três triângulos; portanto, ele requer seis vértices.</span><span class="sxs-lookup"><span data-stu-id="e19a8-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e19a8-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="e19a8-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="e19a8-151">A declaração do [objeto stream-output](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="e19a8-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19a8-152">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e19a8-152">Return Value</span></span>

<span data-ttu-id="e19a8-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e19a8-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="e19a8-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="e19a8-154">Remarks</span></span>

<span data-ttu-id="e19a8-155">O diagrama a seguir mostra os vários tipos primitivos para um objeto de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="e19a8-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![ilustração dos vários tipos primitivos para um objeto de sombreador de geometria](images/d3d11-gsinputs1.png)

<span data-ttu-id="e19a8-157">O diagrama a seguir mostra invocações de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="e19a8-157">The following diagram shows geometry shader invocations.</span></span>

![ilustração de invocações de sombreador de geometria](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="e19a8-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e19a8-159">Examples</span></span>

<span data-ttu-id="e19a8-160">Este exemplo é do exercício 1 do Workshop do Modelo de Sombreador [4.0 do Direct3D 10.](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e19a8-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e19a8-161">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e19a8-161">Minimum Shader Model</span></span>

<span data-ttu-id="e19a8-162">Esse objeto tem suporte nos modelos de sombreador a seguir.</span><span class="sxs-lookup"><span data-stu-id="e19a8-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e19a8-163">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e19a8-163">Shader Model</span></span>                                                        | <span data-ttu-id="e19a8-164">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e19a8-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="e19a8-165">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior</span><span class="sxs-lookup"><span data-stu-id="e19a8-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="e19a8-166">yes</span><span class="sxs-lookup"><span data-stu-id="e19a8-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="e19a8-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e19a8-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e19a8-168">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e19a8-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





