---
description: Recupera a matriz atual na parte superior da pilha.
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790565"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="27c54-103">Método ID3DXMATRIXStack:: GetTop (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="27c54-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="27c54-104">Recupera a matriz atual na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="27c54-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27c54-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="27c54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27c54-106">Parameters</span></span>

<span data-ttu-id="27c54-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="27c54-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27c54-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27c54-108">Return value</span></span>

<span data-ttu-id="27c54-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="27c54-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="27c54-110">Esse método retorna um ponteiro para uma estrutura D3DXMATRIX que representa a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="27c54-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c54-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="27c54-111">Remarks</span></span>

<span data-ttu-id="27c54-112">Não há garantia de que o ponteiro D3DXMATRIX retornado por esse método seja válido após operações de pilha subsequentes.</span><span class="sxs-lookup"><span data-stu-id="27c54-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="27c54-113">Observe que esse método não remove a matriz atual da parte superior da pilha; em vez disso, ele apenas retorna a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="27c54-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c54-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c54-114">Requirements</span></span>



| <span data-ttu-id="27c54-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c54-115">Requirement</span></span> | <span data-ttu-id="27c54-116">Valor</span><span class="sxs-lookup"><span data-stu-id="27c54-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27c54-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27c54-117">Header</span></span><br/>  | <dl> <span data-ttu-id="27c54-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="27c54-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27c54-119">Library</span></span><br/> | <dl> <span data-ttu-id="27c54-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c54-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="27c54-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c54-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="27c54-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="27c54-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="27c54-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
