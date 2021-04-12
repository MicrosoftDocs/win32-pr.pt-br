---
description: Recupera o fator de mistura e o vértice afetados por uma influência de Bone especificada.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'Método ID3DXSkinInfo:: GetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298464"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="49ada-103">Método ID3DXSkinInfo:: GetBoneVertexInfluence</span><span class="sxs-lookup"><span data-stu-id="49ada-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="49ada-104">Recupera o fator de mistura e o vértice afetados por uma influência de Bone especificada.</span><span class="sxs-lookup"><span data-stu-id="49ada-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ada-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49ada-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="49ada-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49ada-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ada-107">*boneNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49ada-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ada-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49ada-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49ada-109">Índice do Bone.</span><span class="sxs-lookup"><span data-stu-id="49ada-109">Index of the bone.</span></span> <span data-ttu-id="49ada-110">Deve estar entre 0 e o número de Bones.</span><span class="sxs-lookup"><span data-stu-id="49ada-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="49ada-111">*influenceNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49ada-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ada-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49ada-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49ada-113">Índice da matriz de influência do Bone especificado.</span><span class="sxs-lookup"><span data-stu-id="49ada-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="49ada-114">*pWeight* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="49ada-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49ada-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49ada-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49ada-116">Ponteiro para o fator de mistura influenciado por influenceNum.</span><span class="sxs-lookup"><span data-stu-id="49ada-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="49ada-117">*pVertexNum* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="49ada-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49ada-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49ada-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49ada-119">Ponteiro para o vértice influenciado por influenceNum.</span><span class="sxs-lookup"><span data-stu-id="49ada-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ada-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49ada-120">Return value</span></span>

<span data-ttu-id="49ada-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49ada-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49ada-122">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49ada-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49ada-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="49ada-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ada-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ada-124">Requirements</span></span>



| <span data-ttu-id="49ada-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ada-125">Requirement</span></span> | <span data-ttu-id="49ada-126">Valor</span><span class="sxs-lookup"><span data-stu-id="49ada-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49ada-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49ada-127">Header</span></span><br/>  | <dl> <span data-ttu-id="49ada-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ada-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49ada-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49ada-129">Library</span></span><br/> | <dl> <span data-ttu-id="49ada-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49ada-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49ada-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="49ada-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ada-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="49ada-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="49ada-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="49ada-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="49ada-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="49ada-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="49ada-135">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="49ada-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
