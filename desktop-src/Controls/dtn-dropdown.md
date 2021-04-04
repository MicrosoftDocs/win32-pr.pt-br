---
title: DTN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando o usuário ativa o calendário do mês suspenso. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824590"
---
# <a name="dtn_dropdown-notification-code"></a>\_Código de notificação da lista suspensa DTN

Enviado por um controle do seletor de data e hora (DTP) quando o usuário ativa o calendário do mês suspenso. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre a notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Uma tarefa que seu manipulador de notificação pode precisar executar é personalizar o controle de calendário de mês suspenso. Por exemplo, se você não quiser "ir para hoje", precisará definir o estilo [**MCS \_ noToday**](month-calendar-control-styles.md)  do controle. Para recuperar um identificador para o controle mês-Calendar, envie o controle DTP a uma mensagem [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) . Você pode usar esse identificador e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir o estilo de calendário de mês desejado.

Os controles DTP não mantêm um controle de calendário de mês filho estático. O controle DTP cria um novo controle de calendário mensal antes de enviar este código de notificação. Além disso, o controle DTP destrói o controle filho quando ele não está ativo (visível). Portanto, seu aplicativo não deve depender de um identificador de janela estático para o calendário do mês filho do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[DTN \_ closeup](dtn-closeup.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

