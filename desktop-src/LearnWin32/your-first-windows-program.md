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
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="b19ec-105">Módulo 1.</span><span class="sxs-lookup"><span data-stu-id="b19ec-105">Module 1.</span></span> <span data-ttu-id="b19ec-106">Seu primeiro programa do Windows</span><span class="sxs-lookup"><span data-stu-id="b19ec-106">Your First Windows Program</span></span>

<span data-ttu-id="b19ec-107">Neste módulo, escreveremos um programa de área de trabalho mínimo do Windows.</span><span class="sxs-lookup"><span data-stu-id="b19ec-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="b19ec-108">Tudo o que ele faz é criar e mostrar uma janela em branco.</span><span class="sxs-lookup"><span data-stu-id="b19ec-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="b19ec-109">Este primeiro programa contém cerca de 50 linhas de código, não contando linhas e comentários em branco.</span><span class="sxs-lookup"><span data-stu-id="b19ec-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="b19ec-110">Será o nosso ponto de partida; posteriormente, adicionaremos elementos gráficos, texto, entrada do usuário e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="b19ec-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="b19ec-111">Se você estiver procurando mais detalhes sobre como criar um aplicativo de área de trabalho tradicional do Windows no Visual Studio, confira  [passo a passos: criar um aplicativo de área de trabalho tradicional do Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="b19ec-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![captura de tela do programa de exemplo](images/window01.png)

<span data-ttu-id="b19ec-113">Este é o código completo do programa:</span><span class="sxs-lookup"><span data-stu-id="b19ec-113">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="b19ec-114">Você pode baixar o projeto completo do Visual Studio do [Windows Olá, mundo exemplo](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b19ec-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="b19ec-115">Pode ser útil dar uma breve descrição do que esse código faz.</span><span class="sxs-lookup"><span data-stu-id="b19ec-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="b19ec-116">Os tópicos posteriores examinarão o código em detalhes.</span><span class="sxs-lookup"><span data-stu-id="b19ec-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="b19ec-117">**wWinMain** é o ponto de entrada do programa.</span><span class="sxs-lookup"><span data-stu-id="b19ec-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="b19ec-118">Quando o programa é iniciado, ele registra algumas informações sobre o comportamento da janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b19ec-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="b19ec-119">Um dos itens mais importantes é o endereço de uma função, chamado `WindowProc` neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b19ec-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="b19ec-120">Essa função define o comportamento da janela — sua aparência, como ela interage com o usuário e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b19ec-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="b19ec-121">Em seguida, o programa cria a janela e recebe um identificador que identifica exclusivamente a janela.</span><span class="sxs-lookup"><span data-stu-id="b19ec-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="b19ec-122">Se a janela for criada com êxito, o programa entrará em um loop **while** .</span><span class="sxs-lookup"><span data-stu-id="b19ec-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="b19ec-123">O programa permanece nesse loop até que o usuário feche a janela e saia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b19ec-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="b19ec-124">Observe que o programa não chama explicitamente a `WindowProc` função, embora tenhamos dito isso onde a maior parte da lógica do aplicativo é definida.</span><span class="sxs-lookup"><span data-stu-id="b19ec-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="b19ec-125">O Windows se comunica com seu programa passando uma série de *mensagens*.</span><span class="sxs-lookup"><span data-stu-id="b19ec-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="b19ec-126">O código dentro do loop **while** orienta esse processo.</span><span class="sxs-lookup"><span data-stu-id="b19ec-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="b19ec-127">Cada vez que o programa chama a função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , ele indiretamente faz com que o Windows invoque a função WindowProc, uma vez para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="b19ec-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b19ec-128">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b19ec-128">In this section</span></span>

-   [<span data-ttu-id="b19ec-129">Criando uma janela</span><span class="sxs-lookup"><span data-stu-id="b19ec-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="b19ec-130">Mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="b19ec-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="b19ec-131">Escrevendo o procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="b19ec-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="b19ec-132">Pintando a janela</span><span class="sxs-lookup"><span data-stu-id="b19ec-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="b19ec-133">Fechando a janela</span><span class="sxs-lookup"><span data-stu-id="b19ec-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="b19ec-134">Gerenciando o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="b19ec-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="b19ec-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b19ec-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b19ec-136">Aprenda a programar para Windows em C++</span><span class="sxs-lookup"><span data-stu-id="b19ec-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="b19ec-137">Exemplo de Olá, Mundo do Windows</span><span class="sxs-lookup"><span data-stu-id="b19ec-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
