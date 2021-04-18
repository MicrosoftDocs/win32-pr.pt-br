---
description: Obtém o tempo de animação global.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'Método ID3DXAnimationController:: getTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771640"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="563d0-103">Método ID3DXAnimationController:: getTime</span><span class="sxs-lookup"><span data-stu-id="563d0-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="563d0-104">Obtém o tempo de animação global.</span><span class="sxs-lookup"><span data-stu-id="563d0-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="563d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="563d0-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="563d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="563d0-106">Parameters</span></span>

<span data-ttu-id="563d0-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="563d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="563d0-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="563d0-108">Return value</span></span>

<span data-ttu-id="563d0-109">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="563d0-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="563d0-110">Retorna o tempo de animação global.</span><span class="sxs-lookup"><span data-stu-id="563d0-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="563d0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="563d0-111">Remarks</span></span>

<span data-ttu-id="563d0-112">As animações são projetadas usando um tempo de animação local e misturadas em tempo global com o [**adiantamento**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="563d0-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="563d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="563d0-113">Requirements</span></span>



| <span data-ttu-id="563d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="563d0-114">Requirement</span></span> | <span data-ttu-id="563d0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="563d0-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="563d0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="563d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="563d0-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="563d0-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="563d0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="563d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="563d0-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="563d0-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="563d0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="563d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563d0-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="563d0-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
