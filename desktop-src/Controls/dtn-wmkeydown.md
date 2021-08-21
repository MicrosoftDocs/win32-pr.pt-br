---
title: DTN_WMKEYDOWN código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando o usuário digita em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN código de notificação Windows controles
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf822cc5eb8d1d8bdeca6b0853766774105af07cda77f55743d60d0fb12cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019974"
---
# <a name="dtn_wmkeydown-notification-code"></a>Código de notificação do DTN \_ WMKEYDOWN

Enviado por um controle do seletor de data e hora (DTP) quando o usuário digita em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) que contém informações sobre esta instância do código de notificação. A estrutura inclui informações sobre a chave que o usuário digitou, a subcadeia de caracteres que define o campo de retorno de chamada e a data e hora atuais do sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O proprietário do controle deve retornar zero.

## <a name="remarks"></a>Comentários

Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) e **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





