---
title: TTN_SHOW código de notificação (commctrl. h)
description: Notifica a janela do proprietário que um controle ToolTip está prestes a ser exibido. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW código de notificação Windows controles
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408808"
---
# <a name="ttn_show-notification-code"></a>TTN \_ Mostrar código de notificação

Notifica a janela do proprietário que um controle ToolTip está prestes a ser exibido. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

[Versão 4,70](common-control-versions.md). Para exibir a dica de ferramenta em seu local padrão, retorne zero. Para personalizar a posição da dica de ferramenta, reposicione a janela de dica de ferramenta com a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) e retorne **true**.

> [!Note]  
> Para versões anteriores a 4,70, não há nenhum valor de retorno.

 

## <a name="remarks"></a>Comentários

Um retângulo de janela de dica de ferramenta é um pouco maior do que seu retângulo de exibição de texto, e sua origem é deslocada para cima e para a esquerda. Se você precisar posicionar com precisão o retângulo de exibição de texto de uma dica de ferramenta, a mensagem [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) converterá um retângulo de exibição de texto no retângulo da janela de dica de ferramenta correspondente e vice-versa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

