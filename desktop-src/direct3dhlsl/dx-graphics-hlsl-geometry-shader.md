---
title: Objeto Geometry-Shader
description: Um objeto Geometry-Shader processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto Geometry-Shader.
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
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "103638986"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="94f1e-105">Objeto Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="94f1e-105">Geometry-Shader Object</span></span>

<span data-ttu-id="94f1e-106">Um objeto Geometry-Shader processa primitivos inteiros.</span><span class="sxs-lookup"><span data-stu-id="94f1e-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="94f1e-107">Use a sintaxe a seguir para declarar um objeto Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="94f1e-107">Use the following syntax to declare a geometry-shader object.</span></span>



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f1e-108">\[maxvertexcount (*NumVerts*) \] void *shadername* ( *Primitivatype nome do tipo de dados \[ \] NumElements*, inout *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="94f1e-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="94f1e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94f1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f1e-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-111">\[em \] declaração para o número máximo de vértices a serem criados.</span><span class="sxs-lookup"><span data-stu-id="94f1e-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="94f1e-112">\[maxvertexcount () \] -palavra-chave necessária; colchetes e parênteses são caracteres necessários para a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="94f1e-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="94f1e-113">*NumVerts* -um número inteiro que representa o número de vértices.</span><span class="sxs-lookup"><span data-stu-id="94f1e-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="94f1e-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*Shadername*</span><span class="sxs-lookup"><span data-stu-id="94f1e-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-115">\[em \] uma cadeia de caracteres ASCII que contém um nome exclusivo para a função Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="94f1e-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="94f1e-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nome do tipo de dados primitivotype \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="94f1e-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-117">Tipo *primitivo* -Primitive, que determina a ordem dos dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="94f1e-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="94f1e-118">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="94f1e-118">Primitive Type</span></span> | <span data-ttu-id="94f1e-119">Description</span><span class="sxs-lookup"><span data-stu-id="94f1e-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="94f1e-120">*empresas*</span><span class="sxs-lookup"><span data-stu-id="94f1e-120">*point*</span></span>        | <span data-ttu-id="94f1e-121">Lista de pontos</span><span class="sxs-lookup"><span data-stu-id="94f1e-121">Point list</span></span>                                                    |
| <span data-ttu-id="94f1e-122">*descritos*</span><span class="sxs-lookup"><span data-stu-id="94f1e-122">*line*</span></span>         | <span data-ttu-id="94f1e-123">Lista de linhas ou faixa de linha</span><span class="sxs-lookup"><span data-stu-id="94f1e-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="94f1e-124">*ângulo*</span><span class="sxs-lookup"><span data-stu-id="94f1e-124">*triangle*</span></span>     | <span data-ttu-id="94f1e-125">Lista de triângulos ou a faixa de triângulo</span><span class="sxs-lookup"><span data-stu-id="94f1e-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="94f1e-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="94f1e-126">*lineadj*</span></span>      | <span data-ttu-id="94f1e-127">Lista de linhas com adjacência ou faixa de linha com adjacência</span><span class="sxs-lookup"><span data-stu-id="94f1e-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="94f1e-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="94f1e-128">*triangleadj*</span></span>  | <span data-ttu-id="94f1e-129">Lista de triângulos com uma faixa de adjacência ou triângulo com adjacência</span><span class="sxs-lookup"><span data-stu-id="94f1e-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="94f1e-130">*Tipo de dados*  -  \[ em \] um tipo de dados de entrada, pode ser qualquer [tipo de dados HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="94f1e-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="94f1e-131">*Nome-nome* do argumento; Esta é uma cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="94f1e-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="94f1e-132">*NumElements* -tamanho da matriz da entrada, que depende do *primitivatype* , conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="94f1e-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="94f1e-133">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="94f1e-133">Primitive Type</span></span> | <span data-ttu-id="94f1e-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="94f1e-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f1e-135">*empresas*</span><span class="sxs-lookup"><span data-stu-id="94f1e-135">*point*</span></span>        | <span data-ttu-id="94f1e-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-136">\[1\]</span></span><br/> <span data-ttu-id="94f1e-137">Você opera em apenas um ponto por vez.</span><span class="sxs-lookup"><span data-stu-id="94f1e-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="94f1e-138">*descritos*</span><span class="sxs-lookup"><span data-stu-id="94f1e-138">*line*</span></span>         | <span data-ttu-id="94f1e-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-139">\[2\]</span></span><br/> <span data-ttu-id="94f1e-140">Uma linha requer dois vértices.</span><span class="sxs-lookup"><span data-stu-id="94f1e-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="94f1e-141">*ângulo*</span><span class="sxs-lookup"><span data-stu-id="94f1e-141">*triangle*</span></span>     | <span data-ttu-id="94f1e-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-142">\[3\]</span></span><br/> <span data-ttu-id="94f1e-143">Um triângulo requer três vértices.</span><span class="sxs-lookup"><span data-stu-id="94f1e-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="94f1e-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="94f1e-144">*lineadj*</span></span>      | <span data-ttu-id="94f1e-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-145">\[4\]</span></span><br/> <span data-ttu-id="94f1e-146">Um lineadj tem duas extremidades; Portanto, ele requer quatro vértices.</span><span class="sxs-lookup"><span data-stu-id="94f1e-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="94f1e-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="94f1e-147">*triangleadj*</span></span>  | <span data-ttu-id="94f1e-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-148">\[6\]</span></span><br/> <span data-ttu-id="94f1e-149">Uma triangleadj bordas mais três triângulos; Portanto, ele requer seis vértices.</span><span class="sxs-lookup"><span data-stu-id="94f1e-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94f1e-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="94f1e-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-151">A declaração do [objeto Stream-output](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="94f1e-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f1e-152">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="94f1e-152">Return Value</span></span>

<span data-ttu-id="94f1e-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="94f1e-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="94f1e-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="94f1e-154">Remarks</span></span>

<span data-ttu-id="94f1e-155">O diagrama a seguir mostra os vários tipos primitivos para um objeto de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="94f1e-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![Ilustração dos vários tipos primitivos para um objeto de sombreador Geometry](images/d3d11-gsinputs1.png)

<span data-ttu-id="94f1e-157">O diagrama a seguir mostra invocações de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="94f1e-157">The following diagram shows geometry shader invocations.</span></span>

![ilustração de invocações do sombreador de geometria](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="94f1e-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94f1e-159">Examples</span></span>

<span data-ttu-id="94f1e-160">Este exemplo é do exercício 1 do [Workshop 4,0 do sombreador do Direct3D 10](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="94f1e-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="94f1e-161">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="94f1e-161">Minimum Shader Model</span></span>

<span data-ttu-id="94f1e-162">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="94f1e-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="94f1e-163">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="94f1e-163">Shader Model</span></span>                                                        | <span data-ttu-id="94f1e-164">Com suporte</span><span class="sxs-lookup"><span data-stu-id="94f1e-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="94f1e-165">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="94f1e-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="94f1e-166">sim</span><span class="sxs-lookup"><span data-stu-id="94f1e-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="94f1e-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94f1e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f1e-168">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="94f1e-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





