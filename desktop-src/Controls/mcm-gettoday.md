---
title: MCM_GETTODAY mensagem (Commctrl.h)
description: Recupera as informações de data para a data especificada como \ 0034;today \ 0034; para um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY controles Windows mensagem
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6925ff24a2d3e042a4f2c752d87642f74345116fc5cc7f94e00e811d453be4fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019024"
---
# <a name="mcm_gettoday-message"></a>Mensagem \_ GETTODAY do MCM

Recupera as informações de data para a data especificada como "hoje" para um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal GetToday.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de data. Esse parâmetro deve ser um endereço válido e não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

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

 

