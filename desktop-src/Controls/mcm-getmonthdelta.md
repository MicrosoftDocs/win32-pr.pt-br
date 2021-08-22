---
title: Mensagem de MCM_GETMONTHDELTA (commctrl. h)
description: Recupera a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- controles de Windows de mensagem de MCM_GETMONTHDELTA
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319606"
---
# <a name="mcm_getmonthdelta-message"></a>\_Mensagem MCM GETMONTHDELTA

Recupera a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o Delta de mês tiver sido definido anteriormente usando a mensagem [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , retornará um valor int que representa a taxa de rolagem atual do calendário do mês. Se o Delta de mês não tiver sido definido anteriormente usando a mensagem **MCM \_ SETMONTHDELTA** ou se o Delta de mês tiver sido redefinido para o padrão, retornará um valor int que representa o número atual de meses visíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





