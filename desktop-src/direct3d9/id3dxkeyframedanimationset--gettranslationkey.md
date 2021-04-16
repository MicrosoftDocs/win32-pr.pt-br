---
description: Obter informações de tradução para um quadro-chave específico no conjunto de animações.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'Método ID3DXKeyframedAnimationSet:: GetTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772633"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="8799a-103">Método ID3DXKeyframedAnimationSet:: GetTranslationKey</span><span class="sxs-lookup"><span data-stu-id="8799a-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="8799a-104">Obter informações de tradução para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="8799a-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="8799a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8799a-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="8799a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8799a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8799a-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8799a-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8799a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8799a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8799a-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="8799a-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="8799a-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8799a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8799a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8799a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8799a-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="8799a-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="8799a-113">*pTranslationKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8799a-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8799a-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="8799a-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="8799a-115">Ponteiro para as informações de rotação.</span><span class="sxs-lookup"><span data-stu-id="8799a-115">Pointer to the rotation information.</span></span> <span data-ttu-id="8799a-116">Consulte [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="8799a-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8799a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8799a-117">Return value</span></span>

<span data-ttu-id="8799a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8799a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8799a-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8799a-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8799a-120">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8799a-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8799a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8799a-121">Requirements</span></span>



| <span data-ttu-id="8799a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8799a-122">Requirement</span></span> | <span data-ttu-id="8799a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8799a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8799a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8799a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8799a-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8799a-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8799a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8799a-126">Library</span></span><br/> | <dl> <span data-ttu-id="8799a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8799a-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8799a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8799a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8799a-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="8799a-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
