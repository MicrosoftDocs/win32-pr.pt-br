---
title: Mensagem de MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Recupera o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ getFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- controles de Windows de mensagem de MCM_GETFIRSTDAYOFWEEK
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319646"
---
# <a name="mcm_getfirstdayofweek-message"></a>\_Mensagem MCM GETfirstdayofweek

Recupera o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ getFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **DWORD** que contém dois valores. A palavra alta é um valor **bool** que é diferente de zero se o primeiro dia da semana for definido como algo diferente de \_ IFIRSTDAYOFWEEK de localidade, caso contrário, zero. A palavra inferior é um valor inteiro que representa o primeiro dia da semana, em que 0 é segunda-feira, 1 é terça-feira e assim por diante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





