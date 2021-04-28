---
description: 'Método ID3DXMATRIXStack:: GetTop (D3DX10. h) – recupera a matriz atual na parte superior da pilha.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Método ID3DXMATRIXStack:: GetTop (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108034"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="d38dc-103">Método ID3DXMATRIXStack:: GetTop (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d38dc-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="d38dc-104">Recupera a matriz atual na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="d38dc-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d38dc-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="d38dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d38dc-106">Parameters</span></span>

<span data-ttu-id="d38dc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d38dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d38dc-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d38dc-108">Return value</span></span>

<span data-ttu-id="d38dc-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d38dc-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d38dc-110">Esse método retorna um ponteiro para uma estrutura D3DXMATRIX que representa a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="d38dc-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38dc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d38dc-111">Remarks</span></span>

<span data-ttu-id="d38dc-112">Não há garantia de que o ponteiro D3DXMATRIX retornado por esse método seja válido após operações de pilha subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d38dc-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="d38dc-113">Observe que esse método não remove a matriz atual da parte superior da pilha; em vez disso, ele apenas retorna a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="d38dc-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38dc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d38dc-114">Requirements</span></span>



| <span data-ttu-id="d38dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38dc-115">Requirement</span></span> | <span data-ttu-id="d38dc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d38dc-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d38dc-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d38dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d38dc-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38dc-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d38dc-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d38dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="d38dc-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d38dc-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38dc-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d38dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38dc-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d38dc-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d38dc-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d38dc-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
