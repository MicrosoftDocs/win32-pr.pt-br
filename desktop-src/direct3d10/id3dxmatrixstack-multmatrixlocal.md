---
description: 'Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h) – determina o produto da matriz e da matriz atual.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107944"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="2ef91-103">Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2ef91-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="2ef91-104">Determina o produto da matriz e da matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2ef91-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ef91-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2ef91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ef91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef91-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ef91-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef91-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ef91-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ef91-109">Ponteiro para a estrutura D3DXMATRIX a ser multiplicado com a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2ef91-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef91-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2ef91-110">Return value</span></span>

<span data-ttu-id="2ef91-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ef91-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ef91-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ef91-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ef91-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2ef91-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef91-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef91-114">Remarks</span></span>

<span data-ttu-id="2ef91-115">Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem local do objeto).</span><span class="sxs-lookup"><span data-stu-id="2ef91-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="2ef91-116">Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz especificada e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2ef91-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef91-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef91-117">Requirements</span></span>



| <span data-ttu-id="2ef91-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef91-118">Requirement</span></span> | <span data-ttu-id="2ef91-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef91-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef91-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ef91-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef91-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef91-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ef91-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ef91-122">Library</span></span><br/> | <dl> <span data-ttu-id="2ef91-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ef91-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef91-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2ef91-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef91-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2ef91-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2ef91-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2ef91-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
