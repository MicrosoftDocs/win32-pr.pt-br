---
title: Mensagem de WM_INITMENU (WinUser. h)
description: Enviado quando um menu está prestes a ficar ativo.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff775849abf6a7e3be4530ce893e1ae8821cb4be6e9fb2888ef9bb0ee6d67d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939566"
---
# <a name="wm_initmenu-message"></a>Mensagem do WM \_ INITMENU

Enviado quando um menu está prestes a ficar ativo. Ele ocorre quando o usuário clica em um item na barra de menus ou pressiona uma tecla de menu. Isso permite que o aplicativo modifique o menu antes que ele seja exibido.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o menu a ser inicializado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma mensagem do **WM \_ INITMENU** é enviada somente quando um menu é acessado pela primeira vez; apenas uma mensagem do **WM \_ INITMENU** é gerada para cada acesso. Por exemplo, mover o mouse em vários itens de menu enquanto mantém pressionado o botão não gera novas mensagens. **WM \_ INITMENU** não fornece informações sobre itens de menu.

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

[**INITMENUPOPUP do WM \_**](wm-initmenupopup.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

