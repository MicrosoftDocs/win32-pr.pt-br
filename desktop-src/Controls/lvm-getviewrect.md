---
title: Mensagem de LVM_GETVIEWRECT (commctrl. h)
description: Recupera o retângulo delimitador de todos os itens no controle de exibição de lista. O modo de exibição de lista deve estar no ícone ou no modo de exibição de ícone pequeno. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetViewRect do ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Controles de LVM_GETVIEWRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009646"
---
# <a name="lvm_getviewrect-message"></a>\_Mensagem GETVIEWRECT LVM

Recupera o retângulo delimitador de todos os itens no controle de exibição de lista. O modo de exibição de lista deve estar no ícone ou no modo de exibição de ícone pequeno. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetViewRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador. Todas as coordenadas são relativas à área visível do controle de exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

