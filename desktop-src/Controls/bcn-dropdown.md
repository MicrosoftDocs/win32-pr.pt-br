---
title: Código de notificação BCN_DROPDOWN (WinUser. h)
description: Enviado quando o usuário clica em uma seta suspensa em um botão. A janela pai do controle recebe esse código de notificação na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN código de notificação Windows controles
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbacf22cdabbac7c5d2932c604fab634dbc185207acda8cee311d434478e5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674968"
---
# <a name="bcn_dropdown-notification-code"></a>\_Código de notificação da lista suspensa BCN

Enviado quando o usuário clica em uma seta suspensa em um botão. A janela pai do controle recebe esse código de notificação na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . O membro **rcButton** é definido para descrever a área suspensa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte **lParam** para recuperar a estrutura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . **WParam** contém a ID do controle que envia essa mensagem. O controle de botão deve ter um estilo de botão suspenso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





