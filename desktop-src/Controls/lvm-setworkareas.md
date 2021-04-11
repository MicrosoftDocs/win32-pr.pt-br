---
title: Mensagem de LVM_SETWORKAREAS (commctrl. h)
description: Define as áreas de trabalho dentro de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetWorkAreas do ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Controles de LVM_SETWORKAREAS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918960"
---
# <a name="lvm_setworkareas-message"></a>\_Mensagem SETWORKAREAS LVM

Define as áreas de trabalho dentro de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de estruturas na matriz em *lprc*. O número máximo de áreas de trabalho permitidas é definido pelo \_ valor de WORKAREAS Max LV \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que contêm as novas áreas de trabalho do controle de exibição de lista. Os valores nessas estruturas estão nas coordenadas do cliente. Se esse parâmetro for **NULL**, a área de trabalho será definida como a área do cliente do controle. *wParam* especifica o número de estruturas nesta matriz.

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

 

