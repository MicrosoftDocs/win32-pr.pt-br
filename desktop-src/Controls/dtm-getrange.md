---
title: Mensagem de DTM_GETRANGE (commctrl. h)
description: Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetRange de DateTime.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- controles de Windows de mensagem de DTM_GETRANGE
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877946"
---
# <a name="dtm_getrange-message"></a>DTM \_ mensagem GETrange

Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetRange de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **DWORD** que é uma combinação de GDTR \_ min ou GDTR \_ Max. O primeiro elemento da matriz [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contém o tempo mínimo permitido se GDTR \_ min estiver definido. O segundo elemento da matriz **SYSTEMTIME** contém o tempo máximo permitido se GDTR \_ Max estiver definido.

## <a name="remarks"></a>Comentários

O seletor de data e hora exibe apenas datas/horários que se enquadram no intervalo especificado, impedindo que o usuário selecione uma data e hora que esteja fora do intervalo. Se a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) especificar uma data e hora que esteja fora do intervalo, ela falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

