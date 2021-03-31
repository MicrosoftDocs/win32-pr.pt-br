---
description: Computa Normals de unidade para cada vértice em uma malha. Fornecido para dar suporte a aplicativos herdados. Use D3DXComputeTangentFrameEx para obter resultados melhores.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Função D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930646"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="a80a0-105">Função D3DXComputeNormals</span><span class="sxs-lookup"><span data-stu-id="a80a0-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="a80a0-106">Computa Normals de unidade para cada vértice em uma malha.</span><span class="sxs-lookup"><span data-stu-id="a80a0-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="a80a0-107">Fornecido para dar suporte a aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="a80a0-107">Provided to support legacy applications.</span></span> <span data-ttu-id="a80a0-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obter resultados melhores.</span><span class="sxs-lookup"><span data-stu-id="a80a0-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80a0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a80a0-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="a80a0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a80a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80a0-111">*pMesh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a80a0-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a80a0-112">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a80a0-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="a80a0-113">Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando o objeto de malha normalizado.</span><span class="sxs-lookup"><span data-stu-id="a80a0-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="a80a0-114">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a80a0-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80a0-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a80a0-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a80a0-116">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha progressiva criada.</span><span class="sxs-lookup"><span data-stu-id="a80a0-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="a80a0-117">Esse parâmetro é opcional e deve ser definido como **nulo** se não for usado.</span><span class="sxs-lookup"><span data-stu-id="a80a0-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80a0-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a80a0-118">Return value</span></span>

<span data-ttu-id="a80a0-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a80a0-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a80a0-120">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a80a0-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a80a0-121">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a80a0-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80a0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a80a0-122">Remarks</span></span>

<span data-ttu-id="a80a0-123">A malha de entrada deve ter o sinalizador [ \_ normal D3DFVF](d3dfvf.md) especificado em seu formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="a80a0-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="a80a0-124">Um normal para um vértice é gerado pela média dos normais de todas as faces que compartilham esse vértice.</span><span class="sxs-lookup"><span data-stu-id="a80a0-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="a80a0-125">Se a adjacência for fornecida, os vértices replicados serão ignorados e "suavizados".</span><span class="sxs-lookup"><span data-stu-id="a80a0-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="a80a0-126">Se a adjacência não for fornecida, os vértices replicados terão a média normal de somente as faces que as referenciam explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a80a0-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="a80a0-127">Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="a80a0-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="a80a0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80a0-128">Requirements</span></span>



| <span data-ttu-id="a80a0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80a0-129">Requirement</span></span> | <span data-ttu-id="a80a0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a80a0-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a80a0-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a80a0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a80a0-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80a0-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a80a0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a80a0-133">Library</span></span><br/> | <dl> <span data-ttu-id="a80a0-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a80a0-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a80a0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a80a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80a0-136">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="a80a0-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
