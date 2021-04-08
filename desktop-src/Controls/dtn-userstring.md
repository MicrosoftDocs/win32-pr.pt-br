---
title: DTN_USERSTRING código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando um usuário termina de editar uma cadeia de caracteres no controle.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824226"
---
# <a name="dtn_userstring-notification-code"></a>Código de notificação do DTN \_ userstring

Enviado por um controle do seletor de data e hora (DTP) quando um usuário termina de editar uma cadeia de caracteres no controle. Esse código de notificação é enviado somente por controles DTP que são definidos para o estilo [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) que contém informações sobre a instância do código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O proprietário do controle deve retornar zero.

## <a name="remarks"></a>Comentários

Manipular esse código de notificação permite que o proprietário forneça respostas personalizadas para cadeias de caracteres inseridas no controle pelo usuário. O proprietário deve estar preparado para analisar a cadeia de caracteres de entrada e tomar medidas, se necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) e **DTN \_ userstringa** (ANSI)<br/>             |



 

 





