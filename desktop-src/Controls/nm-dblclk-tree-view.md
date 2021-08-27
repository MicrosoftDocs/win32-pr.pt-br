---
title: NM_DBLCLK de notificação (exibição de árvore) (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que o usuário clicou duas vezes no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- NM_DBLCLK (exibição de árvore) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c18fa9409365aa55b2410f16ae51ddbdcc1113c730b11293f997e1c641277c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088786"
---
# <a name="nm_dblclk-tree-view-notification-code"></a>Código de notificação \_ dbLCLK (exibição de árvore) NM

Notifica a janela pai de um controle de exibição de árvore de que o usuário clicou duas vezes no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK
        
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



 

 





