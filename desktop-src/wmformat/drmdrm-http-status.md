---
title: DRM_HTTP_STATUS enumeração (Wmdrmsdk.h)
description: O tipo de enumeração STATUS HTTP DO DRM \_ define um intervalo de estados HTTP para uma \_ solicitação DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS formato de mídia das janelas de enumeração
- formato de mídia das janelas de enumeração
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385a52811cc8deb7e1c221737bd97391122160de065ca28111132ee6c5e4a859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447756"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>DRM_HTTP_STATUS enumeração (Wmdrmsdk.h)

O **tipo de \_ enumeração STATUS HTTP \_ DO DRM** define um intervalo de estados HTTP para uma solicitação DRM.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**
</dt> <dd>

As operações HTTP não foram iniciadas.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**CONEXÃO \_ HTTP**
</dt> <dd>

A conexão está sendo estabelecida.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**SOLICITAÇÃO \_ HTTP**
</dt> <dd>

Os dados estão sendo solicitados.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**RECEBIMENTO \_ DE HTTP**
</dt> <dd>

Os dados estão sendo recebidos.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ CONCLUÍDO**
</dt> <dd>

As operações HTTP estão concluídas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela estrutura [**WM \_ INDIVIDUALIZE \_ STATUS.**](drmwm-individualize-status.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





