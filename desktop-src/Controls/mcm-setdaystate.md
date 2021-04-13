---
title: Mensagem de MCM_SETDAYSTATE (commctrl. h)
description: Define os Estados de dia para todos os meses que estão visíveis no momento dentro de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Controles de MCM_SETDAYSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455893"
---
# <a name="mcm_setdaystate-message"></a>\_Mensagem MCM SETDAYSTATE

Define os Estados de dia para todos os meses que estão visíveis no momento dentro de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor indicando quantos elementos estão na matriz para a qual *lParam* aponta.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de valores [**MONTHDAYSTATE**](monthdaystate.md) que definem como o controle de calendário mensal será desenhado todos os dias em sua exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Um aplicativo pode definir explicitamente as informações de estado do dia enviando essa mensagem, mas o estado não será mantido quando uma parte diferente do calendário for rolada para a exibição. As informações de estado de dia geralmente são definidas em resposta ao código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que é enviado sempre que o controle precisa ser atualizado.

A matriz em *lParam* deve conter quantos elementos forem retornados pelo valor retornado pela macro a seguir:

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Tenha em mente que a matriz em *lParam* deve conter valores [**MONTHDAYSTATE**](monthdaystate.md) que correspondam a todos os meses atualmente na exibição do controle, em ordem cronológica. Isso inclui os dois meses que podem ser exibidos parcialmente antes do primeiro mês e após o último mês.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando controles de calendário de mês](using-month-calendar-controls.md)
</dt> </dl>

 

 





