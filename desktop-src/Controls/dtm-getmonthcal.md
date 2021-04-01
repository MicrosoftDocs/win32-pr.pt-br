---
title: Mensagem de DTM_GETMONTHCAL (commctrl. h)
description: Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Controles de DTM_GETMONTHCAL de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918812"
---
# <a name="dtm_getmonthcal-message"></a>\_Mensagem DTM GETMONTHCAL

Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de calendário do mês filho de um controle DTP, se for bem-sucedido, caso contrário, será **nulo** .

## <a name="remarks"></a>Comentários

Os controles DTP criam um controle de calendário de mês filho quando o usuário clica na seta suspensa[( \_ notificação suspensa DTN](dtn-dropdown.md) ). Quando o calendário mensal não é mais necessário, ele é destruído (uma notificação [DTN \_ closeup](dtn-closeup.md) é enviada na destruição). Portanto, seu aplicativo não deve depender de um identificador estático para o calendário de mês filho do controle DTP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[DTN \_ closeup](dtn-closeup.md)
</dt> <dt>

[\_lista suspensa DTN](dtn-dropdown.md)
</dt> </dl>

 

 





