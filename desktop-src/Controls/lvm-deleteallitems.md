---
title: Mensagem de LVM_DELETEALLITEMS (commctrl. h)
description: Remove todos os itens de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteAllItems do ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Controles de LVM_DELETEALLITEMS de mensagens do Windows
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
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454641"
---
# <a name="lvm_deleteallitems-message"></a>\_Mensagem DELETEALLITEMS LVM

Remove todos os itens de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ DeleteAllItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Quando um controle de exibição de lista recebe a mensagem **\_ DELETEALLITEMS LVM** , ele envia o código de notificação [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) para sua janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





