---
title: Mensagem de WM_ENTERMENULOOP (WinUser. h)
description: Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi inserido.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5851109e44100d558603fb268a4668c1f138fff97e5e87db50a28445e70adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939606"
---
# <a name="wm_entermenuloop-message"></a>Mensagem do WM \_ ENTERMENULOOP

Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi inserido.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se o menu de janela foi inserido usando a função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) . Esse parâmetro terá um valor **true** se o menu Window tiver sido inserido usando **TrackPopupMenu** e **false** se não tiver sido.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EXITMENULOOP do WM \_**](wm-exitmenuloop.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

