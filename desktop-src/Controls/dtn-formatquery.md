---
title: DTN_FORMATQUERY de notificação (Commctrl.h)
description: Enviado por um controle DTP (selador de data e hora) para recuperar o tamanho máximo permitida da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY código de notificação Windows Controles
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14bd1a9efe22251aba71f157dfb2a68e2b0a70385c30564bb7f08e420e0c0cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019984"
---
# <a name="dtn_formatquery-notification-code"></a>Código de notificação \_ DTN FORMATQUERY

Enviado por um controle DTP (selador de data e hora) para recuperar o tamanho máximo permitida da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) que contém informações sobre o campo de retorno de chamada. A estrutura contém uma substring que define um campo de retorno de chamada e recebe o tamanho máximo permitida da cadeia de caracteres que será exibida no campo de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O proprietário do controle deve calcular a largura máxima possível do texto que será exibido no campo de retorno de chamada, definir o membro **szMax** da estrutura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e retornar zero.

## <a name="remarks"></a>Comentários

Lidar com esse código de notificação prepara o controle para ajustar o tamanho máximo da cadeia de caracteres que será exibida em um campo de retorno de chamada específico. Isso permite que o controle exibe corretamente a saída em todos os momentos, reduzindo a cintilação dentro da exibição do controle. (Para obter informações adicionais sobre campos de retorno de chamada, consulte [Campos de retorno de chamada](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





