---
description: Remove a matriz atual da parte superior da pilha.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: 'ID3DXMATRIXStack: método op de:P (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785136"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="3c829-103">ID3DXMATRIXStack: método op de:P (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="3c829-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="3c829-104">Remove a matriz atual da parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="3c829-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c829-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c829-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="3c829-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c829-106">Parameters</span></span>

<span data-ttu-id="3c829-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3c829-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c829-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c829-108">Return value</span></span>

<span data-ttu-id="3c829-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c829-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c829-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c829-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c829-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c829-111">Remarks</span></span>

<span data-ttu-id="3c829-112">Observe que esse método diminui a contagem de itens na pilha em 1, removendo efetivamente a matriz atual da parte superior da pilha e promovendo uma matriz para a parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="3c829-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="3c829-113">Se a contagem atual de itens na pilha for 0, esse método retornará sem executar nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="3c829-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="3c829-114">Se a contagem atual de itens na pilha for 1, esse método esvazia a pilha.</span><span class="sxs-lookup"><span data-stu-id="3c829-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c829-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c829-115">Requirements</span></span>



| <span data-ttu-id="3c829-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c829-116">Requirement</span></span> | <span data-ttu-id="3c829-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3c829-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c829-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c829-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3c829-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c829-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c829-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c829-120">Library</span></span><br/> | <dl> <span data-ttu-id="3c829-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c829-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c829-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c829-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c829-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="3c829-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="3c829-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3c829-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




