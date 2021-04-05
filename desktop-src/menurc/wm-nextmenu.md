---
title: Mensagem de WM_NEXTMENU (WinUser. h)
description: Enviado a um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU menus de mensagens e outros recursos
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
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919199"
---
# <a name="wm_nextmenu-message"></a>Mensagem do WM \_ NEXTMENU

Enviado a um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave. Consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contém informações sobre o menu a ser ativado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao responder a essa mensagem, o aplicativo pode especificar o menu para alternar para o membro **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e a janela para receber as mensagens de notificação de menu no membro **hWndNext** da estrutura **MDINEXTMENU** . Você deve definir ambos os membros para que as alterações entrem em vigor (elas são inicialmente **nulas**).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

