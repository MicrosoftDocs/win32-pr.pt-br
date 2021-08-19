---
title: Pré-requisitos para o desenvolvimento com o DirectX
description: Quando você começar a desenvolver um Windows usando o DirectX, lembre-se dos pré-requisitos nesta página. Isso inclui as tecnologias que você precisa conhecer antes de se a fundo.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicativo DirectX, pré-requisitos
- Aplicativo DirectX, Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c575fc24da5632582e30b9786d8c800161e5ad1a1cfbc765aa5ec33db3f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950986"
---
# <a name="prerequisites-for-developing-with-directx"></a>Pré-requisitos para o desenvolvimento com o DirectX

Quando você começar a desenvolver um Windows usando o DirectX, lembre-se dos pré-requisitos nesta página. Isso inclui as tecnologias que você precisa conhecer antes de se a fundo.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>O que devo saber para desenvolver um jogo Windows usando o DirectX?

Antes de começar a desenvolver um aplicativo Windows Store usando o DirectX, você precisa saber como programar em Windows com C++. Windows aplicativos que usam o DirectX são desenvolvidos em um nível baixo de programação, o que significa que você será exposto a muitos recursos do sistema operacional. Isso inclui o gerenciamento de recursos e memória e a interface do próprio dispositivo gráfico. Se você for novo no desenvolvimento de jogos ou aplicativos gráficos, poderá achar isso desafiador. Mas você também o achará interessante, pois aprender o desenvolvimento de jogos nesse nível cria possibilidades muito maiores para design e desenvolvimento de aplicativos gráficos e jogos.

Você também precisará entender os conceitos básicos da programação e matemática de elementos gráficos 2D e 3D, pois muitas das APIs que você usará foram desenvolvidas com esses princípios em mente. Será mais fácil entender os parâmetros e os resultados deles se você estiver familiarizado com as operações por trás deles.

No mínimo, você deve ter uma compreensão do seguinte:

-   Windows Programação em C/C++. Isso significa que você entende ponteiros e referências, eventos e retornos de chamada e talvez algumas das bibliotecas comuns, como a ATL.
-   Programação win32. Você entende como as janelas são criadas e como os eventos de interface do usuário são processados. Você também entende um pouco sobre o COM e as APIs essenciais do Win32.
-   Álgebra linear e trigonometria. Embora não seja essencial, você terá um tempo mais fácil se estiver familiarizado com os conceitos dessas duas disciplinas matemáticas, pois elas são a base de grande parte da programação gráfica 3D.
-   Conceitos e terminologia de elementos gráficos básicos, como bitmaps, texturas, vértices, malhas e viewports.

## <a name="what-does-directx-provide-me"></a>O que o DirectX me fornece?

O DirectX é o principal conjunto de APIs de gráficos que você usará para desenvolver Windows jogos. Aqui estão as categorias de recursos com as quais você deve se familiarizar quando decidir como desenvolver seu jogo.



| Biblioteca     | Descrição                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Um conjunto avançado, orientado ao desempenho e acelerado por hardware de bibliotecas para renderizar gráficos 3D.                                              |
| Direct2D    | Um conjunto de bibliotecas de gráficos 2D para bitmap acelerado por hardware e desenho 2D de vetor.                                                           |
| DirectXMath | Uma biblioteca de operações matemáticas comuns e otimizadas usadas em gráficos 2D e 3D, como operações de vetor e matriz.                                |
| DirectWrite | Uma biblioteca de APIs de layout e renderização de texto 2D. Ele dá suporte à aceleração de hardware e à rasterização de software.                              |
| XAudio2     | Uma API de áudio de baixo nível e plataforma cruzada para o Microsoft Windows que fornece uma base de processamento de sinal e combinação de áudio para desenvolvimento de jogos. |
| XInput      | Uma biblioteca que dá suporte a vários controles de jogos tradicionais, com ênfase no modelo Xbox 360 controlador.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Quais ferramentas preciso para desenvolver um jogo Windows com o DirectX?

Para começar a trabalhar com este tutorial, você precisa de:

-   Windows 8.1 ou superior
-   Microsoft Visual Studio 2013 ou superior

 

 




