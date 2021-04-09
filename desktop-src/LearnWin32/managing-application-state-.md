---
title: Gerenciando o estado do aplicativo
description: Um procedimento de janela é apenas uma função que é invocada para cada mensagem, portanto, é inerentemente sem estado. Portanto, você precisa de uma maneira de acompanhar o estado do seu aplicativo de uma chamada de função para a próxima.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007523"
---
# <a name="managing-application-state"></a><span data-ttu-id="f9f23-104">Gerenciando o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f9f23-104">Managing Application State</span></span>

<span data-ttu-id="f9f23-105">Um procedimento de janela é apenas uma função que é invocada para cada mensagem, portanto, é inerentemente sem estado.</span><span class="sxs-lookup"><span data-stu-id="f9f23-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="f9f23-106">Portanto, você precisa de uma maneira de acompanhar o estado do seu aplicativo de uma chamada de função para a próxima.</span><span class="sxs-lookup"><span data-stu-id="f9f23-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="f9f23-107">A abordagem mais simples é simplesmente colocar tudo em variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="f9f23-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="f9f23-108">Isso funciona bem suficiente para programas pequenos e muitos dos exemplos de SDK usam essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="f9f23-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="f9f23-109">Em um grande programa, no entanto, ele leva a uma proliferação de variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="f9f23-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="f9f23-110">Além disso, você pode ter várias janelas, cada uma com seu próprio procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="f9f23-111">Manter o controle de qual janela deve acessar quais variáveis se tornam confusas e sujeitas a erros.</span><span class="sxs-lookup"><span data-stu-id="f9f23-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="f9f23-112">A função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) fornece uma maneira de passar qualquer estrutura de dados para uma janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="f9f23-113">Quando essa função é chamada, ela envia as duas mensagens a seguir para o procedimento de janela:</span><span class="sxs-lookup"><span data-stu-id="f9f23-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="f9f23-114">**NCCREATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f9f23-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="f9f23-115">**criação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f9f23-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="f9f23-116">Essas mensagens são enviadas na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="f9f23-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="f9f23-117">(Essas não são as duas únicas mensagens enviadas durante [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), mas podemos ignorar as outras para esta discussão.)</span><span class="sxs-lookup"><span data-stu-id="f9f23-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="f9f23-118">A mensagem de [**\_ criação**](/windows/desktop/winmsg/wm-create) do [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e do WM são enviadas antes que a janela fique visível.</span><span class="sxs-lookup"><span data-stu-id="f9f23-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="f9f23-119">Isso os torna um bom lugar para inicializar sua interface do usuário, por exemplo, para determinar o layout inicial da janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="f9f23-120">O último parâmetro de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) é um ponteiro do tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="f9f23-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="f9f23-121">Você pode passar qualquer valor de ponteiro que desejar nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f9f23-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="f9f23-122">Quando o procedimento de janela manipula a mensagem do [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) ou do [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , ele pode extrair esse valor dos dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f9f23-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="f9f23-123">Vamos ver como você usaria esse parâmetro para passar dados de aplicativo para sua janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="f9f23-124">Primeiro, defina uma classe ou estrutura que contém informações de estado.</span><span class="sxs-lookup"><span data-stu-id="f9f23-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="f9f23-125">Ao chamar [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), passe um ponteiro para essa estrutura no parâmetro final **void \*** .</span><span class="sxs-lookup"><span data-stu-id="f9f23-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

