---
description: Testa o BoundingBox para interseção com outro objeto.
ms.assetid: df3d3df9-aa74-413d-808c-f7b276d11279
title: Métodos de interseção BoundingBox.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9039d99640ae3989d0b20e9d48f681edabb021f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502343"
---
# <a name="boundingboxintersects-methods"></a><span data-ttu-id="209eb-103">Métodos de interseção BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="209eb-103">BoundingBox.Intersects methods</span></span>

<span data-ttu-id="209eb-104">Testa o BoundingBox para interseção com outro objeto.</span><span class="sxs-lookup"><span data-stu-id="209eb-104">Tests the BoundingBox for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="209eb-105">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="209eb-105">Overload list</span></span>



| <span data-ttu-id="209eb-106">Método</span><span class="sxs-lookup"><span data-stu-id="209eb-106">Method</span></span>                                                                                   | <span data-ttu-id="209eb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="209eb-107">Description</span></span>                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="209eb-108">[**BoundingBox:: Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="209eb-108">[**BoundingBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="209eb-109">Teste o BoundingBox para interseção com um plano.</span><span class="sxs-lookup"><span data-stu-id="209eb-109">Test the BoundingBox for intersection with a plane.</span></span><br/>                                                                     |
| <span data-ttu-id="209eb-110">[**BoundingBox:: Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="209eb-110">[**BoundingBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="209eb-111">Testa o BoundingBox para interseção com outro BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="209eb-111">Tests the BoundingBox for intersection with another BoundingBox.</span></span><br/>                                                        |
| <span data-ttu-id="209eb-112">[**BoundingBox:: Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="209eb-112">[**BoundingBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span></span>      | <span data-ttu-id="209eb-113">Testa o BoundingBox para interseção com um BoundingSphere.</span><span class="sxs-lookup"><span data-stu-id="209eb-113">Tests the BoundingBox for intersection with a BoundingSphere.</span></span><br/>                                                           |
| <span data-ttu-id="209eb-114">[**BoundingBox:: Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="209eb-114">[**BoundingBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="209eb-115">Teste o [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) para interseção com um [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span><span class="sxs-lookup"><span data-stu-id="209eb-115">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="209eb-116">[**BoundingBox:: Intersects (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="209eb-116">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="209eb-117">Teste o BoundingBox para interseção com um Ray.</span><span class="sxs-lookup"><span data-stu-id="209eb-117">Test the BoundingBox for intersection with a ray.</span></span><br/>                                                                       |
| <span data-ttu-id="209eb-118">[**BoundingBox:: Intersects (XMVECTOR, XMVECTOR, XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="209eb-118">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="209eb-119">Teste o BoundingBox para interseção com um triângulo.</span><span class="sxs-lookup"><span data-stu-id="209eb-119">Test the BoundingBox for intersection with a triangle.</span></span><br/>                                                                  |
| <span data-ttu-id="209eb-120">[**BoundingBox:: Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="209eb-120">[**BoundingBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="209eb-121">Teste o [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) para interseção com um [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="209eb-121">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="209eb-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="209eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209eb-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="209eb-123">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="209eb-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="209eb-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="209eb-125">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="209eb-125">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
