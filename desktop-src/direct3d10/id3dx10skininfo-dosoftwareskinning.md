---
description: Faça a subaparência do software em uma matriz de vértices.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: 'ID3DX10SkinInfo: método oSoftwareSkinning de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761199"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="5a922-103">ID3DX10SkinInfo: método oSoftwareSkinning de:D</span><span class="sxs-lookup"><span data-stu-id="5a922-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="5a922-104">Faça a subaparência do software em uma matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="5a922-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a922-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a922-105">Syntax</span></span>


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a><span data-ttu-id="5a922-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a922-107">*StartVertex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a922-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a922-109">Um índice baseado em 0 em pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="5a922-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-110">*Contagemdevértice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a922-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a922-112">Número de vértices para transformar.</span><span class="sxs-lookup"><span data-stu-id="5a922-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-113">*pSrcVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="5a922-114">Type: **void\***</span></span>

<span data-ttu-id="5a922-115">Ponteiro para uma matriz de vértices para transformar.</span><span class="sxs-lookup"><span data-stu-id="5a922-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-116">*SrcStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a922-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a922-118">O tamanho, em bytes, de um vértice em pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="5a922-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-119">*pDestVertices* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5a922-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-120">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="5a922-120">Type: **void\***</span></span>

<span data-ttu-id="5a922-121">Ponteiro para uma matriz de vértices, que será preenchida com os vértices transformados.</span><span class="sxs-lookup"><span data-stu-id="5a922-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-122">*DestStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a922-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a922-124">O tamanho, em bytes, de um vértice em pDestVertices.</span><span class="sxs-lookup"><span data-stu-id="5a922-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-125">*pBoneMatrices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-126">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a922-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5a922-127">Uma matriz de matrizes que será usada para transformar os pontos mapeados para cada Bone, de modo que os vértices mapeados para Bone \[ i serão \] transformados por pBoneMatrices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="5a922-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="5a922-128">Essa matriz será usada para transformar as matrizes somente se o valor IsNormal em pChannelDescs for definido como **false**; caso contrário, pInverseTransposeBoneMatrices será usado.</span><span class="sxs-lookup"><span data-stu-id="5a922-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-129">*pInverseTransposeBoneMatrices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-130">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a922-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5a922-131">Se esse valor for **NULL**, ele será definido como igual a pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="5a922-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="5a922-132">Essa matriz de matrizes será usada para transformar os vértices somente se o valor IsNormal em pChannelDescs for definido como **true**; caso contrário, pBoneMatrices será usado.</span><span class="sxs-lookup"><span data-stu-id="5a922-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-133">*pChannelDescs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-134">Tipo: **[ **\_ \_ canal de revestimento D3DX10**](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a922-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="5a922-135">Ponteiro para uma \_ estrutura de canal de casca de D3DX10 \_ , que determina o membro da decl Vertex que a subcapa de software será feita em.</span><span class="sxs-lookup"><span data-stu-id="5a922-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="5a922-136">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a922-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a922-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a922-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a922-138">O número de estruturas de canal de D3DX10 \_ \_ de aparência em pChannelDescs.</span><span class="sxs-lookup"><span data-stu-id="5a922-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a922-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a922-139">Return value</span></span>

<span data-ttu-id="5a922-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a922-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a922-141">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a922-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5a922-142">Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5a922-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a922-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a922-143">Remarks</span></span>

<span data-ttu-id="5a922-144">Aqui está um exemplo de como usar a dicapação de software:</span><span class="sxs-lookup"><span data-stu-id="5a922-144">Here is an example of how to use software skinning:</span></span>


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a><span data-ttu-id="5a922-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a922-145">Requirements</span></span>



| <span data-ttu-id="5a922-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a922-146">Requirement</span></span> | <span data-ttu-id="5a922-147">Valor</span><span class="sxs-lookup"><span data-stu-id="5a922-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a922-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a922-148">Header</span></span><br/>  | <dl> <span data-ttu-id="5a922-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a922-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a922-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a922-150">Library</span></span><br/> | <dl> <span data-ttu-id="5a922-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a922-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a922-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a922-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a922-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="5a922-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="5a922-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5a922-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
