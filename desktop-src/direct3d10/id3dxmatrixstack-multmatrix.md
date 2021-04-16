---
description: Determina o produto da matriz atual e a matriz especificada.
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'Método ID3DXMATRIXStack:: MultMatrix (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43f80ca26f615e02570f0855b1ba6c2435e11b5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765318"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="794a0-103">Método ID3DXMATRIXStack:: MultMatrix (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="794a0-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="794a0-104">Determina o produto da matriz atual e a matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="794a0-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="794a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="794a0-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="794a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="794a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794a0-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="794a0-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794a0-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="794a0-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="794a0-109">Ponteiro para a estrutura D3DXMATRIX a ser multiplicado com a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="794a0-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794a0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="794a0-110">Return value</span></span>

<span data-ttu-id="794a0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="794a0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="794a0-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="794a0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="794a0-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="794a0-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="794a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="794a0-114">Remarks</span></span>

<span data-ttu-id="794a0-115">Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem do mundo atual).</span><span class="sxs-lookup"><span data-stu-id="794a0-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="794a0-116">Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz atual e pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="794a0-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="794a0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="794a0-117">Requirements</span></span>



| <span data-ttu-id="794a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="794a0-118">Requirement</span></span> | <span data-ttu-id="794a0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="794a0-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="794a0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="794a0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="794a0-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="794a0-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="794a0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="794a0-122">Library</span></span><br/> | <dl> <span data-ttu-id="794a0-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="794a0-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="794a0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="794a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794a0-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="794a0-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="794a0-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="794a0-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
