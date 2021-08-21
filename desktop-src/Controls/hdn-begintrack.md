---
title: HDN_BEGINTRACK de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de header de que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está em um divisor no controle de header).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4250f178c4e1e2322e1609159eabd2fbd99611c10420bb90ce7bd287c44a5d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170936"
---
# <a name="hdn_begintrack-notification-code"></a>Código de \_ notificação DO HDN BEGINTRACK

Notifica a janela pai de um controle de header de que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está em um divisor no controle de header). Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeça e o item cujo divisor deve ser arrastado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **FALSE** para permitir o acompanhamento do divisor ou **TRUE para** impedir o acompanhamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) e **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





