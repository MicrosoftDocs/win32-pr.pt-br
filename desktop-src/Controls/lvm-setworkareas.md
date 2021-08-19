---
title: LVM_SETWORKAREAS mensagem (Commctrl.h)
description: Define as áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetWorkAreas.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS controles Windows mensagem
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
ms.openlocfilehash: 8f1060377fd9aec9014d18d206444355b052f4aafb796403e3e47fa92a0a7aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830657"
---
# <a name="lvm_setworkareas-message"></a>Mensagem LVM \_ SETWORKAREAS

Define as áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView SetWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de estruturas na matriz em *lprc*. O número máximo de áreas de trabalho permitidas é definido pelo valor LV \_ MAX \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de [**estruturas RECT**](/previous-versions//dd162897(v=vs.85)) que contêm as novas áreas de trabalho do controle de exibição de lista. Os valores nessas estruturas estão nas coordenadas do cliente. Se esse parâmetro for **NULL,** a área de trabalho será definida como a área de cliente do controle . *wParam* especifica o número de estruturas nessa matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando List-View controles](using-list-view-controls.md)
</dt> </dl>

 

