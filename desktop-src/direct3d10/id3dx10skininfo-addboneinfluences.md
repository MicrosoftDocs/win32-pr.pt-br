---
description: Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Método ID3DX10SkinInfo:: AddBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173018"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="0633d-103">Método ID3DX10SkinInfo:: AddBoneInfluences</span><span class="sxs-lookup"><span data-stu-id="0633d-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="0633d-104">Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0633d-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="0633d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0633d-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="0633d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0633d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0633d-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0633d-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0633d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0633d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0633d-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="0633d-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="0633d-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="0633d-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="0633d-111">*InfluenceCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0633d-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0633d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0633d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0633d-113">Número de vértices a serem adicionados à influência do Bone.</span><span class="sxs-lookup"><span data-stu-id="0633d-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="0633d-114">*pIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0633d-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0633d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0633d-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0633d-116">Ponteiro para uma matriz de índices de vértice.</span><span class="sxs-lookup"><span data-stu-id="0633d-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="0633d-117">Cada membro dessa matriz tem um membro correspondente em pWeights, de modo que pIndices \[ \] corresponde a pWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="0633d-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="0633d-118">O valor correspondente em pWeights \[ eu defino o quanto \] a BoneIndex de influência terá no vértice indexado por pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="0633d-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="0633d-119">O tamanho da matriz pIndices deve ser igual ou maior que InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="0633d-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="0633d-120">*pWeights* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0633d-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0633d-121">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="0633d-121">Type: **float\***</span></span>

<span data-ttu-id="0633d-122">Ponteiro para uma matriz de pesos de Bone.</span><span class="sxs-lookup"><span data-stu-id="0633d-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="0633d-123">Cada membro dessa matriz tem um membro correspondente em pIndices, de modo que pWeights \[ \] corresponde a pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="0633d-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="0633d-124">Cada valor em pWeights está entre 0 e 1 e define a quantidade de influência que o Bone tem sobre cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0633d-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="0633d-125">O tamanho de pWeights deve ser igual ou maior que InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="0633d-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0633d-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0633d-126">Return value</span></span>

<span data-ttu-id="0633d-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0633d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0633d-128">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0633d-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0633d-129">Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG ou \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0633d-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0633d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0633d-130">Requirements</span></span>



| <span data-ttu-id="0633d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0633d-131">Requirement</span></span> | <span data-ttu-id="0633d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0633d-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0633d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0633d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0633d-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0633d-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0633d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0633d-135">Library</span></span><br/> | <dl> <span data-ttu-id="0633d-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0633d-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0633d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0633d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0633d-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="0633d-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="0633d-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0633d-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
