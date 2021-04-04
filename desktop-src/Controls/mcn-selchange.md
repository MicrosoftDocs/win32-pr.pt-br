---
title: MCN_SELCHANGE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando a data ou o intervalo de datas selecionado atualmente é alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009000"
---
# <a name="mcn_selchange-notification-code"></a>Código de notificação do MCN \_ SELCHANGE

Enviado por um controle de calendário mensal quando a data ou o intervalo de datas selecionado atualmente é alterado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contém informações sobre o intervalo de datas selecionado no momento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Por exemplo, o controle envia MCN \_ SELCHANGE quando o usuário altera explicitamente a seleção dentro do mês atual ou quando a seleção é implicitamente alterada em resposta à navegação do mês seguinte/anterior. Esse código de notificação também é enviado pelo sistema em intervalos regulares para que o controle possa responder às alterações de data.

Esse código de notificação é semelhante a [MCN \_ Select](mcn-select.md), mas é enviado em resposta a qualquer alteração de seleção. MCN \_ Select é enviado somente para uma seleção de data explícita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





