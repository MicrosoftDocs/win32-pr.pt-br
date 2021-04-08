---
title: MCN_SELECT código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando o usuário faz uma seleção de data explícita dentro de um controle de calendário mensal. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT de código de notificação controles do Windows
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
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008999"
---
# <a name="mcn_select-notification-code"></a>MCN \_ selecionar código de notificação

Enviado por um controle de calendário mensal quando o usuário faz uma seleção de data explícita dentro de um controle de calendário mensal. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
MCN_SELECT

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

O código de notificação **MCN \_ Select** é semelhante a [**MCN \_ SELCHANGE**](mcn-selchange.md), mas **MCN \_ Select** é enviada somente em resposta às seleções de data explícitas de um usuário. **MCN \_ SELCHANGE** aplica-se a qualquer alteração de seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





