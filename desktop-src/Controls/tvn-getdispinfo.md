---
title: TVN_GETDISPINFO código de notificação (commctrl. h)
description: Solicita que uma janela pai do controle de exibição de árvore forneça as informações necessárias para exibir ou classificar um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO de código de notificação controles do Windows
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
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499391"
---
# <a name="tvn_getdispinfo-notification-code"></a>Código de notificação do TVN \_ GETDISPINFO

Solicita que uma janela pai do controle de exibição de árvore forneça as informações necessárias para exibir ou classificar um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . O **membro item** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **Mask**, **hItem**, **State** e **lParam** especificam o tipo de informações necessárias. Você deve preencher os membros da estrutura com as informações apropriadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado sob as seguintes circunstâncias:

-   Se o membro **pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor de \_ textcallback de LPStr, o controle enviará esse código de notificação para recuperar o texto do item. Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador de texto TVIF definido.
-   Se o membro **iImage** ou **ISelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ IMAGECALLBACK, o controle enviará esse código de notificação para recuperar o índice dos ícones de um item na lista de imagens do controle. Nesse caso, se o item for selecionado, o membro **Mask** de *lParam* terá o \_ sinalizador de SELECTEDIMAGE TVIF definido. Se o item não estiver selecionado, o membro **Mask** de *lParam* terá o sinalizador de \_ imagem TVIF definido.
-   Se o membro **cChildren** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ CHILDRENCALLBACK, o controle enviará esse código de notificação para recuperar um valor que indica se o item tem itens filho. Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador filhos TVIF definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





