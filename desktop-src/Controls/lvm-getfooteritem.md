---
title: Mensagem de LVM_GETFOOTERITEM (commctrl. h)
description: Obtém informações sobre um item de rodapé em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterItem do ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Controles de LVM_GETFOOTERITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008860"
---
# <a name="lvm_getfooteritem-message"></a>\_Mensagem GETFOOTERITEM LVM

Obtém informações sobre um item de rodapé em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice do item.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para receber um valor para os membros **State** e/ou **pszText** de acordo com o valor do membro **Mask** . O processo de chamada é responsável por alocar essa estrutura e definir seus membros para indicar ao destinatário quais informações retornar. Para obter mais informações, consulte **LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





