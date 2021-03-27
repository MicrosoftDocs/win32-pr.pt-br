---
title: CalculateLevelOfDetail (objeto de textura DirectX HLSL)
description: Calcula o nível de detalhe.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104967228"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="adfd3-103">CalculateLevelOfDetail (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="adfd3-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="adfd3-104">Calcula o nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="adfd3-104">Calculates the level of detail.</span></span>



|                                                                 |
|-----------------------------------------------------------------|
| <span data-ttu-id="adfd3-105">Ret. CalculateLevelOfDetail ( \_ estado de amostra S, float x);</span><span class="sxs-lookup"><span data-stu-id="adfd3-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="adfd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adfd3-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adfd3-107">Item</span><span class="sxs-lookup"><span data-stu-id="adfd3-107">Item</span></span></th>
<th><span data-ttu-id="adfd3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="adfd3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adfd3-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="adfd3-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="adfd3-110">Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="adfd3-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adfd3-111"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="adfd3-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="adfd3-112">no Um <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="adfd3-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="adfd3-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="adfd3-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adfd3-114"><span id="x"></span><span id="X"></span><em>w.x.y.</em></span><span class="sxs-lookup"><span data-stu-id="adfd3-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="adfd3-115">no O valor ou valores de interpolação linear, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="adfd3-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="adfd3-116">O número de componentes depende do tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="adfd3-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="adfd3-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="adfd3-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="adfd3-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="adfd3-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adfd3-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="adfd3-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="adfd3-120">float1</span><span class="sxs-lookup"><span data-stu-id="adfd3-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adfd3-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="adfd3-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="adfd3-122">float2</span><span class="sxs-lookup"><span data-stu-id="adfd3-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adfd3-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="adfd3-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="adfd3-124">float3</span><span class="sxs-lookup"><span data-stu-id="adfd3-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="adfd3-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="adfd3-125">Return Value</span></span>

<span data-ttu-id="adfd3-126">Retorna o LOD calculado, um único valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="adfd3-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="adfd3-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="adfd3-127">Minimum Shader Model</span></span>

<span data-ttu-id="adfd3-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="adfd3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="adfd3-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="adfd3-129">vs\_4\_0</span></span> | <span data-ttu-id="adfd3-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="adfd3-130">vs\_4\_1</span></span>  | <span data-ttu-id="adfd3-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="adfd3-131">ps\_4\_0</span></span> | <span data-ttu-id="adfd3-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="adfd3-132">ps\_4\_1</span></span>  | <span data-ttu-id="adfd3-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="adfd3-133">gs\_4\_0</span></span> | <span data-ttu-id="adfd3-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="adfd3-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="adfd3-135">x</span><span class="sxs-lookup"><span data-stu-id="adfd3-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="adfd3-136">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="adfd3-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="adfd3-137">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="adfd3-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adfd3-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adfd3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adfd3-139">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="adfd3-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

