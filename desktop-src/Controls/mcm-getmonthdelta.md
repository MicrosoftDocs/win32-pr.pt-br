---
title: Mensagem de MCM_GETMONTHDELTA (commctrl. h)
description: Recupera a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Controles de MCM_GETMONTHDELTA de mensagens do Windows
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
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086549"
---
# <a name="mcm_getmonthdelta-message"></a>\_Mensagem MCM GETMONTHDELTA

Recupera a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o Delta de mês tiver sido definido anteriormente usando a mensagem [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , retornará um valor int que representa a taxa de rolagem atual do calendário do mês. Se o Delta de mês não tiver sido definido anteriormente usando a mensagem **MCM \_ SETMONTHDELTA** ou se o Delta de mês tiver sido redefinido para o padrão, retornará um valor int que representa o número atual de meses visíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





