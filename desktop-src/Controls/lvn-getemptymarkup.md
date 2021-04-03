---
title: LVN_GETEMPTYMARKUP código de notificação (commctrl. h)
description: Enviado por controle de exibição de lista para sua janela pai quando o controle não tem itens. O \_ código de notificação LVN GETEMPTYMARKUP é uma solicitação para que a janela pai forneça o texto de marcação. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP de código de notificação controles do Windows
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
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824860"
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

## <a name="return-value"></a>Retornar valor

Retornar **true** para definir o texto de marcação no controle de exibição de lista ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . O parâmetro *wParam* contém a ID do controle que envia essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





