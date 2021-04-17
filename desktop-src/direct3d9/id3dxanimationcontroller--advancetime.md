---
description: Anima a malha e avança o tempo de animação global por um valor especificado.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'Método ID3DXAnimationController:: AdvanceTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763270"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="f98af-103">Método ID3DXAnimationController:: AdvanceTime</span><span class="sxs-lookup"><span data-stu-id="f98af-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="f98af-104">Anima a malha e avança o tempo de animação global por um valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f98af-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f98af-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="f98af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f98af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98af-107">*Timedelta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f98af-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98af-108">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f98af-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f98af-109">Valor, em segundos, pelo qual avançar o tempo de animação global.</span><span class="sxs-lookup"><span data-stu-id="f98af-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="f98af-110">O valor timedelta deve ser não negativo ou zero.</span><span class="sxs-lookup"><span data-stu-id="f98af-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="f98af-111">*pCallbackHandler* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f98af-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98af-112">Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="f98af-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="f98af-113">Ponteiro para uma interface de manipulador de retorno de chamada de animação definida pelo usuário, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98af-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f98af-114">Return value</span></span>

<span data-ttu-id="f98af-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f98af-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f98af-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f98af-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f98af-117">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f98af-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f98af-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f98af-118">Requirements</span></span>



| <span data-ttu-id="f98af-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98af-119">Requirement</span></span> | <span data-ttu-id="f98af-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f98af-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98af-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f98af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f98af-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98af-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f98af-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f98af-123">Library</span></span><br/> | <dl> <span data-ttu-id="f98af-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f98af-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f98af-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f98af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98af-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f98af-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
