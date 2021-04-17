---
title: TVN_SETDISPINFO código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que ele deve atualizar as informações que ele mantém sobre um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO de código de notificação controles do Windows
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
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756230"
---
# <a name="tvn_setdispinfo-notification-code"></a>Código de notificação do TVN \_ SETDISPINFO

Notifica uma janela pai do controle de exibição de árvore que ele deve atualizar as informações que ele mantém sobre um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que descreve o item que está sendo atualizado. O membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica o item que está sendo atualizado e o membro **Mask** especifica quais atributos do item estão sendo atualizados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Se o membro **pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor de \_ textcallback de LPStr, o controle enviará essa notificação para definir o texto do item. Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador de texto TVIF definido.

Se o membro **iImage** ou **ISelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ IMAGECALLBACK, o controle enviará essa notificação para recuperar o índice da imagem de ícone a ser exibida. Nesse caso, o membro **Mask** de *lParam* terá a \_ imagem TVIF ou o sinalizador de \_ SELECTEDIMAGE TVIF definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





