---
title: MCM_SETFIRSTDAYOFWEEK mensagem (Commctrl.h)
description: Define o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK controles de Windows mensagem
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077106"
---
# <a name="mcm_setfirstdayofweek-message"></a>Mensagem MCM \_ SETFIRSTDAYOFWEEK

Define o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal SetFirstDayOfWeek.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que representa qual dia deve ser definido como o primeiro dia da semana, em que 0 é segunda-feira, 1 é terça-feira e assim por diante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor DWORD** que contém dois valores. A palavra alta será um **valor BOOL** diferente de zero se o primeiro dia anterior da semana não for igual a LOCALE \_ IFIRSTDAYOFWEEK ou zero caso contrário. A palavra baixa é um valor INT que representa o primeiro dia anterior da semana.

## <a name="remarks"></a>Comentários

Se o primeiro dia da semana for definido como algo diferente do padrão (LOCALE IFIRSTDAYOFWEEK), o controle não atualizará automaticamente as alterações do primeiro dia da semana com base nas alterações de \_ localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





