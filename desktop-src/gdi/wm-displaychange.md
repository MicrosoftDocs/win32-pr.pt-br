---
description: A mensagem do WM \_ DISPLAYCHANGE é enviada para todas as janelas quando a resolução de vídeo é alterada.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Mensagem de WM_DISPLAYCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169130"
---
# <a name="wm_displaychange-message"></a>Mensagem do WM \_ DISPLAYCHANGE

A mensagem do **WM \_ DISPLAYCHANGE** é enviada para todas as janelas quando a resolução de vídeo é alterada.

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

A nova profundidade da imagem da exibição, em bits por pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a resolução horizontal da tela.

A palavra de ordem superior especifica a resolução vertical da tela.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada somente para janelas de nível superior. Para todas as outras janelas, ele é Postado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pintura e desenho](painting-and-drawing.md)
</dt> <dt>

[Pintura e desenho de mensagens](painting-and-drawing-messages.md)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
