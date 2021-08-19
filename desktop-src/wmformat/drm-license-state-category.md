---
title: DRM_LICENSE_STATE_CATEGORY enumeração (Drmexternals.h)
description: O tipo de enumeração DRM LICENSE STATE CATEGORY define as categorias para cadeias de caracteres de licença \_ \_ \_ DRM exibidas ao usuário.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY formato de mídia das janelas de enumeração
- formato de mídia das janelas de enumeração
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
ms.openlocfilehash: 2bbfd6c566d6c58314416c787110ea77da25416ed73d80ec87fd2d66602d820b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930996"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY enumeração (Drmexternals.h)

O **tipo de \_ enumeração \_ DRM LICENSE STATE \_ CATEGORY** define as categorias para cadeias de caracteres de licença [*DRM*](wmformat-glossary.md) exibidas ao usuário.

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução não permitida".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ UNLIM**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução ilimitada".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ DRM \_ \_ DO WM**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida 5 vezes".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**ESTADO DE LICENÇA DO WM \_ DRM \_ \_ \_ DE**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida de 12/07/07".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**ESTADO \_ DE LICENÇA DO WM DRM \_ \_ \_ ATÉ**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida até 12/07/07".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ FROM \_ UNTIL**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida de 12/05 a 12/09".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ \_ DRM \_ \_ DO WM**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida 5 vezes de 12/05 a 12/09".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**CONTAGEM \_ DE ESTADO DE LICENÇA \_ \_ DRM WM \_ \_ ATÉ**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida 5 vezes até 12/07/07".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ COUNT \_ FROM \_ UNTIL**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida 5 vezes de 12/05 a 12/09".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ EXPIRATION \_ AFTER \_ FIRSTUSE**
</dt> <dd>

Indica que a cadeia de caracteres assumirá o formato "Reprodução válida por 24 horas do primeiro uso".

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração indica a categoria para cada cadeia de caracteres de saída possível a ser exibida. Ele é membro da estrutura [**DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM.**](drm-license-state-data.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK de Formato de Mídia 7 ou versões posteriores do SDK<br/>                       |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





