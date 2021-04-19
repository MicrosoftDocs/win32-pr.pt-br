---
description: Obtém os vértices e os pesos que um Bone influencia.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'Método ID3DXSkinInfo:: GetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812316"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="b736a-103">Método ID3DXSkinInfo:: GetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="b736a-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="b736a-104">Obtém os vértices e os pesos que um Bone influencia.</span><span class="sxs-lookup"><span data-stu-id="b736a-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="b736a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b736a-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="b736a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b736a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b736a-107">*Bone* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b736a-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b736a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b736a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b736a-109">Número do Bone.</span><span class="sxs-lookup"><span data-stu-id="b736a-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="b736a-110">*vértices* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b736a-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b736a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b736a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b736a-112">Obtenha a matriz de vértices influenciada por um Bone.</span><span class="sxs-lookup"><span data-stu-id="b736a-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="b736a-113">*pesos* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b736a-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b736a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b736a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b736a-115">Obtenha a matriz de pesos influenciada por um Bone.</span><span class="sxs-lookup"><span data-stu-id="b736a-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b736a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b736a-116">Return value</span></span>

<span data-ttu-id="b736a-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b736a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b736a-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b736a-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b736a-119">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b736a-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b736a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b736a-120">Remarks</span></span>

<span data-ttu-id="b736a-121">Use [**ID3DXSkinInfo:: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) para descobrir quantos vértices o Bone influencia.</span><span class="sxs-lookup"><span data-stu-id="b736a-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="b736a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b736a-122">Requirements</span></span>



| <span data-ttu-id="b736a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b736a-123">Requirement</span></span> | <span data-ttu-id="b736a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b736a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b736a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b736a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b736a-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b736a-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b736a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b736a-127">Library</span></span><br/> | <dl> <span data-ttu-id="b736a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b736a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b736a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b736a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b736a-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b736a-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="b736a-131">**ID3DXSkinInfo::SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="b736a-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
