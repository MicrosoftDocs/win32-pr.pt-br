---
title: Pré-requisitos para o desenvolvimento com DirectX
description: Ao começar a desenvolver um aplicativo do Windows usando o DirectX, mantenha os pré-requisitos nessa página em mente. Isso inclui as tecnologias que você precisa saber antes de se aprofundar.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicativo DirectX, pré-requisitos
- Aplicativo DirectX, aplicativo da Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/16/2020
ms.locfileid: "104454480"
---
# <a name="prerequisites-for-developing-with-directx"></a>Pré-requisitos para o desenvolvimento com DirectX

Ao começar a desenvolver um aplicativo do Windows usando o DirectX, mantenha os pré-requisitos nessa página em mente. Isso inclui as tecnologias que você precisa saber antes de se aprofundar.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>O que devo saber para desenvolver um jogo do Windows usando o DirectX?

Antes de começar a desenvolver um aplicativo da Windows Store usando o DirectX, você precisa saber como programar no Windows com o C++. Os aplicativos do Windows que usam o DirectX são desenvolvidos em um nível baixo de programação, o que significa que você será exposto a muitos recursos do sistema operacional. Isso inclui memória e gerenciamento de recursos e a interface para o próprio dispositivo de gráficos. Se você for novo no desenvolvimento de aplicativos gráficos ou de jogos, poderá achar esse desafio. Mas você também encontrará a gratificação de ti, pois o aprendizado do desenvolvimento de jogos nesse nível cria possibilidades muito mais distantes para design e desenvolvimento de aplicativos gráficos e jogos.

Você também precisará compreender as noções básicas de programação de gráficos 2D e 3D e matemática, pois muitas das APIs que você usaram foram desenvolvidas com esses princípios em mente. Será mais fácil entender seus parâmetros e resultados se você estiver familiarizado com as operações por trás deles.

No mínimo, você deve ter uma noção do seguinte:

-   Programação C/C++ do Windows. Isso significa que você entende ponteiros e referências, eventos e retornos de chamada, e talvez algumas das bibliotecas comuns, como a ATL.
-   Programação do Win32. Você entende como o Windows é criado e como os eventos da interface do usuário são processados. Você também entende um pouco sobre o COM e as APIs do Win32 essenciais.
-   Algebra linear e trigonometria. Embora não seja essencial, você terá um tempo mais fácil se estiver familiarizado com os conceitos dessas duas disciplinas matemáticas, pois elas são a base de grande parte da programação de gráficos 3D.
-   Terminologia e conceitos básicos de gráficos, como bitmaps, texturas, vértices, malhas e visores.

## <a name="what-does-directx-provide-me"></a>O que o DirectX fornece?

O DirectX é o principal conjunto de APIs de gráficos que você usará para desenvolver jogos do Windows. Aqui estão as categorias de recursos com os quais você deve se familiarizar quando decidir como desenvolver seu jogo.



| Biblioteca     | Descrição                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Um conjunto avançado, orientado por desempenho e acelerado por hardware de bibliotecas para renderizar gráficos 3D.                                              |
| Direct2D    | Um conjunto de bibliotecas gráficas 2D para bitmap com aceleração de hardware e desenho 2D de vetor.                                                           |
| DirectXMath | Uma biblioteca de operações matemáticas comuns e otimizadas usadas em gráficos 2D e 3D, como operações de vetor e matriz.                                |
| DirectWrite | Uma biblioteca de APIs de renderização e layout de texto 2D. Ele dá suporte à aceleração de hardware e à rasterização de software.                              |
| XAudio2     | Uma API de áudio de plataforma cruzada de baixo nível para o Microsoft Windows que fornece processamento de sinal e base de mixagem de áudio para desenvolvimento de jogos. |
| XInput      | Uma biblioteca que dá suporte a vários controles de jogos tradicionais, com ênfase no modelo de controlador do Xbox 360.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Quais ferramentas preciso para desenvolver um jogo do Windows com o DirectX?

Para começar a usar este tutorial, você precisará de:

-   Windows 8.1 ou superior
-   Microsoft Visual Studio 2013 ou superior

 

 




