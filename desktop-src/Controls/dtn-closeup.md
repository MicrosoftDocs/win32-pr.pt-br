---
title: DTN_CLOSEUP de notificação (Commctrl.h)
description: Enviado por um controle DTP (selador de data e hora) quando o usuário fecha o calendário do mês de lista listada.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP de notificação Windows Controles
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97cd2d799d05afc638b60adc9203eaad80feb159f985df8b3813403bf5ca0d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877716"
---
# <a name="dtn_closeup-notification-code"></a>Código de notificação CLOSEUP de DTN \_

Enviado por um controle DTP (selador de data e hora) quando o usuário fecha o calendário do mês de lista listada. O calendário do mês é fechado quando o usuário escolhe uma data do calendário do mês ou clica na seta para baixo enquanto o calendário está aberto. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre a notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Os controles DTP não mantêm um controle de calendário de mês filho estático. O controle DTP destrói o controle de calendário do mês filho antes de enviar esse código de notificação. Portanto, seu aplicativo não deve depender de uma alça de janela estática para o calendário do mês filho do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[LISTA DE \_ DTN](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





