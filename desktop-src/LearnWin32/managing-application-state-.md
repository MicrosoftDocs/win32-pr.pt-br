---
title: Gerenciando o estado do aplicativo
description: Um procedimento de janela é apenas uma função que é invocada para cada mensagem, portanto, é inerentemente sem estado. Portanto, você precisa de uma maneira de acompanhar o estado do seu aplicativo de uma chamada de função para a próxima.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068056"
---
# <a name="managing-application-state"></a>Gerenciando o estado do aplicativo

Um procedimento de janela é apenas uma função que é invocada para cada mensagem, portanto, é inerentemente sem estado. Portanto, você precisa de uma maneira de acompanhar o estado do seu aplicativo de uma chamada de função para a próxima.

A abordagem mais simples é simplesmente colocar tudo em variáveis globais. Isso funciona bem suficiente para programas pequenos e muitos dos exemplos de SDK usam essa abordagem. Em um grande programa, no entanto, ele leva a uma proliferação de variáveis globais. Além disso, você pode ter várias janelas, cada uma com seu próprio procedimento de janela. Manter o controle de qual janela deve acessar quais variáveis se tornam confusas e sujeitas a erros.

A função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) fornece uma maneira de passar qualquer estrutura de dados para uma janela. Quando essa função é chamada, ela envia as duas mensagens a seguir para o procedimento de janela:

- [**NCCREATE do WM \_**](/windows/desktop/winmsg/wm-nccreate)
- [**criação do WM \_**](/windows/desktop/winmsg/wm-create)

Essas mensagens são enviadas na ordem listada. (Essas não são as duas únicas mensagens enviadas durante [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), mas podemos ignorar as outras para esta discussão.)

A mensagem de [**\_ criação**](/windows/desktop/winmsg/wm-create) do [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e do WM são enviadas antes que a janela fique visível. Isso os torna um bom lugar para inicializar sua interface do usuário, por exemplo, para determinar o layout inicial da janela.

O último parâmetro de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) é um ponteiro do tipo **void \** _. Você pode passar qualquer valor de ponteiro que desejar nesse parâmetro. Quando o procedimento de janela manipula a mensagem de [**\_ criação**](/windows/desktop/winmsg/wm-create) [_ * *WM \_ NCCREATE*](/windows/desktop/winmsg/wm-nccreate) ou WM, ele pode extrair esse valor dos dados da mensagem.

Vamos ver como você usaria esse parâmetro para passar dados de aplicativo para sua janela. Primeiro, defina uma classe ou estrutura que contém informações de estado.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Ao chamar [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), passe um ponteiro para essa estrutura no parâmetro final **void \*** .

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

Quando você recebe as mensagens do [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e do [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , o parâmetro *lParam* de cada mensagem é um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . A estrutura **CREATESTRUCT** , por sua vez, contém o ponteiro passado para [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

![diagrama que mostra o layout da estrutura CREATESTRUCT](images/appstate01.png)

Veja como você extrai o ponteiro para sua estrutura de dados. Primeiro, obtenha a estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) convertendo o parâmetro *lParam* .

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

O membro **lpCreateParams** da estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) é o ponteiro void original que você especificou em [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Obtenha um ponteiro para sua própria estrutura de dados por meio da conversão de **lpCreateParams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Em seguida, chame a função [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) e passe o ponteiro para sua estrutura de dados.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

A finalidade dessa última chamada de função é armazenar o ponteiro *arquivo stateInfo* nos dados da instância para a janela. Depois de fazer isso, você sempre poderá obter o ponteiro de volta da janela chamando [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Cada janela tem seus próprios dados de instância, para que você possa criar várias janelas e dar a cada janela sua própria instância da estrutura de dados. Essa abordagem é especialmente útil se você definir uma classe de janelas e criar mais de uma janela dessa classe — por exemplo, se você criar uma classe de controle Personalizada. É conveniente encapsular a chamada [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) em uma pequena função auxiliar.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Agora você pode escrever o procedimento de janela da seguinte maneira.

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

## <a name="an-object-oriented-approach"></a>Uma abordagem Object-Oriented

Podemos estender essa abordagem mais detalhadamente. Já definimos uma estrutura de dados para manter informações de estado sobre a janela. Faz sentido fornecer essa estrutura de dados com funções de membro (métodos) que operam nos dados. Isso, naturalmente, leva a um design onde a estrutura (ou classe) é responsável por todas as operações na janela. O procedimento de janela então se tornaria parte da classe.

Em outras palavras, gostaríamos de seguir este:

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

Para isso:

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

O único problema é como vincular o `MyWindow::WindowProc` método. A função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) espera que o procedimento de janela seja um ponteiro de função. Você não pode passar um ponteiro para uma função de membro (não estático) neste contexto. No entanto, você pode passar um ponteiro para uma função membro *estática* e, em seguida, delegar para a função membro. Aqui está um modelo de classe que mostra essa abordagem:

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

A `BaseWindow` classe é uma classe base abstrata, da qual classes de janela específicas são derivadas. Por exemplo, aqui está a declaração de uma classe simples derivada de `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Para criar a janela, chame `BaseWindow::Create` :

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

O método virtual puro `BaseWindow::HandleMessage` é usado para implementar o procedimento de janela. Por exemplo, a implementação a seguir é equivalente ao procedimento de janela mostrado no início do [módulo 1](your-first-windows-program.md).

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

Observe que o identificador de janela é armazenado em uma variável de membro (*m \_ HWND*), portanto, não precisamos passá-lo como um parâmetro para `HandleMessage` .

muitas das estruturas de programação Windows existentes, como MFC (MFC) e Active Template Library (ATL), usam abordagens que são basicamente semelhantes àquelas mostradas aqui. É claro que uma estrutura totalmente generalizada, como MFC, é mais complexa do que esse exemplo relativamente simplista.

## <a name="next"></a>Avançar

[módulo 2: usando com em seu programa de Windows](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de BaseWindow](basewindow-sample.md)