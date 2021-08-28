---
title: TVN_ITEMCHANGED de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que os atributos de item foram alterados. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018644"
---
# <a name="tvn_itemchanged-notification-code"></a>Código de notificação DE TVN \_ ITEMCHANGED

Notifica a janela pai de um controle de exibição de árvore de que os atributos de item foram alterados. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que descreve o item que foi alterado. O **membro uChanged** é definido como TVIF \_ STATE.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **FALSE** para aceitar a alteração ou **TRUE** para evitar a alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 





