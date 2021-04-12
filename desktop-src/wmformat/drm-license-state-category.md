---
title: Enumeração de DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)
description: O \_ tipo de enumeração de categoria de estado de licença DRM \_ \_ define as categorias para as cadeias de caracteres de licença DRM que são exibidas para o usuário.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- Formato de mídia do Windows de enumeração de DRM_LICENSE_STATE_CATEGORY
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455555"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="88f9f-105">Enumeração de DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="88f9f-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="88f9f-106">O tipo de enumeração de **categoria de \_ estado de licença \_ \_ DRM** define as categorias para as cadeias de caracteres de [*licença*](wmformat-glossary.md) DRM que são exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="88f9f-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f9f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88f9f-107">Syntax</span></span>


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
} ;
```



## <a name="constants"></a><span data-ttu-id="88f9f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="88f9f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88f9f-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_estado da \_ licença \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="88f9f-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-110">Indica que a cadeia de caracteres terá a forma "reprodução não permitida".</span><span class="sxs-lookup"><span data-stu-id="88f9f-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_UNLIM do \_ estado de licença \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="88f9f-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-112">Indica que a cadeia de caracteres terá a forma "reprodução ilimitada".</span><span class="sxs-lookup"><span data-stu-id="88f9f-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_contagem de \_ Estados de licenças \_ \_ do WM DRM**</span><span class="sxs-lookup"><span data-stu-id="88f9f-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-114">Indica que a cadeia de caracteres terá a forma "reprodução válida 5 vezes".</span><span class="sxs-lookup"><span data-stu-id="88f9f-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado de licença do WM DRM \_ de**</span><span class="sxs-lookup"><span data-stu-id="88f9f-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-116">Indica que a cadeia de caracteres assumirá a forma "reprodução válida de 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="88f9f-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de licença do WM \_ DRM \_ \_ \_ até**</span><span class="sxs-lookup"><span data-stu-id="88f9f-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-118">Indica que a cadeia de caracteres assumirá a forma "reprodução válida até 7/12/00."</span><span class="sxs-lookup"><span data-stu-id="88f9f-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ estado de licença do WM DRM \_ de \_ até**</span><span class="sxs-lookup"><span data-stu-id="88f9f-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-120">Indica que a cadeia de caracteres assumirá a forma "reprodução válida de 5/12 para 9/12."</span><span class="sxs-lookup"><span data-stu-id="88f9f-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de**</span><span class="sxs-lookup"><span data-stu-id="88f9f-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-122">Indica que a cadeia de caracteres assumirá a forma "reprodução válida 5 vezes de 5/12 para 9/12."</span><span class="sxs-lookup"><span data-stu-id="88f9f-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**contagem de estado de licença do WM \_ DRM \_ \_ \_ \_ até**</span><span class="sxs-lookup"><span data-stu-id="88f9f-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-124">Indica que a cadeia de caracteres terá a forma "reprodução válida 5 vezes até 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="88f9f-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de \_ até**</span><span class="sxs-lookup"><span data-stu-id="88f9f-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-126">Indica que a cadeia de caracteres assumirá a forma "reprodução válida 5 vezes de 5/12 para 9/12."</span><span class="sxs-lookup"><span data-stu-id="88f9f-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="88f9f-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiração do estado de licença do WM DRM \_ \_ \_ \_ após \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="88f9f-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="88f9f-128">Indica que a cadeia de caracteres assumirá a forma "reprodução válida por 24 horas a partir do primeiro uso".</span><span class="sxs-lookup"><span data-stu-id="88f9f-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88f9f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="88f9f-129">Remarks</span></span>

<span data-ttu-id="88f9f-130">Essa enumeração indica a categoria para cada cadeia de caracteres de saída possível a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="88f9f-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="88f9f-131">É um membro da estrutura de [**\_ dados de \_ estado \_ da licença do DRM**](drm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="88f9f-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f9f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88f9f-132">Requirements</span></span>



| <span data-ttu-id="88f9f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f9f-133">Requirement</span></span> | <span data-ttu-id="88f9f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="88f9f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f9f-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88f9f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="88f9f-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88f9f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88f9f-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88f9f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="88f9f-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88f9f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="88f9f-139">Versão</span><span class="sxs-lookup"><span data-stu-id="88f9f-139">Version</span></span><br/>                  | <span data-ttu-id="88f9f-140">SDK do Windows Media Format 7 ou versões posteriores do SDK</span><span class="sxs-lookup"><span data-stu-id="88f9f-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="88f9f-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88f9f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="88f9f-142"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f9f-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f9f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="88f9f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f9f-144">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="88f9f-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





