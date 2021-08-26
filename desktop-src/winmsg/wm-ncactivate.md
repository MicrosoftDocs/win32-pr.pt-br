---
description: Enviado para uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095f0cc7f555b4daf80a67a2394e29286f32a49dcba687780e8747f5d1b193fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055996"
---
# <a name="wm_ncactivate-message"></a>Mensagem \_ WM NCACTIVATE

Enviado para uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica quando uma barra de título ou ícone precisa ser alterado para indicar um estado ativo ou inativo. Se uma barra de título ou ícone ativo for desenhado, o *parâmetro wParam* será **TRUE.** Se uma barra de título ou ícone inativo for desenhado, *wParam* será **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Quando um [estilo visual](../controls/themes-overview.md) está ativo para essa janela, esse parâmetro não é usado.

Quando um estilo visual não está ativo para essa janela, esse parâmetro é um handle para uma região de atualização opcional para a área não dependente da janela. Se esse parâmetro for definido como -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não reintigue a área não dependente para refletir a alteração de estado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Quando o *parâmetro wParam* é **FALSE**, um aplicativo deve retornar **TRUE** para indicar que o sistema deve continuar com o processamento padrão ou deve retornar **FALSE** para evitar a alteração. Quando *wParam* é **TRUE,** o valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O processamento de mensagens relacionadas à área não dependente de uma janela padrão não é recomendado, pois o aplicativo deve ser capaz de desenhar todas as partes necessárias da área não dependente para a janela. Se um aplicativo processar essa mensagem, ele deverá retornar **TRUE** para direcionar o sistema para concluir a alteração da janela ativa. Se a janela for minimizada quando essa mensagem for recebida, o aplicativo deverá passar a mensagem para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) desenha a barra de título ou o título do ícone em suas cores ativas quando o parâmetro *wParam* é **TRUE** e em suas cores inativas quando *wParam* é **FALSE.**

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

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
