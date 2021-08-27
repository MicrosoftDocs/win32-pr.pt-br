---
title: TVN_BEGINLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT código de notificação Windows controles
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8fdd2b75ee9f3dcc46e5449c275eeea141162f3d31f524b64e114a623bd915e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060086"
---
# <a name="tvn_beginlabeledit-notification-code"></a>Código de notificação do TVN \_ BEGINLABELEDIT

Notifica uma janela pai do controle de exibição de árvore sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . O membro **Item** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item que está sendo editado nos membros **hItem**, **State**, **lParam** e **pszText** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** para cancelar a edição do rótulo.

## <a name="remarks"></a>Comentários

Quando o rótulo é iniciado, um controle de edição é criado, mas não posicionado ou exibido. Antes de ser exibida, o controle de exibição de árvore envia a janela pai um \_ código de notificação TVN BEGINLABELEDIT.

Para personalizar a edição de rótulo, implemente um manipulador para TVN \_ BEGINLABELEDIT e envie uma mensagem [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) para o controle de exibição em árvore. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em \_ xxx.

Quando o usuário cancela ou conclui a edição, a janela pai recebe um código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) e **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





