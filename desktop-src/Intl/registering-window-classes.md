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
# <a name="registering-window-classes"></a>Registrando classes de janela

Uma classe de janela é suportada por um procedimento de janela. Seu aplicativo pode registrar uma classe de janela usando a [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa). Os novos aplicativos normalmente devem usar **RegisterClassW**.

Se o aplicativo registrar a classe de janela usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), a função informará ao sistema operacional que as janelas da classe criada esperam mensagens com parâmetros de texto ou caracteres para usar um conjunto de caracteres de [página de código do Windows (ANSI)](code-pages.md) . O registro usando [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permite que o aplicativo solicite que o sistema operacional passe parâmetros de texto de mensagens como [Unicode](unicode.md). A função [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite que um aplicativo consulte a natureza de cada janela.

O exemplo a seguir mostra como registrar uma classe de janela de código do Windows e uma classe de janela Unicode e como escrever os procedimentos de janela para ambos os casos. Para os fins deste exemplo, todas as funções e estruturas são mostradas com os tipos de dados "A" (ANSI) ou "W" (Wide, Unicode) específicos. Usando as técnicas explicadas em como [usar tipos de dados genéricos](using-generic-data-types.md), você pode, como alternativa, escrever este exemplo para usar tipos de dados genéricos, para que ele possa ser compilado para usar páginas de código do Windows ou Unicode, dependendo se "Unicode" está definido.


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



O exemplo a seguir mostra a diferença entre a manipulação da mensagem do [**WM \_ Char**](../inputdev/wm-char.md) em um procedimento de janela de página de código do Windows e um procedimento de janela Unicode.


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



Todo texto em mensagens recebidas por **AnsiWndProc** é composto por caracteres de página de código do Windows. Todo o texto nas mensagens recebidas por **UniWndProc** é composto por caracteres Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
