---
title: Mensagem de LVM_SETBKCOLOR (commctrl. h)
description: Define a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetBkColor do ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Controles de LVM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918701"
---
# <a name="lvm_setbkcolor-message"></a>\_Mensagem SETBKCOLOR LVM

Define a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Cor do plano de fundo para definir ou o \_ valor de nenhum CLR para nenhuma cor de plano de fundo. Os controles de exibição de lista com cores de plano de fundo redesenham-se significativamente mais rápido do que aqueles sem cores de plano

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





