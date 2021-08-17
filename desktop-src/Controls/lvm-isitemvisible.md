---
title: Mensagem de LVM_ISITEMVISIBLE (commctrl. h)
description: Indica se um item no controle de exibição de lista está visível. Envie essa mensagem explicitamente ou usando a \_ macro IsItemVisible do ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- controles de Windows de mensagem de LVM_ISITEMVISIBLE
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958175"
---
# <a name="lvm_isitemvisible-message"></a>\_Mensagem ISITEMVISIBLE LVM

Indica se um item no controle de exibição de lista está visível. Envie essa mensagem explicitamente ou usando a macro [**\_ IsItemVisible do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um índice do item no controle de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se visível ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





