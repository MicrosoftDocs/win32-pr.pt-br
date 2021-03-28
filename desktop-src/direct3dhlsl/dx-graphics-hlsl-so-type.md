---
title: Objeto Stream-Output
description: Um objeto Stream-output é um objeto modelo que transmite dados para fora do estágio Geometry-Shader. Use a sintaxe a seguir para declarar um objeto Stream-output.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366166"
---
# <a name="stream-output-object"></a><span data-ttu-id="90c37-104">Objeto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="90c37-104">Stream-Output Object</span></span>

<span data-ttu-id="90c37-105">Um objeto Stream-output é um objeto modelo que transmite dados para fora do [estágio Geometry-Shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90c37-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="90c37-106">Use a sintaxe a seguir para declarar um objeto Stream-output.</span><span class="sxs-lookup"><span data-stu-id="90c37-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="90c37-107">nome de DataType *StreamOutputObject* de InOut <  >  *;*</span><span class="sxs-lookup"><span data-stu-id="90c37-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="90c37-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90c37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c37-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Tipo de dados*  >    *Nome* do</span><span class="sxs-lookup"><span data-stu-id="90c37-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="90c37-110">A declaração do objeto Stream-Output (portanto).</span><span class="sxs-lookup"><span data-stu-id="90c37-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="90c37-111">Stream-Output tipos de objeto</span><span class="sxs-lookup"><span data-stu-id="90c37-111">Stream-Output Object Types</span></span> | <span data-ttu-id="90c37-112">Description</span><span class="sxs-lookup"><span data-stu-id="90c37-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="90c37-113">*PointStream*</span><span class="sxs-lookup"><span data-stu-id="90c37-113">*PointStream*</span></span>              | <span data-ttu-id="90c37-114">Uma sequência de primitivos de ponto</span><span class="sxs-lookup"><span data-stu-id="90c37-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="90c37-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="90c37-115">*LineStream*</span></span>               | <span data-ttu-id="90c37-116">Uma sequência de primitivas de linha</span><span class="sxs-lookup"><span data-stu-id="90c37-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="90c37-117">*TriangleStream*</span><span class="sxs-lookup"><span data-stu-id="90c37-117">*TriangleStream*</span></span>           | <span data-ttu-id="90c37-118">Uma sequência de primitivas de triângulo</span><span class="sxs-lookup"><span data-stu-id="90c37-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="90c37-119">*DataType* -tipo de dados de saída; pode ser qualquer [tipo de dados HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="90c37-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="90c37-120">Deve estar entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="90c37-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="90c37-121">*Nome-variável* nome; uma cadeia de caracteres ASCII que identifica exclusivamente o objeto.</span><span class="sxs-lookup"><span data-stu-id="90c37-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="90c37-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="90c37-122">Example</span></span>

<span data-ttu-id="90c37-123">Este é um exemplo de uma declaração de objeto de saída de fluxo que transfere primitivas de triângulo cujos dados são definidos pelo CUBEMAP do PS \_ \_ na estrutura.</span><span class="sxs-lookup"><span data-stu-id="90c37-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="90c37-124">O Geometry-Shader é limitado à geração de 18 vértices.</span><span class="sxs-lookup"><span data-stu-id="90c37-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="90c37-125">Este é um trecho de código do [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="90c37-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="90c37-126">Métodos de objeto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="90c37-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="90c37-127">Use a sintaxe a seguir para chamar métodos Stream-output-Object.</span><span class="sxs-lookup"><span data-stu-id="90c37-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="90c37-128">Os métodos a seguir são implementados.</span><span class="sxs-lookup"><span data-stu-id="90c37-128">The following methods are implemented.</span></span>



| <span data-ttu-id="90c37-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="90c37-129">Methods</span></span>                                              | <span data-ttu-id="90c37-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="90c37-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="90c37-131">Append</span><span class="sxs-lookup"><span data-stu-id="90c37-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="90c37-132">Acrescente dados de saída a um fluxo existente.</span><span class="sxs-lookup"><span data-stu-id="90c37-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="90c37-133">RestartStrip</span><span class="sxs-lookup"><span data-stu-id="90c37-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="90c37-134">Finalize a faixa primitiva atual e inicie uma nova faixa primitiva.</span><span class="sxs-lookup"><span data-stu-id="90c37-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90c37-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="90c37-135">Minimum Shader Model</span></span>

<span data-ttu-id="90c37-136">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="90c37-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="90c37-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="90c37-137">Shader Model</span></span>                                                        | <span data-ttu-id="90c37-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="90c37-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="90c37-139">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="90c37-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="90c37-140">sim</span><span class="sxs-lookup"><span data-stu-id="90c37-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="90c37-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90c37-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c37-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="90c37-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 