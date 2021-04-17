---
description: Defina a quantidade de influência que um determinado Bone tem sobre um determinado vértice.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'Método ID3DX10SkinInfo:: SetBoneInfluence (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762467"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="579fc-103">Método ID3DX10SkinInfo:: SetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="579fc-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="579fc-104">Defina a quantidade de influência que um determinado Bone tem sobre um determinado vértice.</span><span class="sxs-lookup"><span data-stu-id="579fc-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="579fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="579fc-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="579fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="579fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579fc-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="579fc-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579fc-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="579fc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="579fc-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="579fc-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="579fc-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="579fc-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="579fc-111">*InfluenceIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="579fc-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579fc-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="579fc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="579fc-113">Um índice na lista de vértices do Bone que ele influencia.</span><span class="sxs-lookup"><span data-stu-id="579fc-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="579fc-114">*Peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="579fc-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579fc-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="579fc-115">Type: **float**</span></span>

<span data-ttu-id="579fc-116">A quantidade de influência, entre 0 e 1, que o Bone tem sobre o vértice.</span><span class="sxs-lookup"><span data-stu-id="579fc-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579fc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="579fc-117">Return value</span></span>

<span data-ttu-id="579fc-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="579fc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="579fc-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="579fc-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="579fc-120">Se o método falhar, o valor de retorno poderá ser E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="579fc-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="579fc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="579fc-121">Requirements</span></span>



| <span data-ttu-id="579fc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="579fc-122">Requirement</span></span> | <span data-ttu-id="579fc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="579fc-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="579fc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="579fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="579fc-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="579fc-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="579fc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="579fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="579fc-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="579fc-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579fc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="579fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579fc-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="579fc-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="579fc-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="579fc-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
