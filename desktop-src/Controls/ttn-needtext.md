---
title: TTN_NEEDTEXT de notificação (Commctrl.h)
description: Enviado por um controle de dica de ferramenta para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é idêntico ao TTN \_ GETDISPINFO. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT de notificação Windows Controles
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dae1ac1eb721d918acf38745f19c7e6dee4a6a296c7fa8003f516717ece6cf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967796"
---
# <a name="ttn_needtext-notification-code"></a>Código de notificação \_ TTN NEEDTEXT

Enviado por um controle de dica de ferramenta para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é idêntico [ao TTN \_ GETDISPINFO.](ttn-getdispinfo.md) Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica a ferramenta que precisa de texto e recebe as informações solicitadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Preencha os membros apropriados da estrutura para retornar as informações solicitadas para o controle de dica de ferramenta. Se o manipulador de mensagens definir o membro **uFlags** da estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) como TTF \_ DI SETITEM, o controle de dica de ferramenta armazenará as informações e não as solicitará \_ novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) e **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





