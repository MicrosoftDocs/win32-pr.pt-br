---
description: Recupera o índice da influência do Bone que afeta um único vértice.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'Método ID3DXSkinInfo:: FindBoneVertexInfluenceIndex (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761550"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="8b485-103">Método ID3DXSkinInfo:: FindBoneVertexInfluenceIndex</span><span class="sxs-lookup"><span data-stu-id="8b485-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="8b485-104">Recupera o índice da influência do Bone que afeta um único vértice.</span><span class="sxs-lookup"><span data-stu-id="8b485-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b485-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b485-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="8b485-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b485-107">*boneNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b485-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b485-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b485-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b485-109">Índice do Bone.</span><span class="sxs-lookup"><span data-stu-id="8b485-109">Index of the bone.</span></span> <span data-ttu-id="8b485-110">Deve estar entre 0 e o número de Bones.</span><span class="sxs-lookup"><span data-stu-id="8b485-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="8b485-111">*vertexNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b485-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b485-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b485-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b485-113">Índice do vértice para o qual a influência do Bone deve ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="8b485-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="8b485-114">Deve estar entre 0 e o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="8b485-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8b485-115">*pInfluenceIndex* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8b485-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b485-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b485-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8b485-117">Ponteiro para o índice da influência do Bone que afeta vertexNum.</span><span class="sxs-lookup"><span data-stu-id="8b485-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b485-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b485-118">Return value</span></span>

<span data-ttu-id="8b485-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b485-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b485-120">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b485-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8b485-121">Se o Bone especificado não influenciar o vértice fornecido, S \_ false será retornado.</span><span class="sxs-lookup"><span data-stu-id="8b485-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="8b485-122">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8b485-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b485-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b485-123">Requirements</span></span>



| <span data-ttu-id="8b485-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b485-124">Requirement</span></span> | <span data-ttu-id="8b485-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8b485-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b485-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b485-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8b485-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b485-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8b485-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b485-128">Library</span></span><br/> | <dl> <span data-ttu-id="8b485-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b485-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b485-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b485-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b485-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="8b485-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="8b485-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="8b485-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="8b485-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="8b485-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="8b485-134">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="8b485-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
