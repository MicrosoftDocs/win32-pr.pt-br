---
description: Define a matriz de deslocamento do Bone.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'Método ID3DXSkinInfo:: SetBoneOffsetMatrix (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663962"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="d4ff4-103">Método ID3DXSkinInfo:: SetBoneOffsetMatrix</span><span class="sxs-lookup"><span data-stu-id="d4ff4-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="d4ff4-104">Define a matriz de deslocamento do Bone.</span><span class="sxs-lookup"><span data-stu-id="d4ff4-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ff4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4ff4-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="d4ff4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4ff4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ff4-107">*Bone* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ff4-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ff4-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ff4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ff4-109">Número do Bone.</span><span class="sxs-lookup"><span data-stu-id="d4ff4-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="d4ff4-110">*pBoneTransform* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ff4-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ff4-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4ff4-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d4ff4-112">Ponteiro para a matriz de deslocamento do Bone.</span><span class="sxs-lookup"><span data-stu-id="d4ff4-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ff4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4ff4-113">Return value</span></span>

<span data-ttu-id="d4ff4-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4ff4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4ff4-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4ff4-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d4ff4-116">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4ff4-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ff4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4ff4-117">Remarks</span></span>

<span data-ttu-id="d4ff4-118">Os nomes de Bone são retornados por [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="d4ff4-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ff4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ff4-119">Requirements</span></span>



| <span data-ttu-id="d4ff4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ff4-120">Requirement</span></span> | <span data-ttu-id="d4ff4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d4ff4-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ff4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4ff4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4ff4-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ff4-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d4ff4-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4ff4-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4ff4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4ff4-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4ff4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4ff4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ff4-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d4ff4-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="d4ff4-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="d4ff4-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
