---
description: Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone. A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Método ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768210"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="8cc63-104">Método ID3DXSkinInfo:: ConvertToIndexedBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="8cc63-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="8cc63-105">Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="8cc63-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="8cc63-106">A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.</span><span class="sxs-lookup"><span data-stu-id="8cc63-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc63-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cc63-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8cc63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cc63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc63-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8cc63-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8cc63-111">A malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="8cc63-111">The input mesh.</span></span> <span data-ttu-id="8cc63-112">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="8cc63-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-113">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cc63-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cc63-115">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="8cc63-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-116">*paletteSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cc63-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cc63-118">Número de matrizes Bone disponíveis para a aparência da paleta de matriz.</span><span class="sxs-lookup"><span data-stu-id="8cc63-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-119">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8cc63-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cc63-121">Informações de adjacência da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="8cc63-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-122">*pAdjacencyOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-123">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cc63-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cc63-124">Informações de adjacência de malha de saída.</span><span class="sxs-lookup"><span data-stu-id="8cc63-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-125">*pFaceRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cc63-127">Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha mesclada.</span><span class="sxs-lookup"><span data-stu-id="8cc63-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="8cc63-128">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="8cc63-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-129">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8cc63-131">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="8cc63-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="8cc63-132">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="8cc63-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="8cc63-133">Esse parâmetro é opcional; **NULL** pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="8cc63-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-134">*pMaxVertexInfl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cc63-136">Ponteiro para um DWORD que conterá o número máximo de influências Bone necessárias por vértice para esse método de aparência.</span><span class="sxs-lookup"><span data-stu-id="8cc63-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-137">*pNumBoneCombinations* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cc63-139">Ponteiro para o número de Bones na tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="8cc63-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-140">*ppBoneCombinationTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8cc63-142">Ponteiro para a tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="8cc63-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="8cc63-143">Os dados são organizados em uma estrutura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc63-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8cc63-144">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc63-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc63-145">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc63-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8cc63-146">Ponteiro para a nova malha.</span><span class="sxs-lookup"><span data-stu-id="8cc63-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc63-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cc63-147">Return value</span></span>

<span data-ttu-id="8cc63-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cc63-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cc63-149">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cc63-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cc63-150">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8cc63-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc63-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc63-151">Remarks</span></span>

<span data-ttu-id="8cc63-152">Cada elemento nas matrizes de remapeamento especifica o índice anterior para essa posição.</span><span class="sxs-lookup"><span data-stu-id="8cc63-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="8cc63-153">Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap conterá 3.</span><span class="sxs-lookup"><span data-stu-id="8cc63-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="8cc63-154">Esse método não é executado em hardware que não dá suporte à mesclagem de vértice de função fixa.</span><span class="sxs-lookup"><span data-stu-id="8cc63-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc63-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc63-155">Requirements</span></span>



| <span data-ttu-id="8cc63-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc63-156">Requirement</span></span> | <span data-ttu-id="8cc63-157">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc63-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc63-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cc63-158">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc63-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc63-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8cc63-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cc63-160">Library</span></span><br/> | <dl> <span data-ttu-id="8cc63-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cc63-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cc63-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc63-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc63-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="8cc63-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
