---
description: ID3DXMATRIXStack::P método USH (D3dx9math. h) – adiciona uma matriz à pilha.
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
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093495"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="927ed-103">ID3DXMATRIXStack: método USH de:P (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="927ed-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="927ed-104">Adiciona uma matriz à pilha.</span><span class="sxs-lookup"><span data-stu-id="927ed-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="927ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="927ed-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="927ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="927ed-106">Parameters</span></span>

<span data-ttu-id="927ed-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="927ed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="927ed-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="927ed-108">Return value</span></span>

<span data-ttu-id="927ed-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="927ed-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="927ed-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="927ed-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="927ed-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="927ed-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="927ed-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="927ed-112">Remarks</span></span>

<span data-ttu-id="927ed-113">Esse método incrementa a contagem de itens na pilha em 1, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="927ed-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="927ed-114">A pilha aumentará dinamicamente à medida que mais itens forem adicionados.</span><span class="sxs-lookup"><span data-stu-id="927ed-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="927ed-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="927ed-115">Requirements</span></span>



| <span data-ttu-id="927ed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="927ed-116">Requirement</span></span> | <span data-ttu-id="927ed-117">Valor</span><span class="sxs-lookup"><span data-stu-id="927ed-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="927ed-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="927ed-118">Header</span></span><br/>  | <dl> <span data-ttu-id="927ed-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="927ed-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="927ed-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="927ed-120">Library</span></span><br/> | <dl> <span data-ttu-id="927ed-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="927ed-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="927ed-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="927ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927ed-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="927ed-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="927ed-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="927ed-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="927ed-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="927ed-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




