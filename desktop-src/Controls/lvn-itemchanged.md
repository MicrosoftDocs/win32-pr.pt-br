---
title: LVN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED código de notificação Windows controles
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea129a1b62b442b0fb545f29a57e9eab0d6d1bae057996df5bc269d9a4296d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830380"
---
# <a name="lvn_itemchanged-notification-code"></a>Código de notificação LVN com \_ alterações

Notifica uma janela pai do controle de exibição de lista que um item foi alterado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica o item e especifica quais dos seus atributos foram alterados. Se o membro **iItem** da estrutura apontada por *lParam* for-1, a alteração será aplicada a todos os itens na exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se um controle de exibição de lista tiver o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) e o usuário selecionar um intervalo de itens, mantendo pressionada a tecla Shift e clicando no mouse, os \_ códigos de notificação com alteração de LVN não serão enviados para cada item selecionado ou desmarcado. Em vez disso, você receberá um único código de notificação [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) , indicando que um intervalo de itens alterou o estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





