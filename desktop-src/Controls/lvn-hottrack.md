---
title: LVN_HOTTRACK de notificação (Commctrl.h)
description: Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item. Esse código de notificação só é enviado por controles de exibição de lista que têm o estilo de exibição de lista estendido TRACKSELECT LVS \_ \_ EX. Ele é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab311b17f287b695a6b21d333f7183fdda272029e2c57dfe468527d765d1602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830427"
---
# <a name="lvn_hottrack-notification-code"></a>Código de notificação \_ LVN HOTTRACK

Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item. Esse código de notificação só é enviado por controles de exibição de lista que têm o estilo de exibição de lista estendido [**\_ \_ TRACKSELECT LVS**](extended-list-view-styles.md) EX. Ele é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contém informações sobre esse código de notificação. Os **membros iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item. O aplicativo receptor pode modificar o **membro iItem** para especificar o item que será selecionado. Se **iItem** for definido como -1, nenhum item será selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para permitir que a exibição de lista execute seu processamento de seleção de faixa normal. Se o aplicativo retornar não zero, o item não será selecionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





