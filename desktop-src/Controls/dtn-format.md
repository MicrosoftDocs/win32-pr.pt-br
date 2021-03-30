---
title: DTN_FORMAT código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) para solicitar que o texto seja exibido em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455452"
---
# <a name="dtn_format-notification-code"></a>\_Código de notificação do formato DTN

Enviado por um controle do seletor de data e hora (DTP) para solicitar que o texto seja exibido em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) que contém informações sobre esta instância do código de notificação. A estrutura contém a subcadeia de caracteres que define o campo de retorno de chamada e recebe a cadeia de caracteres formatada que o controle exibirá.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O proprietário do controle deve retornar zero.

## <a name="remarks"></a>Comentários

Manipular esse código de notificação permite que o proprietário do controle forneça uma cadeia de caracteres personalizada que o controle exibirá. (Para obter informações adicionais sobre campos de retorno de chamada, consulte [campos de retorno de chamada](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTN \_ FORMATW** (Unicode) e **DTN \_ formata** (ANSI)<br/>                     |



 

 





