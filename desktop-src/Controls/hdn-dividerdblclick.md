---
title: HDN_DIVIDERDBLCLICK de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de header de que o usuário clicou duas vezes na área do divisor do controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9ba7e974ce9e3adac2b48815bfb9bba5273db8298bc9948164be5904dca8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544668"
---
# <a name="hdn_dividerdblclick-notification-code"></a>Código de notificação DO HDN \_ DIVIDERDBLCLICK

Notifica a janela pai de um controle de header de que o usuário clicou duas vezes na área do divisor do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeça e o item cujo divisor foi clicado duas vezes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ DIVIDERDBLCLICKW** (Unicode) e **HDN \_ DIVIDERDBLCLICKA** (ANSI)<br/>   |



 

 





