---
title: LVN_BEGINLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT de código de notificação controles do Windows
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
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918031"
---
# <a name="lvn_beginlabeledit-notification-code"></a>Código de notificação do LVN \_ BEGINLABELEDIT

Notifica uma janela pai do controle de exibição de lista sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item que está sendo editado. Observe que os subitens não podem ser editados; o membro **iSubItem** é sempre definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para permitir que o usuário edite o rótulo, retorne **false**.

Para impedir que o usuário edite o rótulo, retorne **true**.

## <a name="remarks"></a>Comentários

Quando o rótulo é iniciado, um controle de edição é criado, posicionado e inicializado. Antes de ser exibida, o controle List-View envia à janela pai um \_ código de notificação LVN BEGINLABELEDIT.

Para personalizar a edição de rótulo, implemente um manipulador para LVN \_ BEGINLABELEDIT e envie uma mensagem de [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) para o controle de exibição de lista. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .

Quando o usuário cancela ou conclui a edição, a janela pai recebe um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





