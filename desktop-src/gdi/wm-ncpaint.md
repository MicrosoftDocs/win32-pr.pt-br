---
description: A mensagem do WM \_ NCPAINT é enviada para uma janela quando seu quadro deve ser pintado.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Mensagem de WM_NCPAINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827988"
---
# <a name="wm_ncpaint-message"></a>Mensagem do WM \_ NCPAINT

A mensagem do **WM \_ NCPAINT** é enviada para uma janela quando seu quadro deve ser pintado.

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

Um identificador para a região de atualização da janela. A região de atualização é recortada no quadro da janela.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo retornará zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pinta o quadro da janela.

Um aplicativo pode interceptar a mensagem **\_ NCPAINT do WM** e pintar seu próprio quadro de janela personalizado. A região de recorte para uma janela é sempre retangular, mesmo que a forma do quadro seja alterada.

O valor *wParam* pode ser passado para [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) como no exemplo a seguir.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**pintura do WM \_**](wm-paint.md)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
