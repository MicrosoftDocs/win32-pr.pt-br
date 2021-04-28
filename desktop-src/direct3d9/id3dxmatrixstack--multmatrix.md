---
description: 'Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h) – determina o produto da matriz atual e a matriz especificada.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7361223e8fbcbae0f81641718b216c5903ff6319
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093524"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="35ab2-103">Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="35ab2-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="35ab2-104">Determina o produto da matriz atual e a matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="35ab2-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ab2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ab2-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="35ab2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35ab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ab2-107">*pMat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35ab2-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ab2-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="35ab2-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="35ab2-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) a ser multiplicado com a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="35ab2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ab2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="35ab2-110">Return value</span></span>

<span data-ttu-id="35ab2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35ab2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35ab2-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35ab2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="35ab2-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="35ab2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ab2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="35ab2-114">Remarks</span></span>

<span data-ttu-id="35ab2-115">Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem do mundo atual).</span><span class="sxs-lookup"><span data-stu-id="35ab2-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="35ab2-116">Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz atual e pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="35ab2-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ab2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ab2-117">Requirements</span></span>



| <span data-ttu-id="35ab2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ab2-118">Requirement</span></span> | <span data-ttu-id="35ab2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="35ab2-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ab2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35ab2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="35ab2-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ab2-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="35ab2-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35ab2-122">Library</span></span><br/> | <dl> <span data-ttu-id="35ab2-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35ab2-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35ab2-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="35ab2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ab2-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="35ab2-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="35ab2-126">**ID3DXMATRIXStack::MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="35ab2-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




