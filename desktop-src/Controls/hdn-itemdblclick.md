---
title: HDN_ITEMDBLCLICK de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de header de que o usuário clicou duas vezes no controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY. Somente os controles de header definidos para o estilo \_ BOTÕES HDS enviam esse código de notificação.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK código de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544606"
---
# <a name="hdn_itemdblclick-notification-code"></a>Código de notificação DO HDN \_ ITEMDBLCLICK

Notifica a janela pai de um controle de header de que o usuário clicou duas vezes no controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) Somente os controles de header definidos para o estilo [**\_ BOTÕES HDS**](header-control-styles.md) enviam esse código de notificação.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





