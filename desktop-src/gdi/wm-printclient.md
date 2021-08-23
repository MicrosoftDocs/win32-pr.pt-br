---
description: A mensagem do WM \_ fileclient é enviada a uma janela para solicitar que ela Desenhe sua área de cliente no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Mensagem de WM_PRINTCLIENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717656"
---
# <a name="wm_printclient-message"></a>Mensagem do WM \_ FILEclient

A mensagem do **WM \_ fileclient** é enviada a uma janela para solicitar que ela Desenhe sua área de cliente no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.

Diferentemente do [**WM \_ Print**](wm-print.md), o **WM \_ fileclient** não é processado pelo [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Uma janela deve processar a mensagem do **WM \_ fileclient** por meio de uma função do [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definida pelo aplicativo para que ela seja usada corretamente.


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

Um identificador para o contexto do dispositivo para desenhar.

</dd> <dt>

*lParam* 
</dt> <dd>

As opções de desenho. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Desenha a janela somente se ela estiver visível.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**filhos de PRF \_**</dt> </dl>             | Desenha todas as janelas filhas visíveis.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_cliente PRF**</dt> </dl>                   | Desenha a área do cliente da janela.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Apaga o plano de fundo antes de desenhar a janela.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**Não \_ cliente PRF**</dt> </dl>          | Desenha a área não cliente da janela.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**Propriedade do PRF \_**</dt> </dl>                      | Desenha todas as janelas de propriedade.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma janela pode processar essa mensagem da mesma maneira que o [**WM \_ Paint**](./wm-paint.md), exceto que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) não precisam ser chamados (um contexto de dispositivo é fornecido) e a janela deve desenhar toda a área do cliente em vez de apenas a região inválida.

Windows que podem ser usadas em qualquer lugar no sistema, como controles, devem processar essa mensagem. Provavelmente vale a pena que outras janelas processem essa mensagem também porque é relativamente fácil de implementar.

A função [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) requer que a janela que está sendo animada implemente a mensagem do **WM \_ fileclient** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pintura e desenho](painting-and-drawing.md)
</dt> <dt>

[Pintura e desenho de mensagens](painting-and-drawing-messages.md)
</dt> <dt>

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**pintura do WM \_**](wm-paint.md)
</dt> </dl>

 

 
