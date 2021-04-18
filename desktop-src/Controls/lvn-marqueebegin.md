---
title: LVN_MARQUEEBEGIN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma seleção de caixa delimitadora (letreiro) foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756236"
---
# <a name="lvn_marqueebegin-notification-code"></a>Código de notificação do LVN \_ MARQUEEBEGIN

Notifica uma janela pai do controle de exibição de lista que uma seleção de caixa delimitadora (letreiro) foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para aceitar o código de notificação, retorne zero. Para encerrar a seleção da caixa delimitadora, retorne diferente de zero.

## <a name="remarks"></a>Comentários

Uma *seleção de caixa delimitadora* é o processo de clicar na área do cliente da janela de exibição de lista e arrastar para selecionar vários itens simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





