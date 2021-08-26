---
title: Mensagem de LVM_GETITEMPOSITION (commctrl. h)
description: Recupera a posição de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemPosition do ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- controles de Windows de mensagem de LVM_GETITEMPOSITION
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
ms.openlocfilehash: 92d4f4a55f88b6af9828420871de80117ae492bf53c8a62883e43f928c4f5c70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002616"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

