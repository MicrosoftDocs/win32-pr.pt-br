---
title: D3D12_RECT (D3D12. h)
description: D3D12 \_ RECT é declarado como um RECT.
ms.assetid: 39511ACE-7AC5-42A2-896D-7E0977A346C6
keywords:
- D3D12_RECT
topic_type:
- apiref
api_name:
- D3D12_RECT
api_location:
- D3D12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d408832e800413f94e251ee27a57e5b326378c36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788921"
---
# <a name="d3d12_rect"></a><span data-ttu-id="b6c0c-104">D3D12 \_ Rect</span><span class="sxs-lookup"><span data-stu-id="b6c0c-104">D3D12\_RECT</span></span>

<span data-ttu-id="b6c0c-105">D3D12 \_ RECT é declarado como um RECT.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-105">D3D12\_RECT is declared as a RECT.</span></span> <span data-ttu-id="b6c0c-106">Para obter mais informações sobre essa estrutura de retângulo GDI, consulte [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6c0c-106">For more information about this GDI rectangle structure, see [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span>

``` syntax
typedef RECT D3D12_RECT;
```

## <a name="remarks"></a><span data-ttu-id="b6c0c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c0c-107">Remarks</span></span>

<span data-ttu-id="b6c0c-108">Essa estrutura é usada pelos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="b6c0c-108">This structure is used by the following methods:</span></span>

-   [<span data-ttu-id="b6c0c-109">**RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-109">**RSSetScissorRects**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)
-   [<span data-ttu-id="b6c0c-110">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-110">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="b6c0c-111">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-111">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="b6c0c-112">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-112">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="b6c0c-113">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-113">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)

<span data-ttu-id="b6c0c-114">Essa estrutura é um membro da estrutura [**de \_ \_ região de descarte de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) .</span><span class="sxs-lookup"><span data-stu-id="b6c0c-114">This structure is a member of the [**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c0c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c0c-115">Requirements</span></span>



| <span data-ttu-id="b6c0c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c0c-116">Requirement</span></span> | <span data-ttu-id="b6c0c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c0c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c0c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6c0c-118">Header</span></span><br/> | <dl> <span data-ttu-id="b6c0c-119"><dt>D3D12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0c-119"><dt>D3D12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c0c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6c0c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c0c-121">Estruturas principais</span><span class="sxs-lookup"><span data-stu-id="b6c0c-121">Core Structures</span></span>](direct3d-12-structures.md)
</dt> <dt>

[<span data-ttu-id="b6c0c-122">**CD3DX12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="b6c0c-122">**CD3DX12\_RECT**</span></span>](cd3dx12-rect.md)
</dt> </dl>

 

