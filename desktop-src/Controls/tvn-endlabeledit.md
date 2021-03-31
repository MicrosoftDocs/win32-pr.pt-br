---
title: TVN_ENDLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085629"
---
# <a name="tvn_endlabeledit-notification-code"></a>Código de notificação do TVN \_ ENDLABELEDIT

Notifica uma janela pai do controle de exibição de árvore sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . O membro **Item** dessa estrutura é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **hItem**, **lParam** e **pszText** contêm informações válidas sobre o item que foi editado. Se a edição do rótulo foi cancelada, o membro **pszText** da estrutura **TVITEM** é **nulo**; caso contrário, **pszText** será o endereço do texto editado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o membro **pszText** for não **nulo**, retornará **true** para definir o rótulo do item como o texto editado. Retorne **false** para rejeitar o texto editado e reverter para o rótulo original.

## <a name="remarks"></a>Comentários

Se o membro **pszText** for **nulo**, o valor de retorno será ignorado.

Se você especificou o \_ valor de **pszText** de texto de LPSTR para este item e o membro de messagecast não for **nulo**, o \_ manipulador de ENDLABELEDIT TVN deverá copiar o texto de **pszText** para o armazenamento local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





