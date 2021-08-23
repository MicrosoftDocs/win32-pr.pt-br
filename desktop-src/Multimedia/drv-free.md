---
title: Mensagem de DRV_FREE (mmsystem. h)
description: Notifica o driver de que ele está sendo removido da memória. O driver deve liberar qualquer memória e outros recursos do sistema alocados.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- mensagem de DRV_FREE Windows multimídia
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a558dc7a2c3ece040790b2351ff39dc3054d660eb9368567ed7ce79d40c8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526206"
---
# <a name="drv_free-message"></a>Mensagem do DRV \_ Free

Notifica o driver de que ele está sendo removido da memória. O driver deve liberar qualquer memória e outros recursos do sistema alocados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador da instância de driver instalável.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.

A mensagem **drv \_ Free** é sempre a última mensagem que um driver de dispositivo recebe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





