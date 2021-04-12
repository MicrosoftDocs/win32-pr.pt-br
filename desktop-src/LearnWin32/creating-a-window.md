---
title: Criando uma janela
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366026"
---
# <a name="creating-a-window"></a><span data-ttu-id="f6297-103">Criando uma janela</span><span class="sxs-lookup"><span data-stu-id="f6297-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="f6297-104">Classes de janela</span><span class="sxs-lookup"><span data-stu-id="f6297-104">Window Classes</span></span>

<span data-ttu-id="f6297-105">Uma *classe de janela* define um conjunto de comportamentos que várias janelas podem ter em comum.</span><span class="sxs-lookup"><span data-stu-id="f6297-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="f6297-106">Por exemplo, em um grupo de botões, cada botão tem um comportamento semelhante quando o usuário clica no botão.</span><span class="sxs-lookup"><span data-stu-id="f6297-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="f6297-107">É claro que os botões não são completamente idênticos; cada botão exibe sua própria cadeia de texto e tem suas próprias coordenadas de tela.</span><span class="sxs-lookup"><span data-stu-id="f6297-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="f6297-108">Os dados exclusivos para cada janela são chamados de *dados de instância*.</span><span class="sxs-lookup"><span data-stu-id="f6297-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="f6297-109">Cada janela deve ser associada a uma classe de janela, mesmo que seu programa nunca crie uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="f6297-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="f6297-110">É importante entender que uma classe de janela não é uma "classe" no sentido C++.</span><span class="sxs-lookup"><span data-stu-id="f6297-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="f6297-111">Em vez disso, é uma estrutura de dados usada internamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f6297-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="f6297-112">As classes de janela são registradas com o sistema em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f6297-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="f6297-113">Para registrar uma nova classe de janela, comece preenchendo uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) :</span><span class="sxs-lookup"><span data-stu-id="f6297-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="f6297-114">Você deve definir os seguintes membros da estrutura:</span><span class="sxs-lookup"><span data-stu-id="f6297-114">You must set the following structure members:</span></span>

- <span data-ttu-id="f6297-115">**lpfnWndProc** é um ponteiro para uma função definida pelo aplicativo chamada de *procedimento de janela* ou "proc de janela".</span><span class="sxs-lookup"><span data-stu-id="f6297-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="f6297-116">O procedimento de janela define a maior parte do comportamento da janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="f6297-117">Examinaremos o procedimento de janela detalhadamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f6297-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="f6297-118">Por enquanto, apenas trate isso como uma referência posterior.</span><span class="sxs-lookup"><span data-stu-id="f6297-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="f6297-119">**HINSTANCE** é o identificador para a instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6297-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="f6297-120">Obtenha esse valor do parâmetro *HINSTANCE* de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="f6297-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="f6297-121">**lpszClassName** é uma cadeia de caracteres que identifica a classe da janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="f6297-122">Os nomes de classe são locais para o processo atual, portanto, o nome só precisa ser exclusivo dentro do processo.</span><span class="sxs-lookup"><span data-stu-id="f6297-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="f6297-123">No entanto, os controles padrão do Windows também têm classes.</span><span class="sxs-lookup"><span data-stu-id="f6297-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="f6297-124">Se você usar qualquer um desses controles, deverá escolher nomes de classe que não estejam em conflito com os nomes de classe de controle.</span><span class="sxs-lookup"><span data-stu-id="f6297-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="f6297-125">Por exemplo, a classe Window para o controle Button é chamada de "Button".</span><span class="sxs-lookup"><span data-stu-id="f6297-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="f6297-126">A estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) tem outros membros não mostrados aqui.</span><span class="sxs-lookup"><span data-stu-id="f6297-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="f6297-127">Você pode defini-los como zero, conforme mostrado neste exemplo, ou preenchê-los em.</span><span class="sxs-lookup"><span data-stu-id="f6297-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="f6297-128">A documentação do MSDN descreve a estrutura em detalhes.</span><span class="sxs-lookup"><span data-stu-id="f6297-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="f6297-129">Em seguida, passe o endereço da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) para a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="f6297-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="f6297-130">Essa função registra a classe Window com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f6297-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="f6297-131">Criando a janela</span><span class="sxs-lookup"><span data-stu-id="f6297-131">Creating the Window</span></span>

