---
description: Função D3DXUVAtlasPartition – criar um Atlas UV para uma malha.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Função D3DXUVAtlasPartition (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117794"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="ec31b-103">Função D3DXUVAtlasPartition</span><span class="sxs-lookup"><span data-stu-id="ec31b-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="ec31b-104">Crie um Atlas UV para uma malha.</span><span class="sxs-lookup"><span data-stu-id="ec31b-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec31b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec31b-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="ec31b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec31b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec31b-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ec31b-109">Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o Atlas.</span><span class="sxs-lookup"><span data-stu-id="ec31b-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="ec31b-110">No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="ec31b-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-111">*dwMaxChartNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-113">O número máximo de gráficos para particionar a malha.</span><span class="sxs-lookup"><span data-stu-id="ec31b-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="ec31b-114">Consulte comentários sobre os modos de particionamento.</span><span class="sxs-lookup"><span data-stu-id="ec31b-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="ec31b-115">Use 0 para informar ao D3DX que o Atlas deve ser parametrizado com base na ampliação.</span><span class="sxs-lookup"><span data-stu-id="ec31b-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-116">*fMaxStretch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-118">A quantidade de alongamento permitida.</span><span class="sxs-lookup"><span data-stu-id="ec31b-118">The amount of stretching allowed.</span></span> <span data-ttu-id="ec31b-119">0 significa que nenhum alongamento é permitido, 1 significa que qualquer quantidade de alongamento pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="ec31b-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-120">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-122">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="ec31b-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-123">*pdwAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-124">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec31b-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ec31b-125">Um ponteiro para uma matriz de dados de adjacência com 3 DWORDs por face, indicando quais triângulos são adjacentes entre si (consulte [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="ec31b-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="ec31b-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="ec31b-127">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec31b-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ec31b-128">Uma matriz com 3 DWORDs por face.</span><span class="sxs-lookup"><span data-stu-id="ec31b-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="ec31b-129">Cada face indica se uma borda é falsa ou não.</span><span class="sxs-lookup"><span data-stu-id="ec31b-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="ec31b-130">Uma borda diferente de falsa é indicada por-1, uma borda falsa é indicada por qualquer outro valor.</span><span class="sxs-lookup"><span data-stu-id="ec31b-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="ec31b-131">Isso permite a parametrização de uma malha de quatro processadores em que as bordas no meio do meio de cada Quad não serão recortadas.</span><span class="sxs-lookup"><span data-stu-id="ec31b-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-132">*pfIMTArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ec31b-134">Um ponteiro para uma matriz de tempos de métricas integrados que descreve como alongar um triângulo (consulte [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="ec31b-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-135">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="ec31b-137">Um ponteiro para uma função de retorno de chamada (consulte [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que é útil para monitorar o progresso.</span><span class="sxs-lookup"><span data-stu-id="ec31b-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-138">*fCallbackFrequency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-139">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-140">Especifique com que frequência o D3DX chamará o retorno de chamada; um valor padrão razoável é 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="ec31b-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-141">*pUserContent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-142">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-143">Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ec31b-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-144">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec31b-146">Especifique a qualidade dos gráficos gerados combinando um ou mais sinalizadores [**D3DXUVATLAS**](./d3dxuvatlas.md) .</span><span class="sxs-lookup"><span data-stu-id="ec31b-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-147">*ppMeshOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-148">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ec31b-149">Ponteiro para a malha criada com o Atlas (consulte [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="ec31b-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-150">*pFacePartitioning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="ec31b-152">Um ponteiro para uma matriz dos dados de particionamento de face final.</span><span class="sxs-lookup"><span data-stu-id="ec31b-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="ec31b-153">Cada elemento contém um DWORD por face (consulte [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="ec31b-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-154">*ppVertexRemapArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-155">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ec31b-156">Um ponteiro para uma matriz de vértices remapeados.</span><span class="sxs-lookup"><span data-stu-id="ec31b-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="ec31b-157">Cada elemento da matriz identifica o vértice original a partir do qual cada vértice final veio (se o vértice foi dividido durante o remapeamento).</span><span class="sxs-lookup"><span data-stu-id="ec31b-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="ec31b-158">Cada elemento de matriz contém um DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="ec31b-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="ec31b-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="ec31b-160">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ec31b-161">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec31b-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="ec31b-162">Esse buffer conterá uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="ec31b-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="ec31b-163">Esse parâmetro não deve ser **nulo**, pois a chamada subsequente para D3DXUVAtlasPack () exige isso.</span><span class="sxs-lookup"><span data-stu-id="ec31b-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-164">*pfMaxStretchOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-165">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ec31b-166">Um ponteiro para o valor máximo de Stretch gerado pelo algoritmo do Atlas.</span><span class="sxs-lookup"><span data-stu-id="ec31b-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="ec31b-167">O intervalo está entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="ec31b-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="ec31b-168">*pdwNumChartsOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec31b-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec31b-169">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec31b-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ec31b-170">Um ponteiro para o número de gráficos criados pelo algoritmo do Atlas.</span><span class="sxs-lookup"><span data-stu-id="ec31b-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="ec31b-171">Se dwMaxChartNumber for muito baixo, esse parâmetro retornará o número mínimo de gráficos necessários para criar um Atlas.</span><span class="sxs-lookup"><span data-stu-id="ec31b-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec31b-172">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ec31b-172">Return value</span></span>

<span data-ttu-id="ec31b-173">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec31b-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec31b-174">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ec31b-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec31b-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec31b-175">Remarks</span></span>

<span data-ttu-id="ec31b-176">D3DXUVAtlasPartition é semelhante a [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), exceto pelo fato de que o D3DXUVAtlasPartition não executa a etapa de empacotamento final.</span><span class="sxs-lookup"><span data-stu-id="ec31b-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec31b-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec31b-177">Requirements</span></span>



| <span data-ttu-id="ec31b-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec31b-178">Requirement</span></span> | <span data-ttu-id="ec31b-179">Valor</span><span class="sxs-lookup"><span data-stu-id="ec31b-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec31b-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec31b-180">Header</span></span><br/>  | <dl> <span data-ttu-id="ec31b-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec31b-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ec31b-182">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec31b-182">Library</span></span><br/> | <dl> <span data-ttu-id="ec31b-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec31b-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec31b-184">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec31b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec31b-185">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="ec31b-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="ec31b-186">[Ferramenta de Command-Line do Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ec31b-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
