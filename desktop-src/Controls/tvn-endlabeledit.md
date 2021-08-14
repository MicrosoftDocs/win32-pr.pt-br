---
title: TVN_ENDLABELEDIT de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore sobre o final da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38be7b9fde4b96f3510cd59683ee9df471cc4d77342fe375d9b1818b8ae7da46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408196"
---
# <a name="tvn_endlabeledit-notification-code"></a>Código de notificação TVN \_ ENDLABELEDIT

Notifica a janela pai de um controle de exibição de árvore sobre o final da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) O **membro** do item dessa estrutura é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **hItem**, **lParam** e **pszText** contêm informações válidas sobre o item que foi editado. Se a edição de rótulo tiver sido cancelada, **o membro pszText** da estrutura **TVITEM** será **NULL**; caso contrário, **pszText** é o endereço do texto editado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o **membro pszText** for não **NULL,** retorne **TRUE** para definir o rótulo do item para o texto editado. Retorne **FALSE** para rejeitar o texto editado e reverter para o rótulo original.

## <a name="remarks"></a>Comentários

Se o **membro pszText** for **NULL,** o valor de retorno será ignorado.

Se você especificou o valor LPSTR TEXTCALLBACK para este item e o membro \_ **pszText** é não **NULL,** o manipulador TVN ENDLABELEDIT deve copiar o texto de \_ **pszText** para o armazenamento local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





