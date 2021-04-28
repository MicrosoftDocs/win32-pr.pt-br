---
title: Módulo 1. Seu primeiro programa do Windows
description: Módulo 1. Seu primeiro programa do Windows
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110944"
---
# <a name="module-1-your-first-windows-program"></a>Módulo 1. Seu primeiro programa do Windows

Neste módulo, escreveremos um programa de área de trabalho mínimo do Windows. Tudo o que ele faz é criar e mostrar uma janela em branco. Este primeiro programa contém cerca de 50 linhas de código, não contando linhas e comentários em branco. Será o nosso ponto de partida; posteriormente, adicionaremos elementos gráficos, texto, entrada do usuário e outros recursos.

Se você estiver procurando mais detalhes sobre como criar um aplicativo de área de trabalho tradicional do Windows no Visual Studio, confira  [passo a passos: criar um aplicativo de área de trabalho tradicional do Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![captura de tela do programa de exemplo](images/window01.png)

Este é o código completo do programa:


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

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



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





Você pode baixar o projeto completo do Visual Studio do [Windows Olá, mundo exemplo](windows-hello-world-sample.md).

Pode ser útil dar uma breve descrição do que esse código faz. Os tópicos posteriores examinarão o código em detalhes.

1.  **wWinMain** é o ponto de entrada do programa. Quando o programa é iniciado, ele registra algumas informações sobre o comportamento da janela do aplicativo. Um dos itens mais importantes é o endereço de uma função, chamado `WindowProc` neste exemplo. Essa função define o comportamento da janela — sua aparência, como ela interage com o usuário e assim por diante.
2.  Em seguida, o programa cria a janela e recebe um identificador que identifica exclusivamente a janela.
3.  Se a janela for criada com êxito, o programa entrará em um loop **while** . O programa permanece nesse loop até que o usuário feche a janela e saia do aplicativo.

Observe que o programa não chama explicitamente a `WindowProc` função, embora tenhamos dito isso onde a maior parte da lógica do aplicativo é definida. O Windows se comunica com seu programa passando uma série de *mensagens*. O código dentro do loop **while** orienta esse processo. Cada vez que o programa chama a função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , ele indiretamente faz com que o Windows invoque a função WindowProc, uma vez para cada mensagem.

## <a name="in-this-section"></a>Nesta seção

-   [Criando uma janela](creating-a-window.md)
-   [Mensagens de janela](window-messages.md)
-   [Escrevendo o procedimento de janela](writing-the-window-procedure.md)
-   [Pintando a janela](painting-the-window.md)
-   [Fechando a janela](closing-the-window.md)
-   [Gerenciando o estado do aplicativo](managing-application-state-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprenda a programar para Windows em C++](learn-to-program-for-windows.md)
</dt> <dt>

[Exemplo de Olá, Mundo do Windows](windows-hello-world-sample.md)
</dt> </dl>

 

 
