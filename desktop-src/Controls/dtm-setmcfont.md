---
title: DTM_SETMCFONT mensagem (Commctrl.h)
description: Define a fonte a ser usada pelo controle de calendário de mês filho do DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a macro DateTime \_ SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT controles de Windows mensagem
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877806"
---
# <a name="dtm_setmcfont-message"></a>Mensagem DTM \_ SETMCFONT

Define a fonte a ser usada pelo controle de calendário de mês filho do DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a [**macro DateTime \_ SetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a fonte que será definida.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte. Definir esse parâmetro como **TRUE** faz com que o controle redesenhar a si mesmo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





