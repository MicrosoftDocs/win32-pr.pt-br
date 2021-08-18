---
title: NM_CLICK (exibição de árvore) de código de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que o usuário clicou no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK (exibição de árvore) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d942504afd13359f38fa62c4f6a283367288873f89922311242516b9063990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018884"
---
# <a name="nm_click-tree-view-notification-code"></a>Código de \_ notificação NM CLICK (exibição de árvore)

Notifica a janela pai de um controle de exibição de árvore de que o usuário clicou no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne um valor que não seja zero para impedir o processamento padrão ou zero para permitir o processamento padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





