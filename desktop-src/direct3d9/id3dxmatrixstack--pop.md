---
description: 'ID3DXMATRIXStack: método op de:P (D3dx9math. h) – remove a matriz atual da parte superior da pilha.'
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: 'ID3DXMATRIXStack: método op de:P (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093494"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="b5659-103">ID3DXMATRIXStack: método op de:P (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b5659-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="b5659-104">Remove a matriz atual da parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="b5659-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5659-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5659-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="b5659-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5659-106">Parameters</span></span>

<span data-ttu-id="b5659-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b5659-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5659-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b5659-108">Return value</span></span>

<span data-ttu-id="b5659-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5659-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5659-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5659-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5659-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5659-111">Remarks</span></span>

<span data-ttu-id="b5659-112">Observe que esse método diminui a contagem de itens na pilha em 1, removendo efetivamente a matriz atual da parte superior da pilha e promovendo uma matriz para a parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="b5659-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="b5659-113">Se a contagem atual de itens na pilha for 0, esse método retornará sem executar nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="b5659-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="b5659-114">Se a contagem atual de itens na pilha for 1, esse método esvazia a pilha.</span><span class="sxs-lookup"><span data-stu-id="b5659-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5659-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5659-115">Requirements</span></span>



| <span data-ttu-id="b5659-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5659-116">Requirement</span></span> | <span data-ttu-id="b5659-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b5659-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5659-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5659-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5659-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5659-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5659-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5659-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5659-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5659-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5659-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b5659-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5659-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="b5659-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b5659-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="b5659-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="b5659-125">**ID3DXMATRIXStack::P USH**</span><span class="sxs-lookup"><span data-stu-id="b5659-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




