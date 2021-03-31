---
description: Obter informações de rotação para um quadro-chave específico no conjunto de animações.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'Método ID3DXKeyframedAnimationSet:: GetRotationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664093"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a><span data-ttu-id="5046c-103">Método ID3DXKeyframedAnimationSet:: GetRotationKey</span><span class="sxs-lookup"><span data-stu-id="5046c-103">ID3DXKeyframedAnimationSet::GetRotationKey method</span></span>

<span data-ttu-id="5046c-104">Obter informações de rotação para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="5046c-104">Get rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5046c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5046c-105">Syntax</span></span>


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="5046c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5046c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5046c-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5046c-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5046c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5046c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5046c-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="5046c-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="5046c-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5046c-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5046c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5046c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5046c-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="5046c-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="5046c-113">*pRotationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5046c-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5046c-114">Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="5046c-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="5046c-115">Ponteiro para os dados de rotação.</span><span class="sxs-lookup"><span data-stu-id="5046c-115">Pointer to the rotation data.</span></span> <span data-ttu-id="5046c-116">Consulte [**D3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md).</span><span class="sxs-lookup"><span data-stu-id="5046c-116">See [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5046c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5046c-117">Return value</span></span>

<span data-ttu-id="5046c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5046c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5046c-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5046c-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5046c-120">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5046c-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5046c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5046c-121">Requirements</span></span>



| <span data-ttu-id="5046c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5046c-122">Requirement</span></span> | <span data-ttu-id="5046c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5046c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5046c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5046c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5046c-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5046c-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5046c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5046c-126">Library</span></span><br/> | <dl> <span data-ttu-id="5046c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5046c-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5046c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5046c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5046c-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5046c-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
