---
title: TVN_GETDISPINFO de notificação (Commctrl.h)
description: Solicita que a janela pai de um controle de exibição de árvore forneça informações necessárias para exibir ou classificar um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59728c816ee3fe7dac46c12d7e62da6c18cfdad8387f03d3861e63792d9c8f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059906"
---
# <a name="tvn_getdispinfo-notification-code"></a>Código de \_ notificação TVN GETDISPINFO

Solicita que a janela pai de um controle de exibição de árvore forneça informações necessárias para exibir ou classificar um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) O **membro** do item é uma [**estrutura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujas **máscaras**, **hItem**, **estado** e **membros lParam** especificam o tipo de informação necessária. Você deve preencher os membros da estrutura com as informações apropriadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado nas seguintes circunstâncias:

-   Se o **membro pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor LPSTR TEXTCALLBACK, o controle enviará esse código de notificação para recuperar o \_ texto do item. Nesse caso, o membro **de máscara** de *lParam terá* o sinalizador TEXT TVIF \_ definido.
-   Se o membro **iImage** ou **iSelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I IMAGECALLBACK, o controle enviará esse código de notificação para recuperar o índice dos ícones de um item na lista de imagens do \_ controle. Nesse caso, se o item  for selecionado, o membro de máscara *de lParam* terá o sinalizador TVIF \_ SELECTEDIMAGE definido. Se o item não estiver selecionado, o membro **de máscara** *de lParam* terá o sinalizador IMAGE TVIF \_ definido.
-   Se o membro **cChildren** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I CHILDRENCALLBACK, o controle enviará esse código de notificação para recuperar um valor que indica se o item tem itens \_ filho. Nesse caso, o membro **de máscara** *de lParam terá* o sinalizador TVIF CHILDREN \_ definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





