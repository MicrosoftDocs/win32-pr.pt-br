---
description: Enviado a uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Mensagem de WM_NCACTIVATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789914"
---
# <a name="wm_ncactivate-message"></a>Mensagem do WM \_ NCACTIVATE

Enviado a uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica quando uma barra de título ou um ícone precisa ser alterado para indicar um estado ativo ou inativo. Se uma barra de título ou um ícone ativo for ser desenhado, o parâmetro *wParam* será **true**. Se uma barra de título ou um ícone inativo for ser desenhado, *wParam* será **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando um [estilo visual](../controls/themes-overview.md) está ativo para esta janela, esse parâmetro não é usado.

Quando um estilo visual não está ativo para esta janela, esse parâmetro é um identificador para uma região de atualização opcional para a área não cliente da janela. Se esse parâmetro for definido como-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não repintará a área não cliente para refletir a alteração de estado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Quando o parâmetro *wParam* é **false**, um aplicativo deve retornar **true** para indicar que o sistema deve continuar com o processamento padrão ou deve retornar **false** para impedir a alteração. Quando *wParam* é **true**, o valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O processamento de mensagens relacionadas à área não cliente de uma janela padrão não é recomendado, pois o aplicativo deve ser capaz de desenhar todas as partes necessárias da área não cliente para a janela. Se um aplicativo processar essa mensagem, ele deverá retornar **true** para instruir o sistema a concluir a alteração da janela ativa. Se a janela for minimizada quando essa mensagem for recebida, o aplicativo deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) desenha a barra de título ou o título do ícone em suas cores ativas quando o parâmetro *wParam* é **true** e em suas cores inativas quando *wParam* é **false**.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
