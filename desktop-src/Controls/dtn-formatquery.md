---
title: DTN_FORMATQUERY código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) para recuperar o tamanho máximo permitido da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY de código de notificação controles do Windows
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
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918037"
---
# <a name="dtn_formatquery-notification-code"></a>Código de notificação do DTN \_ FORMATQUERY

Enviado por um controle do seletor de data e hora (DTP) para recuperar o tamanho máximo permitido da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) que contém informações sobre o campo de retorno de chamada. A estrutura contém uma subcadeia de caracteres que define um campo de retorno de chamada e recebe o tamanho máximo permitido da cadeia de caracteres que será exibida no campo de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O proprietário do controle deve calcular a largura máxima possível do texto que será exibido no campo de retorno de chamada, definir o membro **szMax** da estrutura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e retornar zero.

## <a name="remarks"></a>Comentários

Manipular esse código de notificação prepara o controle para ajustar o tamanho máximo da cadeia de caracteres que será exibida em um campo de retorno de chamada específico. Isso permite que o controle exiba corretamente a saída em todos os momentos, reduzindo a cintilação dentro da exibição do controle. (Para obter informações adicionais sobre campos de retorno de chamada, consulte [campos de retorno de chamada](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





