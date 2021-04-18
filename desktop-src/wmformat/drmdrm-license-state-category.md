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
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>Enumeração de DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)

O tipo de enumeração de **\_ categoria de \_ estado \_ de licença DRM** especifica o tipo de restrição de licença que é descrito por uma estrutura de [**dados de \_ estado de licença \_ \_ DRM**](drmdrm-license-state-data.md) .

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_estado da \_ licença \_ \_ do WM DRM**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida não é permitida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_UNLIM do \_ estado de licença \_ \_ do WM DRM**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida sem restrição.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_contagem de \_ Estados de licenças \_ \_ do WM DRM**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado de licença do WM DRM \_ de**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida após uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de licença do WM \_ DRM \_ \_ \_ até**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida até uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ estado de licença do WM DRM \_ de \_ até**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida entre duas datas definidas.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes após uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**contagem de estado de licença do WM \_ DRM \_ \_ \_ \_ até**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes até uma data definida.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de \_ até**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida, mas apenas um número definido de vezes entre duas datas de conjunto.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiração do estado de licença do WM DRM \_ \_ \_ \_ após \_ FIRSTUSE**
</dt> <dd>

Especifica que a ação para a qual **os \_ \_ \_ dados de estado da licença DRM** foi recebida é permitida por um determinado período de tempo que começa com o primeiro uso da ação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





