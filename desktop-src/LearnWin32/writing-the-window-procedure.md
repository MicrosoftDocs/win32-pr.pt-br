---
title: Escrevendo o procedimento de janela
description: Escrevendo o procedimento de janela
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105714"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="05901-103">Escrevendo o procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="05901-103">Writing the Window Procedure</span></span>

<span data-ttu-id="05901-104">A função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chama o procedimento de janela da janela que é o destino da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="05901-105">O procedimento de janela tem a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="05901-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="05901-106">Há quatro parâmetros:</span><span class="sxs-lookup"><span data-stu-id="05901-106">There are four parameters:</span></span>

- <span data-ttu-id="05901-107">*HWND* é um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="05901-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="05901-108">*uMsg* é o código da mensagem; por exemplo, a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) indica que a janela foi redimensionada.</span><span class="sxs-lookup"><span data-stu-id="05901-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="05901-109">*wParam* e *lParam* contêm dados adicionais que pertencem à mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="05901-110">O significado exato depende do código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="05901-111">**LRESULT** é um valor inteiro que seu programa retorna ao Windows.</span><span class="sxs-lookup"><span data-stu-id="05901-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="05901-112">Ele contém a resposta do programa a uma mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="05901-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="05901-113">O significado desse valor depende do código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="05901-114">O **retorno** de chamada é a Convenção de chamada para a função.</span><span class="sxs-lookup"><span data-stu-id="05901-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="05901-115">Um procedimento de janela típico é simplesmente uma grande instrução switch que alterna o código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="05901-116">Adicione casos para cada mensagem que você deseja manipular.</span><span class="sxs-lookup"><span data-stu-id="05901-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="05901-117">Dados adicionais para a mensagem estão contidos nos parâmetros *lParam* e *wParam* .</span><span class="sxs-lookup"><span data-stu-id="05901-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="05901-118">Ambos os parâmetros são valores inteiros do tamanho de uma largura de ponteiro (32 bits ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="05901-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="05901-119">O significado de cada um depende do código da mensagem (*uMsg*).</span><span class="sxs-lookup"><span data-stu-id="05901-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="05901-120">Para cada mensagem, você precisará pesquisar o código de mensagem no MSDN e converter os parâmetros para o tipo de dados correto.</span><span class="sxs-lookup"><span data-stu-id="05901-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="05901-121">Normalmente, os dados são um valor numérico ou um ponteiro para uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="05901-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="05901-122">Algumas mensagens não têm nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="05901-122">Some messages do not have any data.</span></span>

<span data-ttu-id="05901-123">Por exemplo, a documentação para a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) informa que:</span><span class="sxs-lookup"><span data-stu-id="05901-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="05901-124">*wParam* é um sinalizador que indica se a janela foi minimizada, maximizada ou redimensionada.</span><span class="sxs-lookup"><span data-stu-id="05901-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="05901-125">*lParam* contém a nova largura e a altura da janela como valores de 16 bits empacotados no número 1 32-ou 64-bit.</span><span class="sxs-lookup"><span data-stu-id="05901-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="05901-126">Você precisará executar uma mudança de bits para obter esses valores.</span><span class="sxs-lookup"><span data-stu-id="05901-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="05901-127">Felizmente, o arquivo de cabeçalho WinDef. h inclui macros auxiliares que fazem isso.</span><span class="sxs-lookup"><span data-stu-id="05901-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="05901-128">Um procedimento de janela típico lida com dezenas de mensagens, para que possa aumentar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="05901-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="05901-129">Uma maneira de tornar seu código mais modular é colocar a lógica para manipular cada mensagem em uma função separada.</span><span class="sxs-lookup"><span data-stu-id="05901-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="05901-130">No procedimento de janela, converta os parâmetros *wParam* e *lParam* no tipo de dados correto e passe esses valores para a função.</span><span class="sxs-lookup"><span data-stu-id="05901-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="05901-131">Por exemplo, para manipular a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) , o procedimento da janela ficaria assim:</span><span class="sxs-lookup"><span data-stu-id="05901-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="05901-132">As macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obtêm os valores de largura e altura de 16 bits do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="05901-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="05901-133">(Você pode procurar esses tipos de detalhes na documentação do MSDN para cada código de mensagem.) O procedimento de janela extrai a largura e a altura e, em seguida, passa esses valores para a `OnSize` função.</span><span class="sxs-lookup"><span data-stu-id="05901-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="05901-134">Manipulação de mensagens padrão</span><span class="sxs-lookup"><span data-stu-id="05901-134">Default Message Handling</span></span>

<span data-ttu-id="05901-135">Se você não tratar uma mensagem específica em seu procedimento de janela, passe os parâmetros da mensagem diretamente para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="05901-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="05901-136">Essa função executa a ação padrão para a mensagem, que varia por tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="05901-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="05901-137">Evitando afunilamentos em seu procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="05901-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="05901-138">Enquanto o procedimento de janela é executado, ele bloqueia todas as outras mensagens do Windows criadas no mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="05901-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="05901-139">Portanto, evite processamento longo dentro de seu procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="05901-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="05901-140">Por exemplo, suponha que seu programa abra uma conexão TCP e espere indefinidamente que o servidor responda.</span><span class="sxs-lookup"><span data-stu-id="05901-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="05901-141">Se você fizer isso dentro do procedimento de janela, sua interface do usuário não responderá até que a solicitação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="05901-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="05901-142">Durante esse tempo, a janela não pode processar a entrada do mouse ou do teclado, redesenhar a si mesma ou até mesmo fechar.</span><span class="sxs-lookup"><span data-stu-id="05901-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="05901-143">Em vez disso, você deve mover o trabalho para outro thread, usando um dos recursos de multitarefa que são criados no Windows:</span><span class="sxs-lookup"><span data-stu-id="05901-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="05901-144">Crie um novo thread.</span><span class="sxs-lookup"><span data-stu-id="05901-144">Create a new thread.</span></span>
- <span data-ttu-id="05901-145">Use um pool de thread.</span><span class="sxs-lookup"><span data-stu-id="05901-145">Use a thread pool.</span></span>
- <span data-ttu-id="05901-146">Usar chamadas de e/s assíncronas.</span><span class="sxs-lookup"><span data-stu-id="05901-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="05901-147">Usar chamadas de procedimento assíncronos.</span><span class="sxs-lookup"><span data-stu-id="05901-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="05901-148">Avançar</span><span class="sxs-lookup"><span data-stu-id="05901-148">Next</span></span>

[<span data-ttu-id="05901-149">Pintando a janela</span><span class="sxs-lookup"><span data-stu-id="05901-149">Painting the Window</span></span>](painting-the-window.md)
