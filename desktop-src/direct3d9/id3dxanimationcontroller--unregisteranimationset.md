---
description: Remove um conjunto de animações do controlador de animação.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'Método ID3DXAnimationController:: UnregisterAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813539"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="0e871-103">Método ID3DXAnimationController:: UnregisterAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0e871-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="0e871-104">Remove um conjunto de animações do controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="0e871-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e871-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e871-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="0e871-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e871-107">*pAnimSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e871-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e871-108">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="0e871-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="0e871-109">Ponteiro para a animação [**ID3DXAnimationSet**](id3dxanimationset.md) definida como remover.</span><span class="sxs-lookup"><span data-stu-id="0e871-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e871-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e871-110">Return value</span></span>

<span data-ttu-id="0e871-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e871-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e871-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e871-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0e871-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="0e871-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e871-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e871-114">Requirements</span></span>



| <span data-ttu-id="0e871-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e871-115">Requirement</span></span> | <span data-ttu-id="0e871-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0e871-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e871-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e871-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0e871-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e871-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0e871-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e871-119">Library</span></span><br/> | <dl> <span data-ttu-id="0e871-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e871-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e871-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e871-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e871-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0e871-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




