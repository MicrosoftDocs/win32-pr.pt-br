---
title: Como criar um link de comando
description: Este tópico descreve uma maneira de criar um link de comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454401"
---
# <a name="how-to-create-a-command-link"></a>Como criar um link de comando

Este tópico descreve uma maneira de criar um link de comando.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Etapa 1: criar uma instância do botão de link de comando.

No exemplo de código C++ a seguir, a constante de estilo [**BS \_ COMMANDLINK**](button-styles.md) especifica o botão como um botão de link de comando.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Etapa 2: definir o rótulo de link de comando e o texto de explicação

Use a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para definir o rótulo do link de comando e o texto suplementar por meio da mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e da mensagem do [**BCM \_ setnote**](bcm-setnote.md) , respectivamente.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os botões](about-buttons.md)
</dt> <dt>

[Referência de controle de botão](bumper-button-button-control-reference.md)
</dt> <dt>

[Usando botões](using-buttons.md)
</dt> <dt>

[Botão](buttons.md)
</dt> </dl>

 

 