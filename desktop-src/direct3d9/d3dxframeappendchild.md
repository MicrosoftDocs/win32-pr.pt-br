---
description: Adiciona um quadro filho a um quadro.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Função D3DXFrameAppendChild (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173001"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="24fc9-103">Função D3DXFrameAppendChild</span><span class="sxs-lookup"><span data-stu-id="24fc9-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="24fc9-104">Adiciona um quadro filho a um quadro.</span><span class="sxs-lookup"><span data-stu-id="24fc9-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="24fc9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24fc9-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="24fc9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24fc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24fc9-107">*pFrameParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24fc9-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24fc9-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="24fc9-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="24fc9-109">Ponteiro para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="24fc9-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="24fc9-110">*pFrameChild* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24fc9-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24fc9-111">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="24fc9-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="24fc9-112">Ponteiro para o nó filho.</span><span class="sxs-lookup"><span data-stu-id="24fc9-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24fc9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24fc9-113">Return value</span></span>

<span data-ttu-id="24fc9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24fc9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24fc9-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24fc9-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="24fc9-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="24fc9-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="24fc9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24fc9-117">Requirements</span></span>



| <span data-ttu-id="24fc9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24fc9-118">Requirement</span></span> | <span data-ttu-id="24fc9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24fc9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24fc9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24fc9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="24fc9-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="24fc9-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="24fc9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24fc9-122">Library</span></span><br/> | <dl> <span data-ttu-id="24fc9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24fc9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24fc9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="24fc9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24fc9-125">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="24fc9-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




