---
description: A mensagem WM \_ DISPLAYCHANGE é enviada para todas as janelas quando a resolução de exibição é alterada.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: WM_DISPLAYCHANGE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d28f5708618ada0d766b140f01ff81a9427f443abb89cf41ba2c743223fbc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037430"
---
# <a name="wm_displaychange-message"></a>Mensagem WM \_ DISPLAYCHANGE

A **mensagem WM \_ DISPLAYCHANGE** é enviada para todas as janelas quando a resolução de exibição é alterada.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

A palavra de ordem baixa especifica a resolução horizontal da tela.

A palavra de ordem alta especifica a resolução vertical da tela.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem só é enviada para janelas de nível superior. Para todas as outras janelas, ela é postada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pintura e desenho](painting-and-drawing.md)
</dt> <dt>

[Pintar e desenhar mensagens](painting-and-drawing-messages.md)
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