<span data-ttu-id="f9f23-126">Quando você recebe as mensagens do [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e do [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , o parâmetro *lParam* de cada mensagem é um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="f9f23-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="f9f23-127">A estrutura **CREATESTRUCT** , por sua vez, contém o ponteiro passado para [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="f9f23-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![diagrama que mostra o layout da estrutura CREATESTRUCT](images/appstate01.png)

<span data-ttu-id="f9f23-129">Veja como você extrai o ponteiro para sua estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="f9f23-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="f9f23-130">Primeiro, obtenha a estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) convertendo o parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f9f23-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="f9f23-131">O membro **lpCreateParams** da estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) é o ponteiro void original que você especificou em [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="f9f23-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="f9f23-132">Obtenha um ponteiro para sua própria estrutura de dados por meio da conversão de **lpCreateParams**.</span><span class="sxs-lookup"><span data-stu-id="f9f23-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="f9f23-133">Em seguida, chame a função [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) e passe o ponteiro para sua estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="f9f23-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="f9f23-134">A finalidade dessa última chamada de função é armazenar o ponteiro *arquivo stateInfo* nos dados da instância para a janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="f9f23-135">Depois de fazer isso, você sempre poderá obter o ponteiro de volta da janela chamando [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span><span class="sxs-lookup"><span data-stu-id="f9f23-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="f9f23-136">Cada janela tem seus próprios dados de instância, para que você possa criar várias janelas e dar a cada janela sua própria instância da estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="f9f23-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="f9f23-137">Essa abordagem é especialmente útil se você definir uma classe de janelas e criar mais de uma janela dessa classe — por exemplo, se você criar uma classe de controle Personalizada.</span><span class="sxs-lookup"><span data-stu-id="f9f23-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="f9f23-138">É conveniente encapsular a chamada [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) em uma pequena função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f9f23-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="f9f23-139">Agora você pode escrever o procedimento de janela da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f9f23-139">Now you can write your window procedure as follows.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a><span data-ttu-id="f9f23-140">Uma abordagem Object-Oriented</span><span class="sxs-lookup"><span data-stu-id="f9f23-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="f9f23-141">Podemos estender essa abordagem mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="f9f23-141">We can extend this approach further.</span></span> <span data-ttu-id="f9f23-142">Já definimos uma estrutura de dados para manter informações de estado sobre a janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="f9f23-143">Faz sentido fornecer essa estrutura de dados com funções de membro (métodos) que operam nos dados.</span><span class="sxs-lookup"><span data-stu-id="f9f23-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="f9f23-144">Isso, naturalmente, leva a um design onde a estrutura (ou classe) é responsável por todas as operações na janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="f9f23-145">O procedimento de janela então se tornaria parte da classe.</span><span class="sxs-lookup"><span data-stu-id="f9f23-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="f9f23-146">Em outras palavras, gostaríamos de seguir este:</span><span class="sxs-lookup"><span data-stu-id="f9f23-146">In other words, we would like to go from this:</span></span>

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

<span data-ttu-id="f9f23-147">Para isso:</span><span class="sxs-lookup"><span data-stu-id="f9f23-147">To this:</span></span>

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

<span data-ttu-id="f9f23-148">O único problema é como vincular o `MyWindow::WindowProc` método.</span><span class="sxs-lookup"><span data-stu-id="f9f23-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="f9f23-149">A função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) espera que o procedimento de janela seja um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="f9f23-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="f9f23-150">Você não pode passar um ponteiro para uma função de membro (não estático) neste contexto.</span><span class="sxs-lookup"><span data-stu-id="f9f23-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="f9f23-151">No entanto, você pode passar um ponteiro para uma função membro *estática* e, em seguida, delegar para a função membro.</span><span class="sxs-lookup"><span data-stu-id="f9f23-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="f9f23-152">Aqui está um modelo de classe que mostra essa abordagem:</span><span class="sxs-lookup"><span data-stu-id="f9f23-152">Here is a class template that shows this approach:</span></span>

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

<span data-ttu-id="f9f23-153">A `BaseWindow` classe é uma classe base abstrata, da qual classes de janela específicas são derivadas.</span><span class="sxs-lookup"><span data-stu-id="f9f23-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="f9f23-154">Por exemplo, aqui está a declaração de uma classe simples derivada de `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="f9f23-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="f9f23-155">Para criar a janela, chame `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="f9f23-155">To create the window, call `BaseWindow::Create`:</span></span>

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

<span data-ttu-id="f9f23-156">O método virtual puro `BaseWindow::HandleMessage` é usado para implementar o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="f9f23-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="f9f23-157">Por exemplo, a implementação a seguir é equivalente ao procedimento de janela mostrado no início do [módulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="f9f23-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

<span data-ttu-id="f9f23-158">Observe que o identificador de janela é armazenado em uma variável de membro (*m \_ HWND*), portanto, não precisamos passá-lo como um parâmetro para `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="f9f23-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="f9f23-159">Muitas das estruturas de programação existentes do Windows, como MFC (MFC) e Active Template Library (ATL), usam abordagens que são basicamente semelhantes àquelas mostradas aqui.</span><span class="sxs-lookup"><span data-stu-id="f9f23-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="f9f23-160">É claro que uma estrutura totalmente generalizada, como MFC, é mais complexa do que esse exemplo relativamente simplista.</span><span class="sxs-lookup"><span data-stu-id="f9f23-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="f9f23-161">Avançar</span><span class="sxs-lookup"><span data-stu-id="f9f23-161">Next</span></span>

[<span data-ttu-id="f9f23-162">Módulo 2: usando COM em seu programa do Windows</span><span class="sxs-lookup"><span data-stu-id="f9f23-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="f9f23-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9f23-163">Related topics</span></span>

[<span data-ttu-id="f9f23-164">Exemplo de BaseWindow</span><span class="sxs-lookup"><span data-stu-id="f9f23-164">BaseWindow Sample</span></span>](basewindow-sample.md)