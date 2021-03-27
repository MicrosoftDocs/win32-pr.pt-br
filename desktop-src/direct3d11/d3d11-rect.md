---
title: D3D11_RECT (D3D11. h)
description: D3D11 \_ RECT é declarado da seguinte maneira
ms.assetid: d1cbbbd7-1221-4706-b805-8422c5ebdadc
keywords:
- D3D11_RECT Direct3D 11
topic_type:
- apiref
api_name:
- D3D11_RECT
api_location:
- D3D11.lib
- D3D11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7fac5627c74123c977aac379826d5264d767ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837972"
---
# <a name="d3d11_rect"></a><span data-ttu-id="5a3f1-104">D3D11 \_ Rect</span><span class="sxs-lookup"><span data-stu-id="5a3f1-104">D3D11\_RECT</span></span>

<span data-ttu-id="5a3f1-105">D3D11 \_ RECT é declarado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5a3f1-105">D3D11\_RECT is declared as follows:</span></span>

``` syntax
typedef RECT D3D11_RECT;
```

<span data-ttu-id="5a3f1-106">Para obter mais informações sobre essa estrutura de retângulo GDI, consulte [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a3f1-106">For more information about this GDI rectangle structure, see [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a3f1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a3f1-107">Remarks</span></span>

<span data-ttu-id="5a3f1-108">Essa estrutura é usada para retângulos de recorte por [**ID3D11DeviceContext:: RSGetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rsgetscissorrects) e [**ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects).</span><span class="sxs-lookup"><span data-stu-id="5a3f1-108">This structure is used for scissor rectangles by [**ID3D11DeviceContext::RSGetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rsgetscissorrects) and [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3f1-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a3f1-109">Requirements</span></span>



| <span data-ttu-id="5a3f1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3f1-110">Requirement</span></span> | <span data-ttu-id="5a3f1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a3f1-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3f1-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a3f1-112">Header</span></span><br/>  | <dl> <span data-ttu-id="5a3f1-113"><dt>D3D11. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f1-113"><dt>D3D11.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a3f1-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a3f1-114">Library</span></span><br/> | <dl> <span data-ttu-id="5a3f1-115"><dt>D3D11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f1-115"><dt>D3D11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3f1-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a3f1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3f1-117">Estruturas principais</span><span class="sxs-lookup"><span data-stu-id="5a3f1-117">Core Structures</span></span>](d3d11-graphics-reference-d3d11-core-structures.md)
</dt> </dl>

 

