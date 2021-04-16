---
title: Como recuperar e definir uma tecla de atalho
description: Este tópico demonstra como recuperar ou definir a combinação de teclas para um controle de tecla de atalho.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105750313"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Como recuperar e definir uma tecla de atalho

Este tópico demonstra como recuperar ou definir a combinação de teclas para um controle de tecla de atalho. A [**mensagem \_ settecla hkm**](hkm-sethotkey.md) permite que um aplicativo defina a combinação de teclas de acesso para um controle de tecla de atalho. Os aplicativos usam a mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) para recuperar o código de chave virtual e os sinalizadores de modificador da tecla de atalho escolhida pelo usuário.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Use a mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) para recuperar o código de chave virtual e as chaves de modificador que descrevem uma tecla de atalho escolhida pelo usuário. Use a mensagem [**hkm \_ autotecla**](hkm-sethotkey.md) para definir esses valores para uma tecla de acesso.

No exemplo de código C++ a seguir, a função definida pelo aplicativo usa a mensagem [**hkm \_ gettecla de atalho**](hkm-gethotkey.md) para recuperar uma combinação de teclas de um controle de tecla quente e, em seguida, usa a mensagem de [**\_ settecla do WM**](/windows/desktop/inputdev/wm-sethotkey) para definir uma tecla de acesso global. Observe que você não pode definir uma tecla de acesso global para uma janela que tenha o estilo de janela [**\_ filho do WS**](/windows/desktop/winmsg/window-styles) .



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de teclas de acesso](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Sobre os controles de tecla de atalho](hot-key-controls.md)
</dt> <dt>

[Usando controles de tecla quente](using-hot-key-controls.md)
</dt> </dl>

 

 