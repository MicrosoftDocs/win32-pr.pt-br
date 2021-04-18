---
description: Adiciona uma matriz à pilha.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: 'ID3DXMATRIXStack: método USH de:P (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1678ad9481a7c76fdb0e92a0c3b2de66d638de71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793834"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="f11a1-103">ID3DXMATRIXStack: método USH de:P (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f11a1-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="f11a1-104">Adiciona uma matriz à pilha.</span><span class="sxs-lookup"><span data-stu-id="f11a1-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f11a1-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="f11a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f11a1-106">Parameters</span></span>

<span data-ttu-id="f11a1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f11a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f11a1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f11a1-108">Return value</span></span>

<span data-ttu-id="f11a1-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f11a1-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f11a1-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f11a1-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f11a1-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f11a1-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f11a1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f11a1-112">Remarks</span></span>

<span data-ttu-id="f11a1-113">Esse método incrementa a contagem de itens na pilha em 1, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="f11a1-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="f11a1-114">A pilha aumentará dinamicamente à medida que mais itens forem adicionados.</span><span class="sxs-lookup"><span data-stu-id="f11a1-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="f11a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f11a1-115">Requirements</span></span>



| <span data-ttu-id="f11a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f11a1-116">Requirement</span></span> | <span data-ttu-id="f11a1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f11a1-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f11a1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f11a1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f11a1-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f11a1-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f11a1-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f11a1-120">Library</span></span><br/> | <dl> <span data-ttu-id="f11a1-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f11a1-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f11a1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f11a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11a1-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="f11a1-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f11a1-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="f11a1-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="f11a1-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="f11a1-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




