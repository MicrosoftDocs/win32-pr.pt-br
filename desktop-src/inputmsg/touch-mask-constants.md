---
title: Máscara de toque
description: Os valores que podem aparecer no campo touchMask da estrutura de POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455825"
---
# <a name="touch-mask"></a><span data-ttu-id="af77b-103">Máscara de toque</span><span class="sxs-lookup"><span data-stu-id="af77b-103">Touch Mask</span></span>

<span data-ttu-id="af77b-104">Os valores que podem aparecer no campo **touchMask** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="af77b-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="af77b-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="af77b-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="af77b-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af77b-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="af77b-107">Padrão.</span><span class="sxs-lookup"><span data-stu-id="af77b-107">Default.</span></span> <span data-ttu-id="af77b-108">Nenhum dos campos opcionais é válido.</span><span class="sxs-lookup"><span data-stu-id="af77b-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af77b-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="af77b-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af77b-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af77b-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="af77b-111">**rcContact** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) é válido.</span><span class="sxs-lookup"><span data-stu-id="af77b-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af77b-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="af77b-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af77b-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="af77b-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="af77b-114">a **orientação** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) é válida.</span><span class="sxs-lookup"><span data-stu-id="af77b-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af77b-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="af77b-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af77b-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="af77b-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="af77b-117">a **pressão** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) é válida.</span><span class="sxs-lookup"><span data-stu-id="af77b-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af77b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af77b-118">Requirements</span></span>



| <span data-ttu-id="af77b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="af77b-119">Requirement</span></span> | <span data-ttu-id="af77b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="af77b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af77b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af77b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af77b-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="af77b-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="af77b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af77b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af77b-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="af77b-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="af77b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af77b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="af77b-126"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af77b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="af77b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af77b-128">Constantes</span><span class="sxs-lookup"><span data-stu-id="af77b-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="af77b-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="af77b-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





