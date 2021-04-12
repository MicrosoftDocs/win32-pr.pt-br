---
description: Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Método ID3DX10SkinInfo:: GetBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173196"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="38563-103">Método ID3DX10SkinInfo:: GetBoneInfluences</span><span class="sxs-lookup"><span data-stu-id="38563-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="38563-104">Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="38563-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="38563-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38563-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="38563-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38563-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38563-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38563-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38563-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38563-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="38563-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="38563-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="38563-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="38563-111">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38563-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38563-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38563-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38563-113">Um deslocamento da parte superior da lista de vértices influenciados do Bone.</span><span class="sxs-lookup"><span data-stu-id="38563-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="38563-114">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span><span class="sxs-lookup"><span data-stu-id="38563-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="38563-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="38563-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38563-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38563-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38563-117">O número de índices e pesos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="38563-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="38563-118">Deve estar entre 0 e o valor retornado por ID3DX10SkinInfo:: GetBoneInfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="38563-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="38563-119">*pDestIndices* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="38563-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38563-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38563-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38563-121">Uma lista de índices no buffer de vértice, cada um representando um vértice influenciado pelo Bone.</span><span class="sxs-lookup"><span data-stu-id="38563-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="38563-122">Esses valores correspondem aos valores em pDestWeights, de modo que pDestIndices \[ \] corresponde a pDestWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="38563-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="38563-123">*pDestWeights* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="38563-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38563-124">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="38563-124">Type: **float\***</span></span>

<span data-ttu-id="38563-125">Uma lista da quantidade de influência que o Bone tem em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="38563-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="38563-126">Esses valores correspondem aos valores em pDestIndices, de modo que pDestWeights \[ \] corresponde a pDestIndices \[ i \] . f</span><span class="sxs-lookup"><span data-stu-id="38563-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38563-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38563-127">Return value</span></span>

<span data-ttu-id="38563-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38563-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38563-129">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38563-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="38563-130">Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG ou \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="38563-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="38563-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38563-131">Requirements</span></span>



| <span data-ttu-id="38563-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="38563-132">Requirement</span></span> | <span data-ttu-id="38563-133">Valor</span><span class="sxs-lookup"><span data-stu-id="38563-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38563-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38563-134">Header</span></span><br/>  | <dl> <span data-ttu-id="38563-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="38563-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="38563-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38563-136">Library</span></span><br/> | <dl> <span data-ttu-id="38563-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38563-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38563-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="38563-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38563-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="38563-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="38563-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="38563-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
