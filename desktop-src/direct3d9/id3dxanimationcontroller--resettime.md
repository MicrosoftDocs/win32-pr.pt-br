---
description: Redefine o tempo de animação global para zero. Todos os eventos pendentes manterão suas agendas originais, mas no novo período de tempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Método ID3DXAnimationController:: ResetTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664059"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="4b66f-104">Método ID3DXAnimationController:: ResetTime</span><span class="sxs-lookup"><span data-stu-id="4b66f-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="4b66f-105">Redefine o tempo de animação global para zero.</span><span class="sxs-lookup"><span data-stu-id="4b66f-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="4b66f-106">Todos os eventos pendentes manterão suas agendas originais, mas no novo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="4b66f-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b66f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b66f-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="4b66f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b66f-108">Parameters</span></span>

<span data-ttu-id="4b66f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b66f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b66f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b66f-110">Return value</span></span>

<span data-ttu-id="4b66f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b66f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b66f-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b66f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4b66f-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4b66f-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b66f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b66f-114">Remarks</span></span>

<span data-ttu-id="4b66f-115">Esse método geralmente é usado quando o valor de tempo de animação global está se aproximando da precisão máxima do armazenamento duplo, ou 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="4b66f-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b66f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b66f-116">Requirements</span></span>



| <span data-ttu-id="4b66f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b66f-117">Requirement</span></span> | <span data-ttu-id="4b66f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4b66f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b66f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b66f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4b66f-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b66f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4b66f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b66f-121">Library</span></span><br/> | <dl> <span data-ttu-id="4b66f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b66f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b66f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b66f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b66f-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4b66f-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




