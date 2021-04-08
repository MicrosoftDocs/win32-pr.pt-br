---
title: TVN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que os atributos de item foram alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED de código de notificação controles do Windows
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
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824448"
---
# <a name="tvn_itemchanged-notification-code"></a>Código de notificação TVN com \_ alterações

Notifica uma janela pai do controle de exibição de árvore que os atributos de item foram alterados. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que descreve o item que foi alterado. O membro **uChanged** é definido como TVIF \_ State.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** para aceitar a alteração ou **true** para evitar a alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN de \_ alteração](tvn-itemchanging.md)
</dt> </dl>

 

 





