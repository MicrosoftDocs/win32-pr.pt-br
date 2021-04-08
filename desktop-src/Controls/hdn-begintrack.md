---
title: HDN_BEGINTRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está sobre um divisor no controle de cabeçalho).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK de código de notificação controles do Windows
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
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086557"
---
# <a name="hdn_begintrack-notification-code"></a>Código de notificação do HDN \_ BEGINTRACK

Notifica uma janela pai do controle de cabeçalho que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está sobre um divisor no controle de cabeçalho). Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor deve ser arrastado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** para permitir o acompanhamento do divisor ou **true** para impedir o acompanhamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) e **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





