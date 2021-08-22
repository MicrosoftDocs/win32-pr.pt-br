---
title: TVN_SETDISPINFO de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que ele deve atualizar as informações que mantém sobre um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957765"
---
# <a name="tvn_setdispinfo-notification-code"></a>Código de \_ notificação TVN SETDISPINFO

Notifica a janela pai de um controle de exibição de árvore de que ele deve atualizar as informações que mantém sobre um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que descreve o item que está sendo atualizado. O **membro hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica o  item que está sendo atualizado e o membro de máscara especifica quais atributos do item estão sendo atualizados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Se o **membro pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor LPSTR TEXTCALLBACK, o controle enviará essa notificação para definir o \_ texto do item. Nesse caso, o membro **de máscara** de *lParam terá* o sinalizador TEXT TVIF \_ definido.

Se o membro **iImage** ou **iSelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I IMAGECALLBACK, o controle enviará essa notificação para recuperar o índice da imagem de ícone a ser \_ exibida. Nesse caso, o membro **de máscara** *de lParam terá* o sinalizador TVIF IMAGE ou \_ TVIF \_ SELECTEDIMAGE definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**Tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





