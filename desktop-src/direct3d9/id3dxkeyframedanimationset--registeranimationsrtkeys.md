---
description: Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Método ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788750"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="1f59b-103">Método ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys</span><span class="sxs-lookup"><span data-stu-id="1f59b-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="1f59b-104">Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.</span><span class="sxs-lookup"><span data-stu-id="1f59b-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f59b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f59b-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1f59b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f59b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f59b-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f59b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f59b-109">Ponteiro para o nome da animação.</span><span class="sxs-lookup"><span data-stu-id="1f59b-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-110">*NumScaleKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f59b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f59b-112">Número de chaves de escala.</span><span class="sxs-lookup"><span data-stu-id="1f59b-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-113">*NumRotationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f59b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f59b-115">Número de chaves de rotação.</span><span class="sxs-lookup"><span data-stu-id="1f59b-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-116">*NumTranslationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f59b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f59b-118">Número de chaves de tradução.</span><span class="sxs-lookup"><span data-stu-id="1f59b-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-119">*pScaleKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-120">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f59b-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="1f59b-121">Endereço de um ponteiro para uma matriz alocada pelo usuário de vetores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método preenche com dados de escala.</span><span class="sxs-lookup"><span data-stu-id="1f59b-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-122">*pRotationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-123">Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f59b-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="1f59b-124">Endereço de um ponteiro para uma matriz alocada pelo usuário de quaternions [**D3DXKEY do \_ Quaternion**](d3dxkey-quaternion.md) que o método preenche com dados de rotação.</span><span class="sxs-lookup"><span data-stu-id="1f59b-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-125">*pTranslationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-126">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f59b-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="1f59b-127">Endereço de um ponteiro para uma matriz alocada pelo usuário de vetores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método preenche com dados de tradução.</span><span class="sxs-lookup"><span data-stu-id="1f59b-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="1f59b-128">*pAnimationIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f59b-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f59b-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f59b-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1f59b-130">Retorna o índice de animação.</span><span class="sxs-lookup"><span data-stu-id="1f59b-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f59b-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f59b-131">Return value</span></span>

<span data-ttu-id="1f59b-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f59b-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f59b-133">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f59b-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1f59b-134">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="1f59b-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="1f59b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f59b-135">Requirements</span></span>



| <span data-ttu-id="1f59b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f59b-136">Requirement</span></span> | <span data-ttu-id="1f59b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1f59b-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f59b-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f59b-138">Header</span></span><br/>  | <dl> <span data-ttu-id="1f59b-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f59b-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1f59b-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f59b-140">Library</span></span><br/> | <dl> <span data-ttu-id="1f59b-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f59b-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f59b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f59b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f59b-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1f59b-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="1f59b-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="1f59b-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="1f59b-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="1f59b-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="1f59b-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="1f59b-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
