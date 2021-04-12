---
description: Define informações sobre um retorno de chamada específico no conjunto de animações.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'Método ID3DXKeyframedAnimationSet:: SetCallbackKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49d3373e0ab0fa221e707ca6eda9ac9bb468a5a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173167"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a><span data-ttu-id="35259-103">Método ID3DXKeyframedAnimationSet:: SetCallbackKey</span><span class="sxs-lookup"><span data-stu-id="35259-103">ID3DXKeyframedAnimationSet::SetCallbackKey method</span></span>

<span data-ttu-id="35259-104">Define informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="35259-104">Sets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="35259-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35259-105">Syntax</span></span>


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="35259-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35259-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35259-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35259-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35259-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35259-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35259-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="35259-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="35259-110">*pCallbackKeys* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="35259-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35259-111">Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="35259-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="35259-112">Ponteiro para a [**função de retorno de chamada**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="35259-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35259-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35259-113">Return value</span></span>

<span data-ttu-id="35259-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35259-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35259-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35259-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="35259-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="35259-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="35259-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35259-117">Requirements</span></span>



| <span data-ttu-id="35259-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="35259-118">Requirement</span></span> | <span data-ttu-id="35259-119">Valor</span><span class="sxs-lookup"><span data-stu-id="35259-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35259-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35259-120">Header</span></span><br/>  | <dl> <span data-ttu-id="35259-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="35259-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="35259-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35259-122">Library</span></span><br/> | <dl> <span data-ttu-id="35259-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35259-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35259-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="35259-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35259-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="35259-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
