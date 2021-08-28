---
title: LVN_GETEMPTYMARKUP código de notificação (commctrl. h)
description: Enviado por controle de exibição de lista para sua janela pai quando o controle não tem itens. O \_ código de notificação LVN GETEMPTYMARKUP é uma solicitação para que a janela pai forneça o texto de marcação. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP código de notificação Windows controles
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5da87d0585a22d41743e58e946c4b1b39ca24c8bb131e9084596ce4f8c2b7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005697"
---
# <a name="lvn_getemptymarkup-notification-code"></a>Código de notificação do LVN \_ GETEMPTYMARKUP

Enviado por controle de exibição de lista para sua janela pai quando o controle não tem itens. O \_ código de notificação LVN GETEMPTYMARKUP é uma solicitação para que a janela pai forneça o texto de marcação. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Defina os membros dessa estrutura para fornecer o texto de marcação para o controle de exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **true** para definir o texto de marcação no controle de exibição de lista ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . O parâmetro *wParam* contém a ID do controle que envia essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





