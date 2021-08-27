---
title: LVN_MARQUEEBEGIN de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que uma seleção de caixa delimitada (letreiro) foi iniciada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN código de notificação Windows Controles
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
ms.openlocfilehash: d8012981883564450603d11d0eb243375f48b46cdb14a14984a19415c84dab3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109526"
---
# <a name="lvn_marqueebegin-notification-code"></a>Código de notificação LVN \_ MARQUEEBEGIN

Notifica a janela pai de um controle de exibição de lista de que uma seleção de caixa delimitada (letreiro) foi iniciada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para aceitar o código de notificação, retorne zero. Para encerrar a seleção da caixa delimitador, retorne um valor que não seja zero.

## <a name="remarks"></a>Comentários

Uma *seleção de caixa delimitada* é o processo de clicar na área de cliente da janela de exibição de lista e arrastar para selecionar vários itens simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





