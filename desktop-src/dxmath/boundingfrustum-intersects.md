---
description: Testa o BoundingFrustum para interseção com outro objeto.
ms.assetid: b087761c-b298-4b64-86e7-60cd73543144
title: Métodos de interseção BoundingFrustum.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9eb0082fda21978fdf6371267e4cfa0bf531622b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661547"
---
# <a name="boundingfrustumintersects-methods"></a><span data-ttu-id="358f5-103">Métodos de interseção BoundingFrustum.</span><span class="sxs-lookup"><span data-stu-id="358f5-103">BoundingFrustum.Intersects methods</span></span>

<span data-ttu-id="358f5-104">Testa o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com outro objeto.</span><span class="sxs-lookup"><span data-stu-id="358f5-104">Tests the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="358f5-105">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="358f5-105">Overload list</span></span>



| <span data-ttu-id="358f5-106">Método</span><span class="sxs-lookup"><span data-stu-id="358f5-106">Method</span></span>                                                                                           | <span data-ttu-id="358f5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="358f5-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="358f5-108">[**BoundingFrustum:: Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="358f5-108">[**BoundingFrustum::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span></span>                   | <span data-ttu-id="358f5-109">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um plano.</span><span class="sxs-lookup"><span data-stu-id="358f5-109">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a plane.</span></span><br/>                                              |
| <span data-ttu-id="358f5-110">[**BoundingFrustum:: Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="358f5-110">[**BoundingFrustum::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="358f5-111">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span><span class="sxs-lookup"><span data-stu-id="358f5-111">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span></span><br/>                 |
| <span data-ttu-id="358f5-112">[**BoundingFrustum:: Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="358f5-112">[**BoundingFrustum::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span></span>      | <span data-ttu-id="358f5-113">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span><span class="sxs-lookup"><span data-stu-id="358f5-113">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span></span><br/>           |
| <span data-ttu-id="358f5-114">[**BoundingFrustum:: Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="358f5-114">[**BoundingFrustum::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="358f5-115">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com outro **BoundingFrustum**.</span><span class="sxs-lookup"><span data-stu-id="358f5-115">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another **BoundingFrustum**.</span></span><br/>                          |
| <span data-ttu-id="358f5-116">[**BoundingFrustum:: Intersects (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="358f5-116">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="358f5-117">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um Ray.</span><span class="sxs-lookup"><span data-stu-id="358f5-117">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a ray.</span></span><br/>                                                |
| <span data-ttu-id="358f5-118">[**BoundingFrustum:: Intersects (XMVECTOR, XMVECTOR, XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="358f5-118">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="358f5-119">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um triângulo.</span><span class="sxs-lookup"><span data-stu-id="358f5-119">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a triangle.</span></span><br/>                                           |
| <span data-ttu-id="358f5-120">[**BoundingFrustum:: Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="358f5-120">[**BoundingFrustum::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="358f5-121">Teste o [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) para interseção com um [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="358f5-121">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="358f5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="358f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358f5-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="358f5-123">Methods</span></span>](boundingfrustum-methods.md)
</dt> <dt>

<span data-ttu-id="358f5-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="358f5-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="358f5-125">**BoundingFrustum**</span><span class="sxs-lookup"><span data-stu-id="358f5-125">**BoundingFrustum**</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)
</dt> </dl>

 

 
