---
description: 'Método ID3DXMATRIXStack:: GetTop (D3dx9math. h) – recupera a matriz atual na parte superior da pilha.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'Método ID3DXMATRIXStack:: GetTop (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093574"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="05570-103">Método ID3DXMATRIXStack:: GetTop (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="05570-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="05570-104">Recupera a matriz atual na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="05570-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="05570-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05570-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="05570-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05570-106">Parameters</span></span>

<span data-ttu-id="05570-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="05570-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05570-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="05570-108">Return value</span></span>

<span data-ttu-id="05570-109">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="05570-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="05570-110">Esse método retorna um ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que representa a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="05570-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="05570-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="05570-111">Remarks</span></span>

<span data-ttu-id="05570-112">Não há garantia de que o ponteiro [**D3DXMATRIX**](d3dxmatrix.md) retornado por esse método seja válido após operações de pilha subsequentes.</span><span class="sxs-lookup"><span data-stu-id="05570-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="05570-113">Observe que esse método não remove a matriz atual da parte superior da pilha; em vez disso, ele apenas retorna a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="05570-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="05570-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05570-114">Requirements</span></span>



| <span data-ttu-id="05570-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="05570-115">Requirement</span></span> | <span data-ttu-id="05570-116">Valor</span><span class="sxs-lookup"><span data-stu-id="05570-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05570-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05570-117">Header</span></span><br/>  | <dl> <span data-ttu-id="05570-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="05570-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="05570-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05570-119">Library</span></span><br/> | <dl> <span data-ttu-id="05570-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05570-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05570-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05570-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05570-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="05570-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="05570-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="05570-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="05570-124">**ID3DXMATRIXStack::P USH**</span><span class="sxs-lookup"><span data-stu-id="05570-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




