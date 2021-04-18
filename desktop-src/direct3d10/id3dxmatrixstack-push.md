---
description: Adiciona uma matriz à pilha.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: 'ID3DXMATRIXStack: método USH de:P (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 694bb8b02f340be14f38b7d2a44ec2038d175098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793355"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="d9162-103">ID3DXMATRIXStack: método USH de:P (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d9162-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="d9162-104">Adiciona uma matriz à pilha.</span><span class="sxs-lookup"><span data-stu-id="d9162-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9162-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9162-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="d9162-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9162-106">Parameters</span></span>

<span data-ttu-id="d9162-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d9162-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9162-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9162-108">Return value</span></span>

<span data-ttu-id="d9162-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9162-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9162-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9162-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9162-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d9162-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9162-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9162-112">Remarks</span></span>

<span data-ttu-id="d9162-113">Esse método incrementa a contagem de itens na pilha em 1, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="d9162-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="d9162-114">A pilha aumentará dinamicamente à medida que mais itens forem adicionados.</span><span class="sxs-lookup"><span data-stu-id="d9162-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9162-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9162-115">Requirements</span></span>



| <span data-ttu-id="d9162-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9162-116">Requirement</span></span> | <span data-ttu-id="d9162-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d9162-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9162-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9162-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d9162-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9162-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9162-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9162-120">Library</span></span><br/> | <dl> <span data-ttu-id="d9162-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9162-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9162-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9162-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9162-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d9162-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d9162-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d9162-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




