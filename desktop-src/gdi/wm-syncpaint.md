---
description: A mensagem do WM \_ SYNCPAINT é usada para sincronizar a pintura enquanto evita a vinculação de threads de GUI independentes.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Mensagem de WM_SYNCPAINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988950"
---
# <a name="wm_syncpaint-message"></a>Mensagem do WM \_ SYNCPAINT

A mensagem do **WM \_ SYNCPAINT** é usada para sincronizar a pintura enquanto evita a vinculação de threads de GUI independentes.

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

## <a name="return-value"></a>Retornar valor

Um aplicativo retornará zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Quando uma janela é oculta, mostrada, movida ou dimensionada, o sistema pode determinar que é necessário enviar uma mensagem do **WM \_ SYNCPAINT** para as janelas de nível superior de outros threads. Os aplicativos devem passar o **WM \_ SYNCPAINT** para o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para processamento. A função **DefWindowProc** enviará uma mensagem do [**WM \_ NCPAINT**](wm-ncpaint.md) para o procedimento de janela se o quadro da janela precisar ser pintado e enviar uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se o plano de fundo da janela precisar ser apagado.

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

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**pintura do WM \_**](wm-paint.md)
</dt> </dl>

 

 
