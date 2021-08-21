---
title: LVN_DELETEALLITEMS de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que todos os itens no controle estão prestes a ser excluídos. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f76ec4deaf67c1448fab5054c05ea8ede79c0972061c8be8e4f36b2e40ef54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019124"
---
# <a name="lvn_deleteallitems-notification-code"></a>Código de notificação LVN \_ DELETEALLITEMS

Notifica a janela pai de um controle de exibição de lista de que todos os itens no controle estão prestes a ser excluídos. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) O **membro iItem** é -1 e os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para suprimir os códigos [de notificação \_ LVN DELETEITEM](lvn-deleteitem.md) subsequentes, retorne **TRUE.**

Para receber os códigos [de notificação \_ LVN DELETEITEM](lvn-deleteitem.md) subsequentes, retorne **FALSE.**

## <a name="remarks"></a>Comentários

Um controle de exibição de lista envia o código de notificação [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) quando ele é destruído ou quando recebe a mensagem **LVM \_ DELETEALLITEMS.** Se **LVM \_ DELETEALLITEMS** não retornar **TRUE,** o controle também enviará um código de notificação [LVN \_ DELETEITEM](lvn-deleteitem.md) à medida que cada item for excluído.

Se o manipulador de mensagens [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) estiver em um procedimento de caixa de diálogo, retorne **TRUE** do procedimento da caixa de diálogo e use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL MSGRESULT para definir o valor de retorno da \_ mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

