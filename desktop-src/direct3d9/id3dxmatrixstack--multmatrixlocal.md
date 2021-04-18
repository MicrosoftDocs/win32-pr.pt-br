---
description: Determina o produto da matriz e da matriz atual.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'Método ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791637"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="45513-103">Método ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="45513-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="45513-104">Determina o produto da matriz e da matriz atual.</span><span class="sxs-lookup"><span data-stu-id="45513-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="45513-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45513-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="45513-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45513-107">*pMat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45513-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45513-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="45513-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="45513-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) a ser multiplicado com a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="45513-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45513-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45513-110">Return value</span></span>

<span data-ttu-id="45513-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45513-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45513-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45513-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="45513-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="45513-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="45513-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45513-114">Remarks</span></span>

<span data-ttu-id="45513-115">Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem local do objeto).</span><span class="sxs-lookup"><span data-stu-id="45513-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="45513-116">Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz especificada e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="45513-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="45513-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45513-117">Requirements</span></span>



| <span data-ttu-id="45513-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="45513-118">Requirement</span></span> | <span data-ttu-id="45513-119">Valor</span><span class="sxs-lookup"><span data-stu-id="45513-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45513-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45513-120">Header</span></span><br/>  | <dl> <span data-ttu-id="45513-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="45513-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="45513-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45513-122">Library</span></span><br/> | <dl> <span data-ttu-id="45513-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45513-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45513-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="45513-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45513-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="45513-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="45513-126">**ID3DXMATRIXStack::MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="45513-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




