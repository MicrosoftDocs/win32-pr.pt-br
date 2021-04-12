---
title: Definindo a imagem do cursor
description: Definindo a imagem do cursor
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454009"
---
# <a name="setting-the-cursor-image"></a>Definindo a imagem do cursor

O *cursor* é a imagem pequena que mostra o local do mouse ou outro dispositivo apontador. Muitos aplicativos alteram a imagem do cursor para fornecer comentários ao usuário. Embora não seja necessário, ele adiciona um pouco de polonês ao seu aplicativo.

O Windows fornece um conjunto de imagens de cursor padrão, chamadas *cursores do sistema*. Isso inclui a seta, a mão, o I-feixe, a ampulheta (que agora é um círculo girando) e outros. Esta seção descreve como usar os cursores do sistema. Para tarefas mais avançadas, como a criação de cursores personalizados, consulte [cursores](/windows/desktop/menurc/cursors).

Você pode associar um cursor a uma classe de janela definindo o membro **hCursor** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Caso contrário, o cursor padrão será a seta. Quando o mouse se move sobre uma janela, a janela recebe uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) (a menos que outra janela tenha capturado o mouse). Neste ponto, ocorre um dos seguintes eventos:

-   O aplicativo define o cursor e o procedimento de janela retorna **true**.
-   O aplicativo não faz nada e passa o [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Para definir o cursor, um programa faz o seguinte:

1.  Chama [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) para carregar o cursor na memória. Essa função retorna um identificador para o cursor.
2.  Chama [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) e passa na alça do cursor.

Caso contrário, se o aplicativo passar o [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), a função **DefWindowProc** usará o seguinte algoritmo para definir a imagem do cursor:

1.  Se a janela tiver um pai, encaminhe a mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para o pai a ser manipulado.
2.  Caso contrário, se a janela tiver um cursor de classe, defina o cursor para o cursor de classe.
3.  Se não houver um cursor de classe, defina o cursor para o cursor de seta.

A função [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) pode carregar um cursor personalizado de um recurso ou um dos cursores do sistema. O exemplo a seguir mostra como definir o cursor para o cursor da mão do sistema.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Se você alterar o cursor, a imagem do cursor será redefinida na próxima movimentação do mouse, a menos que você intercepte a mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) e defina o cursor novamente. O código a seguir mostra como manipular o **WM \_ SetCursor**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Esse código primeiro verifica os 16 bits inferiores de *lParam*. Se for `LOWORD(lParam)` igual a **HTCLIENT**, significa que o cursor está sobre a área do cliente da janela. Caso contrário, o cursor está sobre a área que não é do cliente. Normalmente, você só deve definir o cursor para a área do cliente e deixar o Windows definir o cursor para a área não cliente.

## <a name="next"></a>Avançar

[Entrada do usuário: exemplo estendido](user-input--extended-example.md)

 

 