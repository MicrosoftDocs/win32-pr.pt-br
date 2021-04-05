---
title: Mensagem de MCM_GETSELRANGE (commctrl. h)
description: Recupera informações de data que representam os limites superior e inferior do intervalo de datas selecionado no momento pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Controles de MCM_GETSELRANGE de mensagens do Windows
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
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918272"
---
# <a name="mcm_getselrange-message"></a>\_Mensagem MCM GETSELRANGE

Recupera informações de data que representam os limites superior e inferior do intervalo de datas selecionado no momento pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá os limites inferior e superior da seleção do usuário. Os limites inferior e superior são colocados em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] , respectivamente. Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. **MCM \_ GETSELRANGE** falhará se for aplicado a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

