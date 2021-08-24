---
title: DRV_ENABLE mensagem (Mmsystem.h)
description: Habilita o driver. O driver deve inicializar todas as variáveis e localizar dispositivos com a interface de entrada e saída (E/S).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ab74abf08380db97a15da22fa99d58d72b6aba124a430cad665f65bc94e26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526276"
---
# <a name="drv_enable-message"></a>Mensagem DRV \_ ENABLE

Habilita o driver. O driver deve inicializar todas as variáveis e localizar dispositivos com a interface de entrada e saída (E/S).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Lidar com a instância do driver instanciada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os *parâmetros dwDriverId,* *lParam1* e *lParam2* não são usados.

Os drivers são considerados habilitados desde o momento em que recebem essa mensagem até que sejam desabilitados usando a [**mensagem DRV \_ DISABLE.**](drv-disable.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





