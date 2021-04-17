---
description: Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Método ID3DX10SkinInfo:: GetBoneInfluence (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798500"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a><span data-ttu-id="43f38-103">Método ID3DX10SkinInfo:: GetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="43f38-103">ID3DX10SkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="43f38-104">Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.</span><span class="sxs-lookup"><span data-stu-id="43f38-104">Get the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43f38-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a><span data-ttu-id="43f38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f38-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43f38-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f38-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f38-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f38-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="43f38-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="43f38-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="43f38-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f38-111">*InfluenceIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43f38-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f38-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f38-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f38-113">Um índice na lista de vértices do Bone que ele influencia.</span><span class="sxs-lookup"><span data-stu-id="43f38-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="43f38-114">*pWeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43f38-114">*pWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f38-115">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="43f38-115">Type: **float\***</span></span>

<span data-ttu-id="43f38-116">A quantidade de influência, entre 0 e 1, que o Bone tem sobre o vértice.</span><span class="sxs-lookup"><span data-stu-id="43f38-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f38-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43f38-117">Return value</span></span>

<span data-ttu-id="43f38-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43f38-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43f38-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43f38-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43f38-120">Se o método falhar, o valor de retorno poderá ser E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="43f38-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f38-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="43f38-121">Remarks</span></span>

<span data-ttu-id="43f38-122">Use ID3DX10SkinInfo:: GetBoneInfluenceCount para descobrir quantos vértices o Bone influencia.</span><span class="sxs-lookup"><span data-stu-id="43f38-122">Use ID3DX10SkinInfo::GetBoneInfluenceCount to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f38-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43f38-123">Requirements</span></span>



| <span data-ttu-id="43f38-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f38-124">Requirement</span></span> | <span data-ttu-id="43f38-125">Valor</span><span class="sxs-lookup"><span data-stu-id="43f38-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43f38-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43f38-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43f38-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f38-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="43f38-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43f38-128">Library</span></span><br/> | <dl> <span data-ttu-id="43f38-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43f38-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f38-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="43f38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f38-131">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="43f38-131">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="43f38-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="43f38-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
