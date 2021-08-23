---
title: O que é uma janela
description: O que é uma janela?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af5d845d1a7eac6474dec9da08dcfde8df9f9fd67bf16d6f59cad94c5af0fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631400"
---
# <a name="what-is-a-window"></a>O que é uma janela?

## <a name="what-is-a-window"></a>O que é uma janela?

Obviamente, as janelas são centrais para Windows. Eles são tão importantes que nomearam o sistema operacional após eles. Mas o que é uma janela? Ao pensar em uma janela, você provavelmente pensa em algo assim:

![captura de tela de uma janela do aplicativo](images/window01.png)

Esse tipo de janela é chamado de janela *do aplicativo* ou *janela principal.* Normalmente, ele tem um quadro com uma barra de título, **botões Minimizar** **e** Maximizar e outros elementos de interface do usuário padrão. O quadro é chamado *de área não* cliente da janela, assim chamado porque o sistema operacional gerencia essa parte da janela. A área dentro do quadro é a *área do cliente*. Essa é a parte da janela gerenciada pelo programa.

Aqui está outro tipo de janela:

![captura de tela de uma janela de controle](images/window02.png)

Se você não estiver Windows programação, pode ser uma surpresa que os controles de interface do usuário, como botões e caixas de edição, sejam janelas. A principal diferença entre um controle de interface do usuário e uma janela do aplicativo é que um controle não existe por si só. Em vez disso, o controle é posicionado em relação à janela do aplicativo. Quando você arrasta a janela do aplicativo, o controle se move com ela, como você esperaria. Além disso, o controle e a janela do aplicativo podem se comunicar entre si. (Por exemplo, a janela do aplicativo recebe notificações de clique de um botão.)

Portanto, quando você pensa *em janela*, não pense simplesmente em janela *do aplicativo.* Em vez disso, pense em uma janela como um constructo de programação que:

-   Ocupa uma determinada parte da tela.
-   Pode ou não estar visível em um determinado momento.
-   Sabe como desenhar a si mesmo.
-   Responde a eventos do usuário ou do sistema operacional.

## <a name="parent-windows-and-owner-windows"></a>Conta Windows e proprietário Windows

No caso de um controle de interface do usuário, diz-se que a janela de controle é o *filho da* janela do aplicativo. A janela do aplicativo é *o pai* da janela de controle. A janela pai fornece o sistema de coordenadas usado para posicionar uma janela filho. Ter uma janela pai afeta aspectos da aparência de uma janela; por exemplo, uma janela filho é recortada para que nenhuma parte da janela filho possa aparecer fora das bordas de sua janela pai.

Outra relação é a relação entre uma janela de aplicativo e uma janela de diálogo modal. Quando um aplicativo exibe uma caixa de diálogo  modal, a janela do aplicativo é a janela do proprietário e a caixa de diálogo é *uma janela* de propriedade. Uma janela de propriedade sempre aparece na frente de sua janela de proprietário. Ele fica oculto quando o proprietário é minimizado e destruído ao mesmo tempo que o proprietário.

A imagem a seguir mostra um aplicativo que exibe uma caixa de diálogo com dois botões:

![captura de tela de um aplicativo com uma caixa de diálogo](images/window03.png)

A janela do aplicativo possui a janela de diálogo e a janela de diálogo é o pai de ambas as janelas de botão. O diagrama a seguir mostra estas relações:

![ilustração mostrando relações pai/filho e proprietário/propriedade](images/window04.png)

## <a name="window-handles"></a>Alças de janela

Windows são objetos — eles têm código e dados — mas não são classes C++. Em vez disso, um programa referencia uma janela usando um valor chamado de *handle*. Um identificador é um tipo opaco. Essencialmente, é apenas um número que o sistema operacional usa para identificar um objeto . Você pode imaginar Windows como tendo uma tabela grande de todas as janelas que foram criadas. Ele usa essa tabela para procurar janelas pelos respectivos alças. (Se é exatamente assim que funciona internamente não é importante.) O tipo de dados para identificador de janela **é HWND,** que geralmente é pronunciado "aitch-wind". Os alças de janela são retornados pelas funções que criam janelas: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) e [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

Para executar uma operação em uma janela, normalmente você chamará alguma função que aceita um **valor HWND** como um parâmetro. Por exemplo, para reposicionar uma janela na tela, chame a [**função MoveWindow:**](/windows/desktop/api/winuser/nf-winuser-movewindow)


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



O primeiro parâmetro é o alça para a janela que você deseja mover. Os outros parâmetros especificam o novo local da janela e se a janela deve ser redesenhada.

Tenha em mente que os alças não são ponteiros. Se *hwnd for* uma variável que contém um handle, tentar desreferenciar o handle escrevendo `*hwnd` será um erro.

## <a name="screen-and-window-coordinates"></a>Coordenadas de tela e janela

As coordenadas são medidas em pixels independentes do dispositivo. Teremos mais a dizer sobre  a parte independente do dispositivo de *pixels* independentes de dispositivo quando discutirmos gráficos.

Dependendo da tarefa, você pode medir coordenadas em relação à tela, em relação a uma janela (incluindo o quadro) ou em relação à área do cliente de uma janela. Por exemplo, você posicionaria uma janela na tela usando coordenadas de tela, mas desenharia dentro de uma janela usando as coordenadas do cliente. Em cada caso, a origem (0, 0) é sempre o canto superior esquerdo da região.

![ilustração mostrando a tela, a janela e as coordenadas do cliente](images/coordinates01.png)

## <a name="next"></a>Avançar

[WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md)

 

 
