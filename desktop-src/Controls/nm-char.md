---
title: NM_CHAR de notificação (Commctrl.h)
description: O código de notificação \_ CHAR NM é enviado por um controle quando uma chave de caractere é processada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR de notificação Windows controles
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018944"
---
# <a name="nm_char-notification-code"></a>Código de \_ notificação CHAR NM

O código de notificação \_ CHAR NM é enviado por um controle quando uma chave de caractere é processada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém informações adicionais sobre o caractere que causou o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado pela maioria dos controles. Para obter mais informações, consulte a documentação para os controles individuais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NM \_ CHAR (barra de ferramentas)](nm-char-toolbar.md)
</dt> </dl>

 

 





