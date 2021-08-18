---
title: Código de notificação do NM_NCHITTEST (rebar) (commctrl. h)
description: Código de notificação de NM_NCHITTEST (rebar) – enviado por um controle rebar quando o controle recebe uma mensagem de NCHITTEST do WM \_ . Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Windows controles de código de notificação NM_NCHITTEST (rebar)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5831ca9dbeda35c7757613cae1d31db921aa80f4b749d4c9407339a2531abcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410697"
---
# <a name="nm_nchittest-rebar-notification-code"></a>\_Código de notificação do NCHITTEST nm (rebar)

Enviado por um controle rebar quando o controle recebe uma mensagem de [**\_ NCHITTEST do WM**](/windows/desktop/inputdev/wm-nchittest) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre o código de notificação. O membro **dwItemSpec** contém o índice de banda sobre o qual ocorreu a mensagem de teste de ocorrência e o membro **pt** contém as coordenadas do mouse da mensagem de teste de clique.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para permitir que o rebar execute o processamento padrão da mensagem de teste de clique ou retorne um dos valores de HT \* documentados em [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para substituir o processamento de teste de clique padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

