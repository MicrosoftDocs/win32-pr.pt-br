---
description: A mensagem do WM \_ SYSCOLORCHANGE é enviada para todas as janelas de nível superior quando uma alteração é feita em uma configuração de cor do sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Mensagem de WM_SYSCOLORCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e39ff8b5189da1a4cf48b7f6923c1cf12e8f30aa20fb26457d54a3f01d1b5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118483095"
---
# <a name="wm_syscolorchange-message"></a>Mensagem do WM \_ SYSCOLORCHANGE

A mensagem do **WM \_ SYSCOLORCHANGE** é enviada para todas as janelas de nível superior quando uma alteração é feita em uma configuração de cor do sistema.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O sistema envia uma mensagem de [**\_ pintura do WM**](wm-paint.md) para qualquer janela afetada por uma alteração de cor do sistema.

Os aplicativos que têm pincéis usando as cores do sistema existentes devem excluir esses pincéis e recriá-los usando as novas cores do sistema.

As janelas de nível superior que usam controles comuns devem encaminhar a mensagem do **WM \_ SYSCOLORCHANGE** para os controles; caso contrário, os controles não serão notificados sobre a alteração de cor. Isso garante que as cores usadas por seus controles comuns sejam consistentes com as usadas por outros objetos da interface do usuário. Por exemplo, um controle Toolbar usa a cor "objetos 3D" para desenhar seus botões. Se o usuário alterar a cor dos objetos 3D, mas a mensagem do **WM \_ SYSCOLORCHANGE** não for encaminhada para a barra de ferramentas, os botões da barra de ferramentas permanecerão na cor original, enquanto a cor de outros botões no sistema será alterada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral das cores](colors.md)
</dt> <dt>

[Mensagens de cores](color-messages.md)
</dt> <dt>

[**pintura do WM \_**](wm-paint.md)
</dt> </dl>

 

 
