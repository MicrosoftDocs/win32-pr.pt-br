---
description: Crie um Atlas UV para uma malha.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Função D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787706"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="a9d98-103">Função D3DXUVAtlasCreate</span><span class="sxs-lookup"><span data-stu-id="a9d98-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="a9d98-104">Crie um Atlas UV para uma malha.</span><span class="sxs-lookup"><span data-stu-id="a9d98-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9d98-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="a9d98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d98-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a9d98-109">Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="a9d98-110">No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a9d98-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-111">*dwMaxChartNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-113">O número máximo de gráficos para particionar a malha.</span><span class="sxs-lookup"><span data-stu-id="a9d98-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="a9d98-114">Consulte comentários sobre os modos de particionamento.</span><span class="sxs-lookup"><span data-stu-id="a9d98-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="a9d98-115">Use 0 para informar ao D3DX que o Atlas deve ser parametrizado com base na ampliação.</span><span class="sxs-lookup"><span data-stu-id="a9d98-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-116">*fMaxStretch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-118">A quantidade de alongamento permitida.</span><span class="sxs-lookup"><span data-stu-id="a9d98-118">The amount of stretching allowed.</span></span> <span data-ttu-id="a9d98-119">0 significa que nenhum alongamento é permitido, 1 significa que qualquer quantidade de alongamento pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="a9d98-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-120">*dwWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-122">Largura da textura.</span><span class="sxs-lookup"><span data-stu-id="a9d98-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-123">*dwHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-125">Altura da textura.</span><span class="sxs-lookup"><span data-stu-id="a9d98-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-126">*fGutter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-128">A distância mínima, em texels, entre dois gráficos no Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="a9d98-129">A medianiz sempre é dimensionada pela largura; Portanto, se uma medianiz de 2,5 for usada em uma textura 512x512, a distância mínima entre dois gráficos será 2,5/512,0 texels.</span><span class="sxs-lookup"><span data-stu-id="a9d98-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-130">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-132">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a9d98-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-133">*pdwAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-134">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9d98-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d98-135">Um ponteiro para uma matriz de dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="a9d98-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="a9d98-136">com 3 DWORDs por face, indicando quais triângulos são adjacentes entre si (consulte [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="a9d98-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="a9d98-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d98-138">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9d98-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d98-139">Uma matriz com 3 DWORDs por face.</span><span class="sxs-lookup"><span data-stu-id="a9d98-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="a9d98-140">Cada face indica se uma borda é falsa ou não.</span><span class="sxs-lookup"><span data-stu-id="a9d98-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="a9d98-141">Uma borda diferente de falsa é indicada por-1, uma borda falsa é indicada por qualquer outro valor.</span><span class="sxs-lookup"><span data-stu-id="a9d98-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="a9d98-142">Isso permite a parametrização de uma malha de quatro processadores em que as bordas no meio do meio de cada Quad não serão recortadas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-143">*pfIMTArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-144">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d98-145">Um ponteiro para uma matriz de tempos de métricas integrados que descreve como alongar um triângulo (consulte [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="a9d98-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-146">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-147">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="a9d98-148">Um ponteiro para uma função de retorno de chamada (consulte [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que é útil para monitorar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a9d98-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-149">*fCallbackFrequency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-150">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-151">Especifique com que frequência o D3DX chamará o retorno de chamada; um valor padrão razoável é 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="a9d98-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-152">*pUserContent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-153">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-154">Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a9d98-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-155">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d98-157">Especifique a qualidade dos gráficos gerados.</span><span class="sxs-lookup"><span data-stu-id="a9d98-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="a9d98-158">Consulte [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="a9d98-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-159">*ppMeshOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-160">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a9d98-161">Ponteiro para a malha criada com o Atlas (consulte [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="a9d98-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-162">*ppFacePartitioning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-163">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a9d98-164">Um ponteiro para uma matriz dos dados de particionamento de face final.</span><span class="sxs-lookup"><span data-stu-id="a9d98-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="a9d98-165">Cada elemento contém um DWORD por face (consulte [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="a9d98-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-166">*ppVertexRemapArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-167">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a9d98-168">Um ponteiro para uma matriz de vértices remapeados.</span><span class="sxs-lookup"><span data-stu-id="a9d98-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="a9d98-169">Cada elemento da matriz identifica o vértice original do qual cada vértice final veio (se o vértice foi dividido durante o remapeamento).</span><span class="sxs-lookup"><span data-stu-id="a9d98-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="a9d98-170">Cada elemento de matriz contém um DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="a9d98-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-171">*pfMaxStretchOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-172">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d98-173">Um ponteiro para o valor máximo de Stretch gerado pelo algoritmo do Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="a9d98-174">O intervalo está entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a9d98-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="a9d98-175">*pdwNumChartsOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a9d98-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d98-176">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d98-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d98-177">Um ponteiro para o número de gráficos criados pelo algoritmo do Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="a9d98-178">Se dwMaxChartNumber for muito baixo, esse parâmetro retornará o número mínimo de gráficos necessários para criar um Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9d98-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d98-179">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9d98-179">Return value</span></span>

<span data-ttu-id="a9d98-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9d98-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9d98-181">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a9d98-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d98-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9d98-182">Remarks</span></span>

<span data-ttu-id="a9d98-183">D3DXUVAtlasCreate pode particionar a geometria de malha de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="a9d98-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="a9d98-184">Com base no número de gráficos</span><span class="sxs-lookup"><span data-stu-id="a9d98-184">Based on the number of charts</span></span>
-   <span data-ttu-id="a9d98-185">Com base na ampliação máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="a9d98-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="a9d98-186">Se a ampliação máxima permitida for 0, cada triângulo provavelmente estará em seu próprio gráfico.</span><span class="sxs-lookup"><span data-stu-id="a9d98-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d98-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9d98-187">Requirements</span></span>



| <span data-ttu-id="a9d98-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d98-188">Requirement</span></span> | <span data-ttu-id="a9d98-189">Valor</span><span class="sxs-lookup"><span data-stu-id="a9d98-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d98-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9d98-190">Header</span></span><br/>  | <dl> <span data-ttu-id="a9d98-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d98-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a9d98-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9d98-192">Library</span></span><br/> | <dl> <span data-ttu-id="a9d98-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9d98-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9d98-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9d98-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d98-195">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="a9d98-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="a9d98-196">[Ferramenta de Command-Line do Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="a9d98-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