<span data-ttu-id="f6297-132">Para criar uma nova instância de uma janela, chame a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :</span><span class="sxs-lookup"><span data-stu-id="f6297-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
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
```

<span data-ttu-id="f6297-133">Você pode ler descrições de parâmetros detalhadas no MSDN, mas aqui está um resumo rápido:</span><span class="sxs-lookup"><span data-stu-id="f6297-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="f6297-134">O primeiro parâmetro permite que você especifique alguns comportamentos opcionais para a janela (por exemplo, janelas transparentes).</span><span class="sxs-lookup"><span data-stu-id="f6297-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="f6297-135">Defina esse parâmetro como zero para os comportamentos padrão.</span><span class="sxs-lookup"><span data-stu-id="f6297-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="f6297-136">`CLASS_NAME` é o nome da classe da janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="f6297-137">Isso define o tipo de janela que você está criando.</span><span class="sxs-lookup"><span data-stu-id="f6297-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="f6297-138">O texto da janela é usado de maneiras diferentes por tipos diferentes de janelas.</span><span class="sxs-lookup"><span data-stu-id="f6297-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="f6297-139">Se a janela tiver uma barra de título, o texto será exibido na barra de título.</span><span class="sxs-lookup"><span data-stu-id="f6297-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="f6297-140">O estilo de janela é um conjunto de sinalizadores que definem algumas das aparências de uma janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="f6297-141">A constante **WS \_ OVERLAPPEDWINDOW** é, na verdade, vários sinalizadores combinados com **um OR-bit.**</span><span class="sxs-lookup"><span data-stu-id="f6297-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="f6297-142">Juntos, esses sinalizadores dão à janela uma barra de título, uma borda, um menu do sistema e **minimizam** e **maximizam** os botões.</span><span class="sxs-lookup"><span data-stu-id="f6297-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="f6297-143">Esse conjunto de sinalizadores é o estilo mais comum para uma janela de aplicativo de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f6297-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="f6297-144">Para posição e tamanho, a constante de **PV de \_ USEDEFAULT** significa usar valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f6297-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="f6297-145">O próximo parâmetro define uma janela pai ou uma janela de proprietário para a nova janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="f6297-146">Defina o pai se você estiver criando uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="f6297-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="f6297-147">Para uma janela de nível superior, defina como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f6297-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="f6297-148">Para uma janela de aplicativo, o próximo parâmetro define o menu para a janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="f6297-149">Este exemplo não usa um menu, portanto, o valor é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f6297-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="f6297-150">*HINSTANCE* é o identificador de instância, descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f6297-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="f6297-151">(Consulte [WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md).)</span><span class="sxs-lookup"><span data-stu-id="f6297-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="f6297-152">O último parâmetro é um ponteiro para dados arbitrários do **tipo \* void**.</span><span class="sxs-lookup"><span data-stu-id="f6297-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="f6297-153">Você pode usar esse valor para passar uma estrutura de dados para o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="f6297-154">Mostraremos uma maneira possível de usar esse parâmetro na seção [Gerenciando o estado do aplicativo](managing-application-state-.md).</span><span class="sxs-lookup"><span data-stu-id="f6297-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="f6297-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) retornará um identificador para a nova janela ou zero se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="f6297-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="f6297-156">Para mostrar a janela — ou seja, tornar a janela visível — passe o identificador de janela para a função de [**janela**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="f6297-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="f6297-157">O parâmetro *HWND* é o identificador de janela retornado por [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="f6297-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="f6297-158">O parâmetro *nCmdShow* pode ser usado para minimizar ou maximizar uma janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="f6297-159">O sistema operacional passa esse valor para o programa por meio da função **wWinMain** .</span><span class="sxs-lookup"><span data-stu-id="f6297-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="f6297-160">Este é o código completo para criar a janela.</span><span class="sxs-lookup"><span data-stu-id="f6297-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="f6297-161">Lembre-se `WindowProc` de que ainda é apenas uma declaração de encaminhamento de uma função.</span><span class="sxs-lookup"><span data-stu-id="f6297-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
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
```

<span data-ttu-id="f6297-162">Parabéns, você criou uma janela!</span><span class="sxs-lookup"><span data-stu-id="f6297-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="f6297-163">No momento, a janela não contém nenhum conteúdo ou interage com o usuário.</span><span class="sxs-lookup"><span data-stu-id="f6297-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="f6297-164">Em um aplicativo de GUI real, a janela responderia a eventos do usuário e do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f6297-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="f6297-165">A próxima seção descreve como as mensagens de janela fornecem esse tipo de interatividade.</span><span class="sxs-lookup"><span data-stu-id="f6297-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="f6297-166">Avançar</span><span class="sxs-lookup"><span data-stu-id="f6297-166">Next</span></span>

[<span data-ttu-id="f6297-167">Mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="f6297-167">Window Messages</span></span>](window-messages.md)