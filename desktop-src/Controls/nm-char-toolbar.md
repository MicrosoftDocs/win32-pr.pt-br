---
title: Código de notificação de NM_CHAR (barra de ferramentas) (commctrl. h)
description: Enviado por uma barra de ferramentas quando recebe uma \_ mensagem do WM Char. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Código de notificação de NM_CHAR (barra de ferramentas) controles do Windows
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
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824856"
---
# <a name="nm_char-toolbar-notification-code"></a>\_Código de notificação de caracteres nm (barra de ferramentas)

Enviado por uma barra de ferramentas quando recebe uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém informações adicionais sobre o caractere que causou o código de notificação. O membro **dwItemPrev** dessa estrutura contém o identificador de comando do item que é atualmente quente ou-1 se nenhum item está quente no momento. O membro **dwItemNext** dessa estrutura contém o identificador de comando do item que se tornará quente ou-1 se a chave não corresponder ao acelerador de qualquer item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** para indicar que a barra de ferramentas não deve processar o caractere e **false** para que a barra de ferramentas processe o caractere.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

