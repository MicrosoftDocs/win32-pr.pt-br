---
title: LVN_SETDISPINFO código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que ele deve atualizar as informações que ele mantém para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918801"
---
# <a name="lvn_setdispinfo-notification-code"></a>Código de notificação do LVN \_ SETDISPINFO

Notifica uma janela pai do controle de exibição de lista que ele deve atualizar as informações que ele mantém para um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que especifica informações para o item alterado. O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contém informações sobre o item que foi alterado. O membro **pszText** do **Item** contém um valor válido, independentemente de o sinalizador de \_ texto LVIF ser definido no membro **Mask** dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . O parâmetro *wParam* contém o código da mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





