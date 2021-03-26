---
title: Append (objeto Stream-Output do DirectX HLSL)
description: Acrescente dados geometry-Shader-output a um fluxo existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104293642"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="558b7-103">Append (objeto Stream-Output do DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="558b7-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="558b7-104">Acrescente dados geometry-Shader-output a um fluxo existente.</span><span class="sxs-lookup"><span data-stu-id="558b7-104">Append geometry-shader-output data to an existing stream.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="558b7-105">Append ( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="558b7-105">Append( *StreamDataType*);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="558b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="558b7-106">Parameters</span></span>



| <span data-ttu-id="558b7-107">Item</span><span class="sxs-lookup"><span data-stu-id="558b7-107">Item</span></span>                                                                                                                             | <span data-ttu-id="558b7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="558b7-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="558b7-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="558b7-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="558b7-110">Uma descrição de entrada de dados.</span><span class="sxs-lookup"><span data-stu-id="558b7-110">A data input description.</span></span> <span data-ttu-id="558b7-111">Essa descrição deve corresponder ao parâmetro de modelo de objeto de fluxo chamado [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="558b7-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="558b7-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="558b7-112">Return Value</span></span>

<span data-ttu-id="558b7-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="558b7-113">None</span></span>

## <a name="example"></a><span data-ttu-id="558b7-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="558b7-114">Example</span></span>

<span data-ttu-id="558b7-115">Este trecho de código (do [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) mostra um exemplo parcial de como acrescentar primitivos de faixa de triângulo a um objeto Stream-output.</span><span class="sxs-lookup"><span data-stu-id="558b7-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="558b7-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="558b7-116">Minimum Shader Model</span></span>

<span data-ttu-id="558b7-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="558b7-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="558b7-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="558b7-118">Shader Model</span></span>                                              | <span data-ttu-id="558b7-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="558b7-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="558b7-120">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="558b7-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="558b7-121">sim</span><span class="sxs-lookup"><span data-stu-id="558b7-121">yes</span></span>       |
| [<span data-ttu-id="558b7-122">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="558b7-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="558b7-123">não</span><span class="sxs-lookup"><span data-stu-id="558b7-123">no</span></span>        |
| [<span data-ttu-id="558b7-124">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="558b7-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="558b7-125">não</span><span class="sxs-lookup"><span data-stu-id="558b7-125">no</span></span>        |
| [<span data-ttu-id="558b7-126">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="558b7-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="558b7-127">não</span><span class="sxs-lookup"><span data-stu-id="558b7-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="558b7-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="558b7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="558b7-129">Fluxo-objeto de saída</span><span class="sxs-lookup"><span data-stu-id="558b7-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





