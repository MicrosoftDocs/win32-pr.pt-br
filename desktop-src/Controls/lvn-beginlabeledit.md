---
title: LVN_BEGINLABELEDIT de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5b5ecfed8fdc15ec2779e204d01b0375c7da702e2a2e9fe8a3cdc3b178b0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830647"
---
# <a name="lvn_beginlabeledit-notification-code"></a>Código de notificação LVN \_ BEGINLABELEDIT

Notifica a janela pai de um controle de exibição de lista sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) O **membro** do item dessa estrutura é uma [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item que está sendo editado. Observe que subitens não podem ser editados; o **membro iSubItem** é sempre definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para permitir que o usuário edite o rótulo, retorne **FALSE.**

Para impedir que o usuário edite o rótulo, retorne **TRUE.**

## <a name="remarks"></a>Comentários

Quando a edição de rótulo é iniciada, um controle de edição é criado, posicionado e inicializado. Antes de ser exibido, o controle de exibição de lista envia à janela pai um código de notificação LVN \_ BEGINLABELEDIT.

Para personalizar a edição de rótulo, implemente um manipulador para LVN BEGINLABELEDIT e envie uma mensagem \_ [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) para o controle de exibição de lista. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse alça para personalizar o controle de edição enviando as mensagens **EM \_ XXX** usuais.

Quando o usuário cancela ou conclui a edição, a janela pai recebe um código de notificação [LVN \_ ENDLABELEDIT.](lvn-endlabeledit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





