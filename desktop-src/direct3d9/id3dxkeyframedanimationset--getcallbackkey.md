---
description: Obtém informações sobre um retorno de chamada específico no conjunto de animações.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814062"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="0b745-103">Método ID3DXKeyframedAnimationSet:: GetCallbackKey</span><span class="sxs-lookup"><span data-stu-id="0b745-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="0b745-104">Obtém informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="0b745-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b745-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b745-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="0b745-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b745-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b745-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b745-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b745-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b745-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b745-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="0b745-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="0b745-110">*pCallbackKeys* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0b745-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b745-111">Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="0b745-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="0b745-112">Ponteiro para a [**função de retorno de chamada**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="0b745-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b745-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b745-113">Return value</span></span>

<span data-ttu-id="0b745-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b745-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b745-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b745-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0b745-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b745-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b745-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b745-117">Requirements</span></span>



| <span data-ttu-id="0b745-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b745-118">Requirement</span></span> | <span data-ttu-id="0b745-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0b745-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b745-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b745-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0b745-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b745-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0b745-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b745-122">Library</span></span><br/> | <dl> <span data-ttu-id="0b745-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b745-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b745-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b745-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b745-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0b745-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
