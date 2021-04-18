---
description: Define um valor de influência de um Bone em um único vértice.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'Método ID3DXSkinInfo:: SetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760653"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="45f5d-103">Método ID3DXSkinInfo:: SetBoneVertexInfluence</span><span class="sxs-lookup"><span data-stu-id="45f5d-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="45f5d-104">Define um valor de influência de um Bone em um único vértice.</span><span class="sxs-lookup"><span data-stu-id="45f5d-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45f5d-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="45f5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45f5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f5d-107">*boneNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45f5d-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45f5d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45f5d-109">Índice do Bone.</span><span class="sxs-lookup"><span data-stu-id="45f5d-109">Index of the bone.</span></span> <span data-ttu-id="45f5d-110">Deve estar entre 0 e o número de Bones.</span><span class="sxs-lookup"><span data-stu-id="45f5d-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="45f5d-111">*influenceNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45f5d-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5d-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45f5d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45f5d-113">Índice da matriz de influência do Bone especificado.</span><span class="sxs-lookup"><span data-stu-id="45f5d-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="45f5d-114">*peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45f5d-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f5d-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45f5d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45f5d-116">Fator de mistura da influência do Bone especificado.</span><span class="sxs-lookup"><span data-stu-id="45f5d-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f5d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45f5d-117">Return value</span></span>

<span data-ttu-id="45f5d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45f5d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45f5d-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45f5d-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="45f5d-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="45f5d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f5d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f5d-121">Requirements</span></span>



| <span data-ttu-id="45f5d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f5d-122">Requirement</span></span> | <span data-ttu-id="45f5d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="45f5d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45f5d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45f5d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="45f5d-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f5d-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="45f5d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45f5d-126">Library</span></span><br/> | <dl> <span data-ttu-id="45f5d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45f5d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45f5d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45f5d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f5d-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="45f5d-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="45f5d-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="45f5d-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="45f5d-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="45f5d-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="45f5d-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="45f5d-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
