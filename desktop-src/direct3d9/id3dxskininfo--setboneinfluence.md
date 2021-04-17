---
description: Define o valor de influência para um Bone.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'Método ID3DXSkinInfo:: SetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780418"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="1e346-103">Método ID3DXSkinInfo:: SetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="1e346-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="1e346-104">Define o valor de influência para um Bone.</span><span class="sxs-lookup"><span data-stu-id="1e346-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e346-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e346-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="1e346-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e346-107">*Bone* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e346-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e346-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e346-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e346-109">Número do Bone.</span><span class="sxs-lookup"><span data-stu-id="1e346-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="1e346-110">*numInfluences* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e346-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e346-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e346-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e346-112">Número de influências.</span><span class="sxs-lookup"><span data-stu-id="1e346-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="1e346-113">*vértices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e346-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e346-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e346-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e346-115">A matriz de vértices influenciada por um Bone.</span><span class="sxs-lookup"><span data-stu-id="1e346-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="1e346-116">*pesos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e346-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e346-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e346-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e346-118">A matriz de pesos influenciada por um Bone.</span><span class="sxs-lookup"><span data-stu-id="1e346-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e346-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e346-119">Return value</span></span>

<span data-ttu-id="1e346-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e346-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e346-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e346-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e346-122">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1e346-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e346-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e346-123">Requirements</span></span>



| <span data-ttu-id="1e346-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e346-124">Requirement</span></span> | <span data-ttu-id="1e346-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1e346-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e346-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e346-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1e346-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e346-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1e346-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e346-128">Library</span></span><br/> | <dl> <span data-ttu-id="1e346-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e346-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e346-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e346-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e346-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="1e346-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="1e346-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="1e346-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="1e346-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="1e346-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
