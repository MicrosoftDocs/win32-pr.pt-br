---
title: Mensagem de LVM_GETWORKAREAS (commctrl. h)
description: Recupera as áreas de trabalho de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetWorkAreas do ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- controles de Windows de mensagem de LVM_GETWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aed6173ef00860900d7690199cfb2c81535f088790290e30cc01898666bb068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968226"
---
# <a name="lvm_getworkareas-message"></a>\_Mensagem GETWORKAREAS LVM

Recupera as áreas de trabalho de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) na matriz em *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebem as áreas de trabalho atuais do controle de exibição de lista. Os valores nessas estruturas estão nas coordenadas do cliente. *wParam* especifica o número de estruturas nesta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

