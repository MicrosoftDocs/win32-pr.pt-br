---
title: MCN_SELECT de notificação (Commctrl.h)
description: Enviado por um controle de calendário de mês quando o usuário faz uma seleção de data explícita dentro de um controle de calendário de mês. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT de notificação Windows Controles
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018964"
---
# <a name="mcn_select-notification-code"></a>Código de \_ notificação MCN SELECT

Enviado por um controle de calendário de mês quando o usuário faz uma seleção de data explícita dentro de um controle de calendário de mês. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contém informações sobre o intervalo de datas selecionado no momento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O código de notificação **MCN \_ SELECT** é semelhante ao [**MCN \_ SELCHANGE**](mcn-selchange.md), mas **MCN \_ SELECT** é enviado somente em resposta às seleções de data explícitas de um usuário. **MCN \_ SELCHANGE** se aplica a qualquer alteração de seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





