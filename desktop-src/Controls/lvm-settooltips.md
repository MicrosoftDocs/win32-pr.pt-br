---
title: Mensagem de LVM_SETTOOLTIPS (commctrl. h)
description: Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Controles de LVM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454932"
---
# <a name="lvm_settooltips-message"></a>Mensagem do LVM \_ SETtooltips

Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a macro [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador para o controle de dica de ferramenta a ser definido.</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle ToolTip anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ GETtooltips**](lvm-gettooltips.md)
</dt> </dl>

 

 





