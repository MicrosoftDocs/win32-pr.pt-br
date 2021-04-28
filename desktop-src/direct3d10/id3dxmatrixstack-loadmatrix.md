---
description: 'Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h) – carrega a matriz determinada na matriz atual.'
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107954"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="81380-103">Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="81380-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="81380-104">Carrega a matriz determinada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="81380-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="81380-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81380-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="81380-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81380-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81380-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81380-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81380-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81380-109">Ponteiro para a estrutura D3DXMATRIX carregada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="81380-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81380-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="81380-110">Return value</span></span>

<span data-ttu-id="81380-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81380-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81380-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81380-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81380-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="81380-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="81380-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81380-114">Remarks</span></span>

<span data-ttu-id="81380-115">Observe que esse método não adiciona um item à pilha; em vez disso, ele substitui a matriz atual pela matriz fornecida.</span><span class="sxs-lookup"><span data-stu-id="81380-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="81380-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81380-116">Requirements</span></span>



| <span data-ttu-id="81380-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81380-117">Requirement</span></span> | <span data-ttu-id="81380-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81380-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81380-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81380-119">Header</span></span><br/>  | <dl> <span data-ttu-id="81380-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="81380-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="81380-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81380-121">Library</span></span><br/> | <dl> <span data-ttu-id="81380-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81380-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81380-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81380-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81380-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="81380-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="81380-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="81380-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
