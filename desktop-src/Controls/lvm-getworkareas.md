---
title: Mensagem de LVM_GETWORKAREAS (commctrl. h)
description: Recupera as áreas de trabalho de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetWorkAreas do ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Controles de LVM_GETWORKAREAS de mensagens do Windows
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
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455742"
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

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

