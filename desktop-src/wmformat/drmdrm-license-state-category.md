---
title: DRM_LICENSE_STATE_CATEGORY enumeração (Wmdrmsdk.h)
description: O tipo de enumeração DRM LICENSE STATE CATEGORY especifica o tipo de restrição de licença descrito por uma estrutura DE DADOS DE \_ \_ ESTADO DE LICENÇA \_ \_ \_ \_ DRM.
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY formato de mídia das janelas de enumeração
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
ms.openlocfilehash: 43b8724526142236b70faade68bf7d3ca358eb3f3810cae73f58adde17f25a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591566"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY enumeração (Wmdrmsdk.h)

O **tipo de enumeração DRM \_ LICENSE STATE \_ \_ CATEGORY** especifica o tipo de restrição de licença descrito por uma estrutura DE DADOS DE [**ESTADO DE LICENÇA \_ \_ \_ DRM.**](drmdrm-license-state-data.md)

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Especifica que a ação para a qual os **DADOS DE ESTADO DA LICENÇA DRM \_ \_ \_** foram recebidos não é permitida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ UNLIM**
</dt> <dd>

Especifica que a ação para a qual os **DADOS DE ESTADO DA LICENÇA DRM \_ \_ \_** foram recebidos é permitida sem restrição.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ DRM \_ \_ DO WM**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA **\_ LICENÇA \_ \_ DRM** foram recebidos é permitida, mas apenas um número definido de vezes.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**ESTADO DE LICENÇA DO WM \_ DRM \_ \_ \_ DE**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA **\_ LICENÇA \_ \_ DRM** foram recebidos é permitida após uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**ESTADO \_ DE LICENÇA DO WM DRM \_ \_ \_ ATÉ**
</dt> <dd>

Especifica que a ação para a qual os **DADOS DE ESTADO DA LICENÇA DRM \_ \_ \_** foram recebidos é permitida até uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ FROM \_ UNTIL**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA **LICENÇA DRM \_ \_ \_** foram recebidos é permitida entre duas datas definidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ \_ DRM \_ \_ DO WM**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA LICENÇA DRM foram recebidos é permitida, mas apenas um número definido de vezes após uma data definida. **\_ \_ \_**

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ \_ DRM WM \_ \_ ATÉ**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA **LICENÇA DRM \_ \_ \_** foram recebidos é permitida, mas apenas um número definido de vezes até uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ COUNT \_ FROM \_ UNTIL**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA **LICENÇA DRM \_ \_ \_** foram recebidos é permitida, mas apenas um número definido de vezes entre duas datas definidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ EXPIRATION \_ AFTER \_ FIRSTUSE**
</dt> <dd>

Especifica que a ação para a qual os DADOS DE ESTADO DA LICENÇA DRM foram recebidos é permitida por um período de tempo definido, começando com o primeiro uso da ação. **\_ \_ \_**

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





