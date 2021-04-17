---
description: Remova os dados de animação do conjunto de animações.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'Método ID3DXKeyframedAnimationSet:: UnregisterAnimation (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791091"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="1ba65-103">Método ID3DXKeyframedAnimationSet:: UnregisterAnimation</span><span class="sxs-lookup"><span data-stu-id="1ba65-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="1ba65-104">Remova os dados de animação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="1ba65-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ba65-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="1ba65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ba65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba65-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1ba65-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba65-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba65-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ba65-109">O índice de animação.</span><span class="sxs-lookup"><span data-stu-id="1ba65-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba65-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ba65-110">Return value</span></span>

<span data-ttu-id="1ba65-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ba65-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ba65-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ba65-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1ba65-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1ba65-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba65-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba65-114">Requirements</span></span>



| <span data-ttu-id="1ba65-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba65-115">Requirement</span></span> | <span data-ttu-id="1ba65-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba65-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba65-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ba65-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1ba65-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba65-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1ba65-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ba65-119">Library</span></span><br/> | <dl> <span data-ttu-id="1ba65-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ba65-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ba65-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba65-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba65-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1ba65-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
