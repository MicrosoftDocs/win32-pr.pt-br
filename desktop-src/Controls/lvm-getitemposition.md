---
title: Mensagem de LVM_GETITEMPOSITION (commctrl. h)
description: Recupera a posição de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemPosition do ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Controles de LVM_GETITEMPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824672"
---
# <a name="lvm_getitemposition-message"></a>\_Mensagem GETITEMPOSITION LVM

Recupera a posição de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemPosition do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe a posição do canto superior esquerdo do item, em coordenadas de exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

