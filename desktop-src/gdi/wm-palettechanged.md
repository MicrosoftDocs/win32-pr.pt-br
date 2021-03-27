---
description: A \_ mensagem da paletachanged do WM é enviada a todas as janelas de nível superior e sobrepostas após a janela com o foco do teclado ter percebido sua paleta lógica, alterando assim a paleta do sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Mensagem de WM_PALETTECHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661962"
---
# <a name="wm_palettechanged-message"></a>\_Mensagem da paletachanged do WM

A mensagem da **\_ Paletachanged do WM** é enviada a todas as janelas de nível superior e sobrepostas após a janela com o foco do teclado ter percebido sua paleta lógica, alterando assim a paleta do sistema. Essa mensagem habilita uma janela que usa uma paleta de cores, mas não tem o foco do teclado para compreender sua paleta lógica e atualizar sua área do cliente.

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

Um identificador para a janela que fez com que a paleta do sistema fosse alterada.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem deve ser enviada a todas as janelas de nível superior e sobrepostas, incluindo aquela que alterou a paleta do sistema. Se qualquer janela filho usar uma paleta de cores, essa mensagem também deverá ser passada para elas.

Para evitar a criação de um loop infinito, uma janela que recebe essa mensagem não deve perceber sua paleta, a menos que ela determine que *wParam* não contém seu próprio identificador de janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral das cores](colors.md)
</dt> <dt>

[Mensagens de cores](color-messages.md)
</dt> <dt>

[**PALETTEISCHANGING do WM \_**](wm-paletteischanging.md)
</dt> <dt>

[**QUERYNEWPALETTE do WM \_**](wm-querynewpalette.md)
</dt> </dl>

 

 
