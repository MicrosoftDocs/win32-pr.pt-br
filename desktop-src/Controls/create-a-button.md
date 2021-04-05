---
title: Como criar um botão
description: Para criar botões dinamicamente, use a função CreateWindow ou CreateWindowEx. Este tópico demonstra como usar a função CreateWindow para criar um botão de ação padrão.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008628"
---
# <a name="how-to-create-a-button"></a>Como criar um botão

Para criar botões dinamicamente, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Este tópico demonstra como usar a função **CreateWindow** para criar um botão de ação padrão.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para criar um controle de botão.

No exemplo de C++ a seguir, o parâmetro de *\_ HWND m* é o identificador para a janela pai. O estilo de [**\_ DEFPUSHBUTTON BS**](button-styles.md) especifica que um botão de push padrão deve ser criado. Observe que os valores de tamanho e posição devem ser especificados porque o uso de **\_ USEDEFAULT de PV** para um botão define os valores como zero.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
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

 

 