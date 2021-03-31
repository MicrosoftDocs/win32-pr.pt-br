---
title: Mensagem de MCM_SETTODAY (commctrl. h)
description: Define o \ 0034; hoje \ 0034; seleção de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ sethoje.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Controles de MCM_SETTODAY de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645228"
---
# <a name="mcm_settoday-message"></a>MCM \_ mensagem de hoje

Define a seleção "hoje" para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ sethoje**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a data a ser definida como a seleção "hoje" para o controle. Se esse parâmetro for definido como **NULL**, o controle retornará à configuração padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

Se a seleção "hoje" for definida como qualquer data diferente do padrão, as seguintes condições se aplicarão:

-   O controle não atualizará automaticamente a seleção "hoje" quando o tempo passar a meia-noite do dia atual.
-   O controle não atualizará automaticamente sua exibição com base nas alterações de localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

