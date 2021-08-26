---
Description: A mensagem de pintura do WM \_ é enviada quando o sistema ou outro aplicativo faz uma solicitação para pintar uma parte da janela de um aplicativo.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Mensagem de WM_PAINT (WinUser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b5efec4bc92fcb3c90a8def59b2e85d98342cf641dfe959fc2a651f81ffc1f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092506"
---
# <a name="wm_paint-message"></a>Mensagem de pintura do WM \_

A mensagem de **\_ pintura do WM** é enviada quando o sistema ou outro aplicativo faz uma solicitação para pintar uma parte da janela de um aplicativo. A mensagem é enviada quando a função [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) ou [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) é chamada ou pela função [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) quando o aplicativo obtém uma mensagem de **\_ pintura do WM** usando a função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

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

## <a name="return-value"></a>Valor retornado

Um aplicativo retornará zero se ele processar essa mensagem.

## <a name="example"></a>Exemplo

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

exemplo de [exemplos clássicos Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) em GitHub.

## <a name="remarks"></a>Comentários

A mensagem de **\_ pintura do WM** é gerada pelo sistema e não deve ser enviada por um aplicativo. Para forçar uma janela a desenhar em um contexto de dispositivo específico, use a mensagem do [**WM \_ Print**](wm-print.md) ou [**WM \_ fileclient**](wm-printclient.md) . Observe que isso requer que a janela de destino dê suporte à mensagem do **WM \_ fileclient** . Os controles mais comuns dão suporte à mensagem do **WM \_ fileclient** .

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valida a região de atualização. A função também pode enviar a mensagem do [**WM \_ NCPAINT**](wm-ncpaint.md) para o procedimento de janela se o quadro da janela deve ser pintado e enviar a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se o plano de fundo da janela precisar ser apagado.

O sistema envia essa mensagem quando não há nenhuma outra mensagem na fila de mensagens do aplicativo. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina para onde enviar a mensagem; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina qual mensagem deve ser expedida. **GetMessage** retorna a mensagem de **\_ pintura do WM** quando não há nenhuma outra mensagem na fila de mensagens do aplicativo e **DispatchMessage** envia a mensagem para o procedimento de janela apropriado.

Uma janela pode receber mensagens de pintura internas como resultado da chamada de [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com o \_ sinalizador RDW INTERNALPAINT definido. Nesse caso, a janela pode não ter uma região de atualização. Um aplicativo pode chamar a função [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) para determinar se a janela tem uma região de atualização. Se **GetUpdateRect** retornar zero, o aplicativo não precisará chamar as funções [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**endpaintt**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Um aplicativo deve verificar se há qualquer pintura interna necessária examinando suas estruturas de dados internas para cada mensagem de **\_ pintura do WM** , pois uma mensagem de **\_ pintura do WM** pode ter sido causada por uma região de atualização não nula e uma chamada para [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com o \_ sinalizador RDW INTERNALPAINT definido.

O sistema envia uma mensagem **de \_ pintura do WM** interno apenas uma vez. Depois que uma mensagem de **\_ pintura do WM** interno for retornada de [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou for enviada para uma janela pelo [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), o sistema não publicará nem enviará mais mensagens de **\_ pintura do WM** até que a janela seja invalidada ou até que [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) seja chamado novamente com o \_ sinalizador RDW INTERNALPAINT definido.

Para alguns controles comuns, o processamento de mensagem padrão do **WM \_ Paint** verifica o parâmetro *wParam* . Se *wParam* for não nulo, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo.

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

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**ERASEBKGND do WM \_**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**NCPAINT do WM \_**](wm-ncpaint.md)
</dt> <dt>

[**impressão do WM \_**](wm-print.md)
</dt> <dt>

[**WM \_ FILEclient**](wm-printclient.md)
</dt> </dl>

 

 
