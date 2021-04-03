---
description: Uma classe de janela é suportada por um procedimento de janela. Seu aplicativo pode registrar uma classe de janela usando a RegisterClassa ou RegisterClassW. Os novos aplicativos normalmente devem usar RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrando classes de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091817"
---
# <a name="registering-window-classes"></a><span data-ttu-id="b09f5-105">Registrando classes de janela</span><span class="sxs-lookup"><span data-stu-id="b09f5-105">Registering Window Classes</span></span>

<span data-ttu-id="b09f5-106">Uma classe de janela é suportada por um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="b09f5-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="b09f5-107">Seu aplicativo pode registrar uma classe de janela usando a [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="b09f5-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="b09f5-108">Os novos aplicativos normalmente devem usar **RegisterClassW**.</span><span class="sxs-lookup"><span data-stu-id="b09f5-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="b09f5-109">Se o aplicativo registrar a classe de janela usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), a função informará ao sistema operacional que as janelas da classe criada esperam mensagens com parâmetros de texto ou caracteres para usar um conjunto de caracteres de [página de código do Windows (ANSI)](code-pages.md) .</span><span class="sxs-lookup"><span data-stu-id="b09f5-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="b09f5-110">O registro usando [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permite que o aplicativo solicite que o sistema operacional passe parâmetros de texto de mensagens como [Unicode](unicode.md).</span><span class="sxs-lookup"><span data-stu-id="b09f5-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="b09f5-111">A função [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite que um aplicativo consulte a natureza de cada janela.</span><span class="sxs-lookup"><span data-stu-id="b09f5-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="b09f5-112">O exemplo a seguir mostra como registrar uma classe de janela de código do Windows e uma classe de janela Unicode e como escrever os procedimentos de janela para ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="b09f5-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="b09f5-113">Para os fins deste exemplo, todas as funções e estruturas são mostradas com os tipos de dados "A" (ANSI) ou "W" (Wide, Unicode) específicos.</span><span class="sxs-lookup"><span data-stu-id="b09f5-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="b09f5-114">Usando as técnicas explicadas em como [usar tipos de dados genéricos](using-generic-data-types.md), você pode, como alternativa, escrever este exemplo para usar tipos de dados genéricos, para que ele possa ser compilado para usar páginas de código do Windows ou Unicode, dependendo se "Unicode" está definido.</span><span class="sxs-lookup"><span data-stu-id="b09f5-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



<span data-ttu-id="b09f5-115">O exemplo a seguir mostra a diferença entre a manipulação da mensagem do [**WM \_ Char**](../inputdev/wm-char.md) em um procedimento de janela de página de código do Windows e um procedimento de janela Unicode.</span><span class="sxs-lookup"><span data-stu-id="b09f5-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



<span data-ttu-id="b09f5-116">Todo texto em mensagens recebidas por **AnsiWndProc** é composto por caracteres de página de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="b09f5-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="b09f5-117">Todo o texto nas mensagens recebidas por **UniWndProc** é composto por caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="b09f5-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b09f5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b09f5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b09f5-119">Usando Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="b09f5-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
