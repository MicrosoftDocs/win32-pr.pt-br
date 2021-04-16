---
title: NM_CHAR código de notificação (commctrl. h)
description: O código de notificação do NM \_ Char é enviado por um controle quando uma chave de caractere é processada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR de código de notificação controles do Windows
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
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750309"
---
# <a name="nm_char-notification-code"></a>Código de notificação do NM \_ Char

O código de notificação do NM \_ Char é enviado por um controle quando uma chave de caractere é processada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém informações adicionais sobre o caractere que causou o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado pela maioria dos controles. Para obter mais informações, consulte a documentação para os controles individuais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NM \_ Char (barra de ferramentas)](nm-char-toolbar.md)
</dt> </dl>

 

 





