---
description: Carrega a matriz determinada na matriz atual.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'Método ID3DXMATRIXStack:: loadmatrix (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506463"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="db2c1-103">Método ID3DXMATRIXStack:: loadmatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="db2c1-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="db2c1-104">Carrega a matriz determinada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="db2c1-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="db2c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db2c1-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="db2c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db2c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db2c1-107">*pMat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db2c1-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db2c1-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="db2c1-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db2c1-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) carregada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="db2c1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db2c1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db2c1-110">Return value</span></span>

<span data-ttu-id="db2c1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db2c1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db2c1-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db2c1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db2c1-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db2c1-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db2c1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db2c1-114">Remarks</span></span>

<span data-ttu-id="db2c1-115">Observe que esse método não adiciona um item à pilha; em vez disso, ele substitui a matriz atual pela matriz fornecida.</span><span class="sxs-lookup"><span data-stu-id="db2c1-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2c1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db2c1-116">Requirements</span></span>



| <span data-ttu-id="db2c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db2c1-117">Requirement</span></span> | <span data-ttu-id="db2c1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db2c1-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db2c1-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db2c1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="db2c1-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="db2c1-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="db2c1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db2c1-121">Library</span></span><br/> | <dl> <span data-ttu-id="db2c1-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db2c1-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db2c1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="db2c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db2c1-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="db2c1-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="db2c1-125">**ID3DXMATRIXStack:: loadidentity**</span><span class="sxs-lookup"><span data-stu-id="db2c1-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




