---
description: Uma classe de janela é suportada por um procedimento de janela. Seu aplicativo pode registrar uma classe de janela usando RegisterClassA ou RegisterClassW. Novos aplicativos normalmente devem usar RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrando classes de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040446"
---
# <a name="registering-window-classes"></a>Registrando classes de janela

Uma classe de janela é suportada por um procedimento de janela. Seu aplicativo pode registrar uma classe de janela usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassW.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Novos aplicativos normalmente devem usar **RegisterClassW**.

Se o aplicativo registrar a classe de janela usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), a função informará ao sistema operacional que as janelas da classe criada esperam mensagens com parâmetros de texto ou caractere para usar um conjunto de caracteres de página de [código ANSI (Windows).](code-pages.md) O registro [**usando RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) permite que o aplicativo solicite que o sistema operacional passe parâmetros de texto de mensagens como [Unicode.](unicode.md) A [**função IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite que um aplicativo consulte a natureza de cada janela.

O exemplo a seguir mostra como registrar uma classe de Windows de página de código e uma classe de janela Unicode e como escrever os procedimentos de janela para ambos os casos. Para os fins deste exemplo, todas as funções e estruturas são mostradas com os tipos de dados específicos "A" (ANSI) ou "W" (wide, Unicode). Usando as técnicas explicadas em Usando tipos de dados genéricos [,](using-generic-data-types.md)você pode, como alternativa, escrever este exemplo para usar tipos de dados genéricos, para que ele possa ser compilado para usar páginas de código Windows ou Unicode, dependendo se "UNICODE" está definido.


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



O exemplo a seguir mostra a diferença entre lidar com a mensagem [**CHAR \_ WM**](../inputdev/wm-char.md) em um procedimento de janela Windows página de código e um procedimento de janela Unicode.


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



Todo o texto em mensagens **recebidas por AnsiWndProc** é composto por Windows de página de código. Todo o texto em mensagens recebidas **pelo UniWndProc** é composto por caracteres Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
