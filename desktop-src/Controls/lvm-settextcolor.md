---
title: Mensagem de LVM_SETTEXTCOLOR (commctrl. h)
description: Define a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTextColor do ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Controles de LVM_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085401"
---
# <a name="lvm_settextcolor-message"></a>\_Mensagem SETTEXTCOLOR LVM

Define a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTextColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um [**COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor do texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

