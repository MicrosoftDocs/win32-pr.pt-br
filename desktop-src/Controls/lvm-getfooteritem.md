---
title: LVM_GETFOOTERITEM mensagem (Commctrl.h)
description: Obtém informações sobre um item de rodapé em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM controles de Windows mensagem
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
ms.openlocfilehash: c0b38bb8a91f93c456bd8096a3736eaec79e6c3472d0f18a133de482bb2c0328
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968276"
---
# <a name="lvm_getfooteritem-message"></a>Mensagem \_ GETFOOTERITEM LVM

Obtém informações sobre um item de rodapé em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ ListView GetFooterItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

O índice do item.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Um ponteiro para uma [**estrutura LV SENIORERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para receber um valor para os membros **state** e/ou **pszText** de acordo com o valor do **membro de** máscara. O processo de chamada é responsável por alocar essa estrutura e definir seus membros para indicar ao receptor quais informações retornar. Para obter mais informações, **consulte LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





