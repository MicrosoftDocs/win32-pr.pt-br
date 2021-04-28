---
title: O que é uma janela
description: O que é uma janela?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8494738e3985f78930549f313cb2868b79b34f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103844"
---
# <a name="what-is-a-window"></a>O que é uma janela?

## <a name="what-is-a-window"></a>O que é uma janela?

Obviamente, as janelas são fundamentais para o Windows. Eles são tão importantes que chamaram o sistema operacional depois deles. Mas o que é uma janela? Quando você considera uma janela, provavelmente imagina algo assim:

![captura de tela de uma janela de aplicativo](images/window01.png)

Esse tipo de janela é chamado de *janela de aplicativo* ou *janela principal*. Normalmente, ele tem um quadro com uma barra de título, os botões **minimizar** e **maximizar** e outros elementos padrão da interface do usuário. O quadro é chamado de *área não cliente* da janela, portanto chamado porque o sistema operacional gerencia essa parte da janela. A área dentro do quadro é a *área do cliente*. Essa é a parte da janela que seu programa gerencia.

Aqui está outro tipo de janela:

![captura de tela de uma janela de controle](images/window02.png)

Se você for novo na programação do Windows, poderá surpreender que os controles da interface do usuário, como botões e caixas de edição, sejam as mesmas janelas. A principal diferença entre um controle de interface do usuário e uma janela de aplicativo é que um controle não existe por si só. Em vez disso, o controle é posicionado em relação à janela do aplicativo. Quando você arrasta a janela do aplicativo, o controle se move com ela, como esperado. Além disso, o controle e a janela do aplicativo podem se comunicar entre si. (Por exemplo, a janela do aplicativo recebe notificações de clique de um botão.)

Portanto, quando você considera a *janela*, não considere simplesmente a *janela do aplicativo*. Em vez disso, considere uma janela como um constructo de programação que:

-   Ocupa uma determinada parte da tela.
-   Pode ou não estar visível em um determinado momento.
-   Sabe como desenhar a si mesmo.
-   Responde a eventos do usuário ou do sistema operacional.

## <a name="parent-windows-and-owner-windows"></a>Janelas pai e Windows proprietário

No caso de um controle de interface do usuário, a janela de controle é chamada de *filho* da janela do aplicativo. A janela do aplicativo é o *pai* da janela de controle. A janela pai fornece o sistema de coordenadas usado para posicionar uma janela filho. Ter uma janela pai afeta os aspectos da aparência de uma janela; por exemplo, uma janela filho é recortada para que nenhuma parte da janela filho possa aparecer fora das bordas de sua janela pai.

Outra relação é a relação entre uma janela de aplicativo e uma janela de diálogo modal. Quando um aplicativo exibe uma caixa de diálogo modal, a janela do aplicativo é a janela do *proprietário* e a caixa de diálogo é uma janela de *Propriedade* . Uma janela de propriedade sempre aparece na frente de sua janela do proprietário. Ele fica oculto quando o proprietário é minimizado e é destruído ao mesmo tempo que o proprietário.

A imagem a seguir mostra um aplicativo que exibe uma caixa de diálogo com dois botões:

![captura de tela de um aplicativo com uma caixa de diálogo](images/window03.png)

A janela do aplicativo é proprietária da janela de diálogo e a janela de diálogo é pai de ambas as janelas de botão. O diagrama a seguir mostra essas relações:

![ilustração mostrando pai/filho e relações de propriedade/proprietário](images/window04.png)

## <a name="window-handles"></a>Identificadores de janela

O Windows são objetos — eles têm código e dados, mas não são classes C++. Em vez disso, um programa faz referência a uma janela usando um valor chamado *identificador*. Um identificador é um tipo opaco. Essencialmente, é apenas um número que o sistema operacional usa para identificar um objeto. Você pode fazer com que as janelas de imagem tenham uma grande tabela de todas as janelas que foram criadas. Ele usa essa tabela para pesquisar as janelas por seus identificadores. (Quer seja exatamente como ele funciona internamente não é importante.) O tipo de dados para identificadores de janela é **HWND**, que geralmente é pronunciado "Aitch-Wind". Os identificadores de janela são retornados pelas funções que criam Windows: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) e [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

Para executar uma operação em uma janela, você normalmente chamará alguma função que usa um valor de **HWND** como parâmetro. Por exemplo, para reposicionar uma janela na tela, chame a função [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) :


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



O primeiro parâmetro é o identificador para a janela que você deseja mover. Os outros parâmetros especificam o novo local da janela e se a janela deve ser redesenhada.

Tenha em mente que os identificadores não são ponteiros. Se *HWND* for uma variável que contém um identificador, a tentativa de desreferenciar o identificador por gravação `*hwnd` será um erro.

## <a name="screen-and-window-coordinates"></a>Coordenadas de tela e janela

As coordenadas são medidas em pixels independentes de dispositivo. Teremos mais a dizer sobre a parte *independente do dispositivo* de *pixels independentes de dispositivo* quando discutimos gráficos.

Dependendo da sua tarefa, você pode medir as coordenadas em relação à tela, em relação a uma janela (incluindo o quadro) ou em relação à área do cliente de uma janela. Por exemplo, você posicionaria uma janela na tela usando coordenadas de tela, mas desenharia dentro de uma janela usando coordenadas de cliente. Em cada caso, a origem (0, 0) é sempre o canto superior esquerdo da região.

![ilustração mostrando coordenadas de tela, janela e cliente](images/coordinates01.png)

## <a name="next"></a>Avançar

[WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md)

 

 
