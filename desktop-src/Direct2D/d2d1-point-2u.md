---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Representa um par de coordenadas x e y em espaço bidimensional. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172728"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="f4385-105">D2D1 \_ ponto \_ 2U</span><span class="sxs-lookup"><span data-stu-id="f4385-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="f4385-106">Representa um par de coordenadas x e y em espaço bidimensional.</span><span class="sxs-lookup"><span data-stu-id="f4385-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="f4385-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4385-107">Remarks</span></span>

<span data-ttu-id="f4385-108">Os pontos em Direct2D são representados pelas estruturas do [**d2d1 \_ Point \_ 2F**](d2d1-point-2f.md) ou do **d2d1 \_ Point \_ 2U** .</span><span class="sxs-lookup"><span data-stu-id="f4385-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="f4385-109">Ambos contêm uma coordenada x e um par de coordenadas y em espaço bidimensional.</span><span class="sxs-lookup"><span data-stu-id="f4385-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="f4385-110">A estrutura **d2d1 do \_ ponto \_ 2F** armazena as coordenadas como valores **float** e a **estrutura \_ \_ 2U do ponto d2d1** armazena-as como valores **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="f4385-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="f4385-111">**D2d1 \_ O ponto \_ 2U** é um novo nome para o tipo já definido [**D2D \_ Point \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="f4385-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4385-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4385-112">Requirements</span></span>



| <span data-ttu-id="f4385-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4385-113">Requirement</span></span> | <span data-ttu-id="f4385-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f4385-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4385-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4385-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f4385-116">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f4385-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f4385-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4385-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f4385-118">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f4385-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f4385-119">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="f4385-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f4385-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f4385-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="f4385-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4385-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4385-122"><dt>D2DBaseTypes. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4385-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f4385-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4385-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4385-124">**D2D \_ ponto \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="f4385-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="f4385-125">**\_Ponto D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="f4385-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





