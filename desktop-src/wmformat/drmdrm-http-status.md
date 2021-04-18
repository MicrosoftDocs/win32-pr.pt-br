---
title: Enumeração de DRM_HTTP_STATUS (wmdrmsdk. h)
description: O \_ \_ tipo de enumeração de status http DRM define um intervalo de Estados http para uma solicitação de DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Formato de mídia do Windows de enumeração de DRM_HTTP_STATUS
- Formato de mídia do Windows de enumeração
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
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764483"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>Enumeração de DRM_HTTP_STATUS (wmdrmsdk. h)

O tipo de enumeração de **\_ \_ status http DRM** define um intervalo de Estados http para uma solicitação de DRM.

## <a name="syntax"></a>Syntax


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

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP não \_ iniciado**
</dt> <dd>

As operações HTTP não foram iniciadas.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_conexão http**
</dt> <dd>

A conexão está sendo estabelecida.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitando http**
</dt> <dd>

Os dados estão sendo solicitados.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**recebimento de HTTP \_**
</dt> <dd>

Os dados estão sendo recebidos.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ concluído**
</dt> <dd>

As operações HTTP foram concluídas.

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

 

 





