---
title: WM_MENUDRAG mensagem (Winuser.h)
description: Enviado ao proprietário de um menu do tipo "arrastar e soltar" quando o usuário arrasta um item de menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22792c7606bb001b72b7c4751d14129bca02c5b4a5b337e0349a9a9a2120b62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971795"
---
# <a name="wm_menudrag-message"></a>Mensagem \_ WM MENUDRAG

Enviado ao proprietário de um menu do tipo "arrastar e soltar" quando o usuário arrasta um item de menu.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A posição do item em que a operação de arrastar começou.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o menu que contém o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo deve retornar um dos valores a seguir.



| Valor/código de retorno                                                                                                                                   | Descrição                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUE**</dt> <dt>0</dt> </dl> | O menu deve permanecer ativo. Se o mouse for liberado, ele deverá ser ignorado.<br/> |
| <dl> <dt>**MND \_ ENDMENU**</dt> <dt>1</dt> </dl>  | O menu deve ser encerrado.<br/>                                                      |



 

## <a name="remarks"></a>Comentários

O aplicativo pode chamar a [**função DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) em resposta a essa mensagem.

Para criar um menu do arrastar e soltar, chame [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) com **MNS \_ DRAGDROP.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

