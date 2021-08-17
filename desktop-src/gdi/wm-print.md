---
description: A mensagem WM PRINT é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo \_ de impressora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09d3cb7dbb3b4a4fca7a2af4272f1b4175aa26e911d1def909c97ba35f3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964846"
---
# <a name="wm_print-message"></a>Mensagem WM \_ PRINT

A **mensagem WM \_ PRINT** é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.

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

Um alça para o contexto do dispositivo no qual desenhar.

</dd> <dt>

*lParam* 
</dt> <dd>

As opções de desenho. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Desenha a janela somente se ela estiver visível.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Desenha todas as janelas filho visíveis.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**CLIENTE \_ PRF**</dt> </dl>                   | Desenha a área do cliente da janela.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | Apaga a plano de fundo antes de desenhar a janela.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Desenha a área não dependente da janela.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PRF \_ PROPRIEDADE**</dt> </dl>                      | Desenha todas as janelas de propriedade.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa essa mensagem com base na opção de desenho especificada: se PRF CHECKVISIBLE for especificado e a janela não estiver visível, não faça nada, se PRF NONCLIENT for especificado, desenhe a área não cliente no contexto do dispositivo especificado, se ERASEBKGND prf for especificado, envie à janela uma mensagem \_ WM \_ \_ [**\_ ERASEBKGND,**](../winmsg/wm-erasebkgnd.md) se o CLIENTE PRF for especificado, envie à janela uma mensagem \_ WM [**\_ PRINTCLIENT,**](wm-printclient.md) se CHILD PRF estiver \_ definido, **\_** \_ **\_** envie a cada janela filho visível uma mensagem WM PRINT, se PRF OWNED estiver definida, envie a cada janela de propriedade visível uma mensagem WM PRINT.

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

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
