---
description: Enviado a uma janela que o usuário está movendo. Ao processar essa mensagem, um aplicativo pode monitorar a posição do retângulo de arrastar e, se necessário, alterar sua posição.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Mensagem de WM_MOVING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770047"
---
# <a name="wm_moving-message"></a>Mensagem de movimentação do WM \_

Enviado a uma janela que o usuário está movendo. Ao processar essa mensagem, um aplicativo pode monitorar a posição do retângulo de arrastar e, se necessário, alterar sua posição.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com a posição atual da janela, em coordenadas da tela. Para alterar a posição do retângulo de arrastar, um aplicativo deve alterar os membros dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar **true** se ele processar essa mensagem.

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

[**movimentação do WM \_**](wm-move.md)
</dt> <dt>

[**\_dimensionamento do WM**](wm-sizing.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
