---
title: Mensagem de LVM_ISITEMVISIBLE (commctrl. h)
description: Indica se um item no controle de exibição de lista está visível. Envie essa mensagem explicitamente ou usando a \_ macro IsItemVisible do ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Controles de LVM_ISITEMVISIBLE de mensagens do Windows
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
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824662"
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

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se visível ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





