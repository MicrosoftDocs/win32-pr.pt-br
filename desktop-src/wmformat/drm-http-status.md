---
title: Enumeração de DRM_HTTP_STATUS (Drmexternals. h)
description: O \_ tipo de enumeração de status http DRM \_ define um intervalo de Estados para uma solicitação de DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Formato de mídia do Windows de enumeração de DRM_HTTP_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757643"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>Enumeração de DRM_HTTP_STATUS (Drmexternals. h)

O tipo de enumeração de **\_ \_ status http DRM** define um intervalo de Estados para uma solicitação de [*DRM*](wmformat-glossary.md) .

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

Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](wm-individualize-status.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | SDK do Windows Media Format 7 ou versões posteriores do SDK<br/>                       |
| parâmetro<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_status de individualização de DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





