---
title: MCM_GETSELRANGE mensagem (Commctrl.h)
description: Recupera informações de data que representam os limites superior e inferior do intervalo de datas atualmente selecionado pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE controles Windows mensagem
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7c446c98a43714a8cd839704050d2aedd1b7eab83b9199700ba24dd4e2be98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061946"
---
# <a name="mcm_getselrange-message"></a>Mensagem MCM \_ GETSELRANGE

Recupera informações de data que representam os limites superior e inferior do intervalo de datas atualmente selecionado pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal GetSelRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá os limites inferior e superior da seleção do usuário. Os limites inferior e superior são colocados em *lprgSysTimeArray* 0 e \[ \] *lprgSysTimeArray* \[ \] 1, respectivamente. Esse parâmetro deve ser um endereço válido e não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário. **MCM \_ GETSELRANGE** falhará se aplicado a um controle de calendário de mês que não usa o estilo [**\_ MCS MULTISELECT.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Horas no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

