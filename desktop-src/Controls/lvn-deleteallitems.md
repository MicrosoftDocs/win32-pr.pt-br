---
title: LVN_DELETEALLITEMS código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que todos os itens no controle estão prestes a ser excluídos. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS de código de notificação controles do Windows
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
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919245"
---
# <a name="lvn_deleteallitems-notification-code"></a>Código de notificação do LVN \_ DELETEALLITEMS

Notifica uma janela pai do controle de exibição de lista que todos os itens no controle estão prestes a ser excluídos. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . O membro **iItem** é-1 e os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para suprimir os códigos de notificação subsequentes do [LVN \_ DELETEITEM](lvn-deleteitem.md) , retorne **true**.

Para receber códigos de notificação [LVN \_ DELETEITEM](lvn-deleteitem.md) subsequentes, retorne **false**.

## <a name="remarks"></a>Comentários

Um controle de exibição de lista envia o código de notificação do [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) quando ele é destruído ou recebe a mensagem do **LVM \_ DELETEALLITEMS** . Se o **LVM \_ DELETEALLITEMS** não retornar **true**, o controle também enviará um código de notificação [LVN \_ DELETEITEM](lvn-deleteitem.md) , pois cada item será excluído.

Se o manipulador de mensagens [**\_ DELETEALLITEMS do LVM**](lvm-deleteallitems.md) estiver em um procedimento da caixa de diálogo, retorne **verdadeiro** do procedimento da caixa de diálogo e use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT para definir o valor de retorno da mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

