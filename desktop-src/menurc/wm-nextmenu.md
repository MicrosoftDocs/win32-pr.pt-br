---
title: WM_NEXTMENU mensagem (Winuser.h)
description: Enviado para um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952076"
---
# <a name="wm_nextmenu-message"></a>Mensagem \_ WM NEXTMENU

Enviado para um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave. Consulte [**Códigos de chave virtual.**](/windows/desktop/inputdev/virtual-key-codes)

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura MMAXXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contém informações sobre o menu a ser ativado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao responder a essa mensagem, o aplicativo pode especificar o menu para o qual alternar no **membro hmenuNext** de [**M FITNESSXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e na janela para receber as mensagens de notificação de menu no **hwndNext** membro da estrutura **MWNXTMENU.** Você deve definir os dois membros para que as alterações entre em vigor (inicialmente são **NULL).**

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

[**MARDXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

