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
ms.openlocfilehash: 47e339fda95ccf7408ad2f218179cfb591da217b16fbbce9c9870eabd7437eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848222"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>Enumeração de DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)

O tipo de enumeração **\_ \_ status de individualização de DRM** define os Estados válidos para individualização de DRM.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**i \_ INdefinido**
</dt> <dd>

Este valor está reservado para uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**início do i \_**
</dt> <dd>

Indica o início do processo de individualização.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**i com \_ sucesso**
</dt> <dd>

Indica que o processo de individualização foi concluído.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**falha de i \_**
</dt> <dd>

Indica que o processo de individualização falhou.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**i \_ cancelar**
</dt> <dd>

Indica que o processo de individualização foi cancelado pelo aplicativo.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Download do i \_**
</dt> <dd>

Indica que a atualização de segurança está sendo baixada.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**i \_ instalar**
</dt> <dd>

Indica que a atualização de segurança está sendo instalada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](drmwm-individualize-status.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





