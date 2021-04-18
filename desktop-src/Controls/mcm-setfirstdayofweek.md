---
title: Mensagem de MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Define o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ setFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Controles de MCM_SETFIRSTDAYOFWEEK de mensagens do Windows
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
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756425"
---
# <a name="mcm_setfirstdayofweek-message"></a>\_Mensagem MCM SETfirstdayofweek

Define o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ setFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que representa qual dia deve ser definido como o primeiro dia da semana, em que 0 é segunda-feira, 1 é terça-feira e assim por diante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém dois valores. A palavra alta é um valor **bool** que será diferente de zero se o primeiro dia da semana anterior não for igual a IFIRSTDAYOFWEEK de localidade \_ nem nenhum outro. A palavra inferior é um valor inteiro que representa o primeiro dia da semana anterior.

## <a name="remarks"></a>Comentários

Se o primeiro dia da semana for definido como algo diferente do padrão (localidade \_ IFIRSTDAYOFWEEK), o controle não atualizará automaticamente as alterações do primeiro dia da semana com base nas alterações de localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





