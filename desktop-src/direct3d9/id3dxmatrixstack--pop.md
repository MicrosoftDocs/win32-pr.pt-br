---
description: Remove a matriz atual da parte superior da pilha.
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
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012080"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="1fef6-103">ID3DXMATRIXStack: método op de:P (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1fef6-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="1fef6-104">Remove a matriz atual da parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="1fef6-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fef6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fef6-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="1fef6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fef6-106">Parameters</span></span>

<span data-ttu-id="1fef6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1fef6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fef6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fef6-108">Return value</span></span>

<span data-ttu-id="1fef6-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fef6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fef6-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fef6-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fef6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fef6-111">Remarks</span></span>

<span data-ttu-id="1fef6-112">Observe que esse método diminui a contagem de itens na pilha em 1, removendo efetivamente a matriz atual da parte superior da pilha e promovendo uma matriz para a parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="1fef6-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="1fef6-113">Se a contagem atual de itens na pilha for 0, esse método retornará sem executar nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="1fef6-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="1fef6-114">Se a contagem atual de itens na pilha for 1, esse método esvazia a pilha.</span><span class="sxs-lookup"><span data-stu-id="1fef6-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fef6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fef6-115">Requirements</span></span>



| <span data-ttu-id="1fef6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fef6-116">Requirement</span></span> | <span data-ttu-id="1fef6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1fef6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fef6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fef6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1fef6-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fef6-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1fef6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fef6-120">Library</span></span><br/> | <dl> <span data-ttu-id="1fef6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fef6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fef6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fef6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fef6-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="1fef6-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="1fef6-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="1fef6-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="1fef6-125">**ID3DXMATRIXStack::P USH**</span><span class="sxs-lookup"><span data-stu-id="1fef6-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




