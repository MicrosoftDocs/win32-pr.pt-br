---
title: LVN_ENDLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754375"
---
# <a name="lvn_endlabeledit-notification-code"></a>Código de notificação do LVN \_ ENDLABELEDIT

Notifica uma janela pai do controle de exibição de lista sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item que está sendo editado. O membro **pszText** do **Item** contém um valor válido quando o \_ código de notificação ENDLABELEDIT de LVN é enviado, independentemente de o \_ sinalizador de texto LVIF ser definido no membro **Mask** da estrutura **LVITEM** . Se o usuário cancelar a edição, o membro **pszText** da estrutura **LVITEM** será **nulo**; caso contrário, **pszText** será o endereço do texto editado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) for não **nulo**, retornará **true** para definir o rótulo do item como o texto editado. Retorne **false** para rejeitar o texto editado e reverter para o rótulo original.

Se o membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) for **nulo**, o valor de retorno será ignorado.

## <a name="remarks"></a>Comentários

O valor de retorno do procedimento da caixa de diálogo é se a mensagem foi tratada. O segundo valor de retorno deve ser definido chamando [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) com **DWLP_MSGRESULT**.

Quando o usuário começa a editar um rótulo de item, a janela pai do controle List-View recebe um código de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Quando o usuário cancela ou conclui a edição, a janela pai recebe um \_ código de notificação LVN ENDLABELEDIT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) e **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





