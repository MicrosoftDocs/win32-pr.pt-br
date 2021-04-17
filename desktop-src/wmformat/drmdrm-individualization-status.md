---
title: Enumeração de DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: O \_ tipo de enumeração status de individualização de DRM \_ define os Estados válidos para individualização de DRM. | Enumeração de DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Formato de mídia do Windows de enumeração de DRM_INDIVIDUALIZATION_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749175"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="c5d9f-106">Enumeração de DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="c5d9f-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="c5d9f-107">O tipo de enumeração **\_ \_ status de individualização de DRM** define os Estados válidos para individualização de DRM.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d9f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d9f-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="c5d9f-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5d9f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5d9f-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**i \_ INdefinido**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-111">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**início do i \_**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-113">Indica o início do processo de individualização.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**i com \_ sucesso**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-115">Indica que o processo de individualização foi concluído.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**falha de i \_**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-117">Indica que o processo de individualização falhou.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**i \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-119">Indica que o processo de individualização foi cancelado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Download do i \_**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-121">Indica que a atualização de segurança está sendo baixada.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="c5d9f-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**i \_ instalar**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="c5d9f-123">Indica que a atualização de segurança está sendo instalada.</span><span class="sxs-lookup"><span data-stu-id="c5d9f-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5d9f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5d9f-124">Remarks</span></span>

<span data-ttu-id="c5d9f-125">Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d9f-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d9f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d9f-126">Requirements</span></span>



| <span data-ttu-id="c5d9f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d9f-127">Requirement</span></span> | <span data-ttu-id="c5d9f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c5d9f-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d9f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5d9f-129">Header</span></span><br/> | <dl> <span data-ttu-id="c5d9f-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d9f-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d9f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5d9f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d9f-132">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="c5d9f-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





