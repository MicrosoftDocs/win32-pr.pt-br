---
title: Enumeração de DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)
description: O \_ \_ \_ tipo de enumeração de categoria de estado de licença DRM especifica o tipo de restrição de licença que é descrito por uma \_ estrutura de dados de estado de licença DRM \_ \_ .
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- Formato de mídia do Windows de enumeração de DRM_LICENSE_STATE_CATEGORY
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785510"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="a9d70-104">Enumeração de DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="a9d70-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="a9d70-105">O tipo de enumeração de **\_ categoria de \_ estado \_ de licença DRM** especifica o tipo de restrição de licença que é descrito por uma estrutura de [**dados de \_ estado de licença \_ \_ DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d70-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d70-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d70-106">Syntax</span></span>


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a><span data-ttu-id="a9d70-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="a9d70-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9d70-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_estado da \_ licença \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="a9d70-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-109">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida não é permitida.</span><span class="sxs-lookup"><span data-stu-id="a9d70-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_UNLIM do \_ estado de licença \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="a9d70-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-111">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida sem restrição.</span><span class="sxs-lookup"><span data-stu-id="a9d70-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_contagem de \_ Estados de licenças \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="a9d70-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-113">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes.</span><span class="sxs-lookup"><span data-stu-id="a9d70-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado de licença do WM DRM \_ de**</span><span class="sxs-lookup"><span data-stu-id="a9d70-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-115">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida após uma data definida.</span><span class="sxs-lookup"><span data-stu-id="a9d70-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de licença do WM \_ DRM \_ \_ \_ até**</span><span class="sxs-lookup"><span data-stu-id="a9d70-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-117">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida até uma data definida.</span><span class="sxs-lookup"><span data-stu-id="a9d70-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ estado de licença do WM DRM \_ de \_ até**</span><span class="sxs-lookup"><span data-stu-id="a9d70-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-119">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida entre duas datas definidas.</span><span class="sxs-lookup"><span data-stu-id="a9d70-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de**</span><span class="sxs-lookup"><span data-stu-id="a9d70-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-121">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes após uma data definida.</span><span class="sxs-lookup"><span data-stu-id="a9d70-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**contagem de estado de licença do WM \_ DRM \_ \_ \_ \_ até**</span><span class="sxs-lookup"><span data-stu-id="a9d70-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-123">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes até uma data definida.</span><span class="sxs-lookup"><span data-stu-id="a9d70-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de \_ até**</span><span class="sxs-lookup"><span data-stu-id="a9d70-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-125">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes entre duas datas de conjunto.</span><span class="sxs-lookup"><span data-stu-id="a9d70-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="a9d70-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiração do estado de licença do WM DRM \_ \_ \_ \_ após \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="a9d70-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="a9d70-127">Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida por um determinado período de tempo que começa com o primeiro uso da ação.</span><span class="sxs-lookup"><span data-stu-id="a9d70-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9d70-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9d70-128">Remarks</span></span>

<span data-ttu-id="a9d70-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a9d70-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d70-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9d70-130">Requirements</span></span>



| <span data-ttu-id="a9d70-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d70-131">Requirement</span></span> | <span data-ttu-id="a9d70-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a9d70-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d70-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9d70-133">Header</span></span><br/> | <dl> <span data-ttu-id="a9d70-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d70-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d70-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9d70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d70-136">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="a9d70-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





