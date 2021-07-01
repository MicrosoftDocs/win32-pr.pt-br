---
title: CalculateLevelOfDetail (objeto de textura directX HLSL)
description: Calcula o nível de detalhes.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120551"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="fce19-103">CalculateLevelOfDetail (objeto de textura directX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fce19-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="fce19-104">Calcula o nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="fce19-104">Calculates the level of detail.</span></span>

<span data-ttu-id="fce19-105">ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );</span><span class="sxs-lookup"><span data-stu-id="fce19-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="fce19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fce19-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fce19-107">Item</span><span class="sxs-lookup"><span data-stu-id="fce19-107">Item</span></span></th>
<th><span data-ttu-id="fce19-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fce19-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fce19-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="fce19-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="fce19-110">Qualquer <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="fce19-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fce19-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="fce19-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="fce19-112">[in] Um <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">estado sampler</a>.</span><span class="sxs-lookup"><span data-stu-id="fce19-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="fce19-113">Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="fce19-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fce19-114"><span id="x"></span><span id="X"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="fce19-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="fce19-115">[in] O valor ou valores de interpolação linear, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="fce19-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="fce19-116">O número de componentes depende do tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="fce19-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fce19-117">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="fce19-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="fce19-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="fce19-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fce19-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fce19-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="fce19-120">float1</span><span class="sxs-lookup"><span data-stu-id="fce19-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fce19-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fce19-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="fce19-122">float2</span><span class="sxs-lookup"><span data-stu-id="fce19-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fce19-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fce19-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="fce19-124">float3</span><span class="sxs-lookup"><span data-stu-id="fce19-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="fce19-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fce19-125">Return Value</span></span>

<span data-ttu-id="fce19-126">Retorna o LOD calculado, um único valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="fce19-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fce19-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fce19-127">Minimum Shader Model</span></span>

<span data-ttu-id="fce19-128">Essa função tem suporte nos modelos de sombreador a seguir.</span><span class="sxs-lookup"><span data-stu-id="fce19-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fce19-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fce19-129">vs\_4\_0</span></span> | <span data-ttu-id="fce19-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fce19-130">vs\_4\_1</span></span>  | <span data-ttu-id="fce19-131">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fce19-131">ps\_4\_0</span></span> | <span data-ttu-id="fce19-132">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fce19-132">ps\_4\_1</span></span>  | <span data-ttu-id="fce19-133">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fce19-133">gs\_4\_0</span></span> | <span data-ttu-id="fce19-134">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fce19-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="fce19-135">x</span><span class="sxs-lookup"><span data-stu-id="fce19-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="fce19-136">TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="fce19-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="fce19-137">O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="fce19-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fce19-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fce19-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fce19-139">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="fce19-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

