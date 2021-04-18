---
description: Usa uma malha e retorna uma nova malha com pesos de mistura por vértice e uma tabela de combinação de Bone. A tabela descreve quais Bones afetam quais subconjuntos da malha.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'Método ID3DXSkinInfo:: ConvertToBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772655"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="d24cb-104">Método ID3DXSkinInfo:: ConvertToBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="d24cb-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="d24cb-105">Usa uma malha e retorna uma nova malha com pesos de mistura por vértice e uma tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="d24cb-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="d24cb-106">A tabela descreve quais Bones afetam quais subconjuntos da malha.</span><span class="sxs-lookup"><span data-stu-id="d24cb-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d24cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d24cb-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="d24cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d24cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d24cb-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d24cb-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d24cb-111">Malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="d24cb-111">Input mesh.</span></span> <span data-ttu-id="d24cb-112">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="d24cb-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-113">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d24cb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d24cb-115">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d24cb-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-116">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d24cb-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d24cb-118">Informações de adjacência da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="d24cb-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-119">*pAdjacencyOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-120">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d24cb-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d24cb-121">Informações de adjacência de malha de saída.</span><span class="sxs-lookup"><span data-stu-id="d24cb-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-122">*pFaceRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d24cb-124">Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha mesclada.</span><span class="sxs-lookup"><span data-stu-id="d24cb-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="d24cb-125">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="d24cb-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-126">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d24cb-128">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="d24cb-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="d24cb-129">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="d24cb-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="d24cb-130">Esse parâmetro é opcional; **NULL** pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="d24cb-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-131">*pMaxVertexInfl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d24cb-133">Ponteiro para um DWORD que conterá o número máximo de influências Bone necessárias por vértice para esse método de aparência.</span><span class="sxs-lookup"><span data-stu-id="d24cb-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-134">*pNumBoneCombinations* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d24cb-136">Ponteiro para o número de Bones na tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="d24cb-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-137">*ppBoneCombinationTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d24cb-139">Ponteiro para a tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="d24cb-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="d24cb-140">Os dados são organizados em uma estrutura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="d24cb-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d24cb-141">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d24cb-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24cb-142">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d24cb-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d24cb-143">Ponteiro para a nova malha.</span><span class="sxs-lookup"><span data-stu-id="d24cb-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d24cb-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d24cb-144">Return value</span></span>

<span data-ttu-id="d24cb-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d24cb-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d24cb-146">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d24cb-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d24cb-147">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d24cb-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d24cb-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="d24cb-148">Remarks</span></span>

<span data-ttu-id="d24cb-149">Cada elemento na matriz de remapeamento especifica o índice anterior para essa posição.</span><span class="sxs-lookup"><span data-stu-id="d24cb-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="d24cb-150">Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap conterá 3.</span><span class="sxs-lookup"><span data-stu-id="d24cb-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="d24cb-151">Esse método não é executado em hardware que não dá suporte à mesclagem de vértice de função fixa.</span><span class="sxs-lookup"><span data-stu-id="d24cb-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="d24cb-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d24cb-152">Requirements</span></span>



| <span data-ttu-id="d24cb-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="d24cb-153">Requirement</span></span> | <span data-ttu-id="d24cb-154">Valor</span><span class="sxs-lookup"><span data-stu-id="d24cb-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d24cb-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d24cb-155">Header</span></span><br/>  | <dl> <span data-ttu-id="d24cb-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d24cb-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d24cb-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d24cb-157">Library</span></span><br/> | <dl> <span data-ttu-id="d24cb-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d24cb-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d24cb-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="d24cb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d24cb-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d24cb-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
