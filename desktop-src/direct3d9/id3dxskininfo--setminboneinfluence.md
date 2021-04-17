---
description: Define a influência mínima do Bone. Influenciar valores menores do que isso é ignorado.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'Método ID3DXSkinInfo:: SetMinBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798163"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="87e95-104">Método ID3DXSkinInfo:: SetMinBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="87e95-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="87e95-105">Define a influência mínima do Bone.</span><span class="sxs-lookup"><span data-stu-id="87e95-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="87e95-106">Influenciar valores menores do que isso é ignorado.</span><span class="sxs-lookup"><span data-stu-id="87e95-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e95-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87e95-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="87e95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87e95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e95-109">*MinInfl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87e95-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e95-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e95-111">Valor mínimo de influência.</span><span class="sxs-lookup"><span data-stu-id="87e95-111">Minimum influence value.</span></span> <span data-ttu-id="87e95-112">Influenciar valores menores do que isso é ignorado.</span><span class="sxs-lookup"><span data-stu-id="87e95-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e95-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87e95-113">Return value</span></span>

<span data-ttu-id="87e95-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87e95-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87e95-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87e95-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="87e95-116">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="87e95-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e95-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e95-117">Requirements</span></span>



| <span data-ttu-id="87e95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e95-118">Requirement</span></span> | <span data-ttu-id="87e95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="87e95-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e95-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87e95-120">Header</span></span><br/>  | <dl> <span data-ttu-id="87e95-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e95-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="87e95-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87e95-122">Library</span></span><br/> | <dl> <span data-ttu-id="87e95-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87e95-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87e95-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="87e95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e95-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="87e95-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="87e95-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="87e95-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
