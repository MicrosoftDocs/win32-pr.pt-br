---
title: LVN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED de código de notificação controles do Windows
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
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753574"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se um controle de exibição de lista tiver o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) e o usuário selecionar um intervalo de itens, mantendo pressionada a tecla Shift e clicando no mouse, os \_ códigos de notificação com alteração de LVN não serão enviados para cada item selecionado ou desmarcado. Em vez disso, você receberá um único código de notificação [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) , indicando que um intervalo de itens alterou o estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





