---
description: Cria uma malha de capa de outra malha.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Função D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506485"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="201f3-103">Função D3DXCreateSkinInfoFromBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="201f3-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="201f3-104">Cria uma malha de capa de outra malha.</span><span class="sxs-lookup"><span data-stu-id="201f3-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="201f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="201f3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="201f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="201f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="201f3-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="201f3-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201f3-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="201f3-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="201f3-109">Ponteiro para um objeto [**ID3DXBaseMesh**](id3dxbasemesh.md) , a malha a partir da qual criar a malha de capa.</span><span class="sxs-lookup"><span data-stu-id="201f3-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="201f3-110">*NumBones* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="201f3-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201f3-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="201f3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="201f3-112">O comprimento da matriz anexada ao Boneid.</span><span class="sxs-lookup"><span data-stu-id="201f3-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="201f3-113">Consulte [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="201f3-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="201f3-114">*pBoneCombinationTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="201f3-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201f3-115">Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="201f3-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="201f3-116">Ponteiro para uma matriz de combinações de Bone.</span><span class="sxs-lookup"><span data-stu-id="201f3-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="201f3-117">Consulte [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="201f3-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="201f3-118">*ppSkinInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="201f3-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="201f3-119">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="201f3-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="201f3-120">Endereço de um ponteiro para uma interface [**ID3DXSkinInfo**](id3dxskininfo.md) que representa o objeto de malha de capa criado.</span><span class="sxs-lookup"><span data-stu-id="201f3-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="201f3-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="201f3-121">Return value</span></span>

<span data-ttu-id="201f3-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="201f3-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="201f3-123">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="201f3-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="201f3-124">Se a função falhar, o valor de retorno poderá ser o seguinte: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="201f3-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="201f3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="201f3-125">Requirements</span></span>



| <span data-ttu-id="201f3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="201f3-126">Requirement</span></span> | <span data-ttu-id="201f3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="201f3-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="201f3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="201f3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="201f3-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="201f3-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="201f3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="201f3-130">Library</span></span><br/> | <dl> <span data-ttu-id="201f3-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="201f3-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="201f3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="201f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201f3-133">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="201f3-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
