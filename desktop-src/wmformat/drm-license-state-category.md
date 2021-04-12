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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>Enumeração de DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)

O tipo de enumeração de **categoria de \_ estado de licença \_ \_ DRM** define as categorias para as cadeias de caracteres de [*licença*](wmformat-glossary.md) DRM que são exibidas para o usuário.

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
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_estado da \_ licença \_ \_ do WM DRM**
</dt> <dd>

Indica que a cadeia de caracteres terá a forma "reprodução não permitida".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_UNLIM do \_ estado de licença \_ \_ do WM DRM**
</dt> <dd>

Indica que a cadeia de caracteres terá a forma "reprodução ilimitada".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_contagem de \_ Estados de licenças \_ \_ do WM DRM**
</dt> <dd>

Indica que a cadeia de caracteres terá a forma "reprodução válida 5 vezes".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ \_ estado de licença do WM DRM \_ de**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida de 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**Estado de licença do WM \_ DRM \_ \_ \_ até**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida até 7/12/00."

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ \_ estado de licença do WM DRM \_ de \_ até**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida de 5/12 para 9/12."

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida 5 vezes de 5/12 para 9/12."

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**contagem de estado de licença do WM \_ DRM \_ \_ \_ \_ até**
</dt> <dd>

Indica que a cadeia de caracteres terá a forma "reprodução válida 5 vezes até 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ \_ \_ contagem de Estados de licenças \_ do WM DRM de \_ até**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida 5 vezes de 5/12 para 9/12."

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_expiração do estado de licença do WM DRM \_ \_ \_ \_ após \_ FIRSTUSE**
</dt> <dd>

Indica que a cadeia de caracteres assumirá a forma "reprodução válida por 24 horas a partir do primeiro uso".

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração indica a categoria para cada cadeia de caracteres de saída possível a ser exibida. É um membro da estrutura de [**\_ dados de \_ estado \_ da licença do DRM**](drm-license-state-data.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | SDK do Windows Media Format 7 ou versões posteriores do SDK<br/>                       |
| parâmetro<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





