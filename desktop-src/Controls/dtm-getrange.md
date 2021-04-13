---
title: Mensagem de DTM_GETRANGE (commctrl. h)
description: Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetRange de DateTime.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Controles de DTM_GETRANGE de mensagens do Windows
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
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455552"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que é uma combinação de GDTR \_ min ou GDTR \_ Max. O primeiro elemento da matriz [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contém o tempo mínimo permitido se GDTR \_ min estiver definido. O segundo elemento da matriz **SYSTEMTIME** contém o tempo máximo permitido se GDTR \_ Max estiver definido.

## <a name="remarks"></a>Comentários

O seletor de data e hora exibe apenas datas/horários que se enquadram no intervalo especificado, impedindo que o usuário selecione uma data e hora que esteja fora do intervalo. Se a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) especificar uma data e hora que esteja fora do intervalo, ela falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

