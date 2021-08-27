---
title: LVM_DELETEALLITEMS mensagem (Commctrl.h)
description: Remove todos os itens de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteAllItems de ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958404"
---
# <a name="lvm_deleteallitems-message"></a>Mensagem LVM \_ DELETEALLITEMS

Remove todos os itens de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ DeleteAllItems de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Quando um controle de exibição de lista recebe a mensagem **LVM \_ DELETEALLITEMS,** ele envia o código de notificação [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) para sua janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





