---
title: Módulo 1. Seu primeiro programa do Windows
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104563579"
---
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="34b64-104">Módulo 1.</span><span class="sxs-lookup"><span data-stu-id="34b64-104">Module 1.</span></span> <span data-ttu-id="34b64-105">Seu primeiro programa do Windows</span><span class="sxs-lookup"><span data-stu-id="34b64-105">Your First Windows Program</span></span>

<span data-ttu-id="34b64-106">Neste módulo, escreveremos um programa de área de trabalho mínimo do Windows.</span><span class="sxs-lookup"><span data-stu-id="34b64-106">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="34b64-107">Tudo o que ele faz é criar e mostrar uma janela em branco.</span><span class="sxs-lookup"><span data-stu-id="34b64-107">All it does is create and show a blank window.</span></span> <span data-ttu-id="34b64-108">Este primeiro programa contém cerca de 50 linhas de código, não contando linhas e comentários em branco.</span><span class="sxs-lookup"><span data-stu-id="34b64-108">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="34b64-109">Será o nosso ponto de partida; posteriormente, adicionaremos elementos gráficos, texto, entrada do usuário e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="34b64-109">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="34b64-110">Se você estiver procurando mais detalhes sobre como criar um aplicativo de área de trabalho tradicional do Windows no Visual Studio, confira  [passo a passos: criar um aplicativo de área de trabalho tradicional do Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="34b64-110">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![captura de tela do programa de exemplo](images/window01.png)

<span data-ttu-id="34b64-112">Este é o código completo do programa:</span><span class="sxs-lookup"><span data-stu-id="34b64-112">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="34b64-113">Você pode baixar o projeto completo do Visual Studio do [Windows Olá, mundo exemplo](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="34b64-113">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="34b64-114">Pode ser útil dar uma breve descrição do que esse código faz.</span><span class="sxs-lookup"><span data-stu-id="34b64-114">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="34b64-115">Os tópicos posteriores examinarão o código em detalhes.</span><span class="sxs-lookup"><span data-stu-id="34b64-115">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="34b64-116">**wWinMain** é o ponto de entrada do programa.</span><span class="sxs-lookup"><span data-stu-id="34b64-116">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="34b64-117">Quando o programa é iniciado, ele registra algumas informações sobre o comportamento da janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34b64-117">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="34b64-118">Um dos itens mais importantes é o endereço de uma função, chamado `WindowProc` neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="34b64-118">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="34b64-119">Essa função define o comportamento da janela — sua aparência, como ela interage com o usuário e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="34b64-119">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="34b64-120">Em seguida, o programa cria a janela e recebe um identificador que identifica exclusivamente a janela.</span><span class="sxs-lookup"><span data-stu-id="34b64-120">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="34b64-121">Se a janela for criada com êxito, o programa entrará em um loop **while** .</span><span class="sxs-lookup"><span data-stu-id="34b64-121">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="34b64-122">O programa permanece nesse loop até que o usuário feche a janela e saia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34b64-122">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="34b64-123">Observe que o programa não chama explicitamente a `WindowProc` função, embora tenhamos dito isso onde a maior parte da lógica do aplicativo é definida.</span><span class="sxs-lookup"><span data-stu-id="34b64-123">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="34b64-124">O Windows se comunica com seu programa passando uma série de *mensagens*.</span><span class="sxs-lookup"><span data-stu-id="34b64-124">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="34b64-125">O código dentro do loop **while** orienta esse processo.</span><span class="sxs-lookup"><span data-stu-id="34b64-125">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="34b64-126">Cada vez que o programa chama a função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , ele indiretamente faz com que o Windows invoque a função WindowProc, uma vez para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="34b64-126">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34b64-127">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="34b64-127">In this section</span></span>

-   [<span data-ttu-id="34b64-128">Criando uma janela</span><span class="sxs-lookup"><span data-stu-id="34b64-128">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="34b64-129">Mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="34b64-129">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="34b64-130">Escrevendo o procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="34b64-130">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="34b64-131">Pintando a janela</span><span class="sxs-lookup"><span data-stu-id="34b64-131">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="34b64-132">Fechando a janela</span><span class="sxs-lookup"><span data-stu-id="34b64-132">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="34b64-133">Gerenciando o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="34b64-133">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="34b64-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34b64-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34b64-135">Aprenda a programar para Windows em C++</span><span class="sxs-lookup"><span data-stu-id="34b64-135">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="34b64-136">Exemplo de Olá, Mundo do Windows</span><span class="sxs-lookup"><span data-stu-id="34b64-136">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
