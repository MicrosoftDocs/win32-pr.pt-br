---
title: Experiência do usuário intuitiva
description: Pela primeira vez, o Windows 7 permite que os desenvolvedores e seus usuários finais controlem seus computadores tocando na tela.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641644"
---
# <a name="intuitive-user-experience"></a>Experiência do usuário intuitiva

Pela primeira vez, o Windows 7 permite que os desenvolvedores e seus usuários finais controlem seus computadores tocando na tela. Os recursos de toque e multitoque fornecem uma maneira natural e intuitiva para que os usuários interajam com PCs. A plataforma de desenvolvedor inclui APIs de gesto de alto nível, bem como mensagens de toque de baixo nível e APIs de entrada por toque. Os elementos da interface de usuário de nível superior, como o menu *Iniciar* e a *barra de tarefas*, têm destinos maiores do que as versões anteriores do Windows, facilitando a seleção com um dedo em vez de um mouse. Os comentários visuais são fornecidos para toque e toque duplo. O Windows Explorer e o Windows Internet Explorer 8 são amigáveis para toque e facilmente integrados a aplicativos do Windows 7.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Gestos de multitoque e APIs de manipulação e inércia

Os recursos do Windows 7 têm suporte aprimorado para toque e gesto, capacitando os desenvolvedores a criarem com rapidez e facilidade experiências de aplicativos exclusivas que vão além do ponteiro simples, clicando e arrastando. As novas APIs multitoque oferecem suporte a gestos avançados, como panorâmica, zoom e rotação. Todos os gestos fornecem comentários visuais diretos e interagem com o conteúdo subjacente de maneira natural e intuitiva. Por exemplo, um gesto de zoom centraliza a exibição no local do gesto. As APIs de entrada por toque de nível inferior também estão disponíveis para a definição de gestos personalizados e experiências avançadas de resposta a toque. O Windows 7 fornece uma plataforma de desenvolvimento que fornece aos desenvolvedores as ferramentas de que eles precisam para desenvolver aplicativos criativos para dispositivos de entrada multitoque, processando a entrada do usuário de dispositivos multitoque e melhorando a interface do usuário. O resultado são ambientes mais intuitivos, que permitem inovações em interação com o PC.

O Windows 7 também fornece suporte de plataforma para manipulação de objetos e processamento de inércia. Um rico conjunto de funções de manipulação permite ampliar, redimensionar ou girar vários objetos simultaneamente e em granularidade muito fina. Por exemplo, várias fotografias digitais podem ser cortadas, redimensionadas e giradas em uma única sessão usando gestos baseados em toque.

O Windows 7 inclui APIs inércia que simulam inércia quando os objetos são movidos, trabalhando em conjunto com as APIs de manipulação. Por exemplo, em um aplicativo de fotos, você pode usar as APIs de manipulação para permitir que os usuários girem, redimensionem e movam fotos. Da mesma forma, se um usuário "joga" uma foto, as APIs do inércia fornecem interação natural e permitem que a foto se costa em uma parada ou salte das bordas da janela do aplicativo. (Consulte [Guia de programação do Windows Touch](../wintouch/programming-guide.md) e [Windows Touch: recursos do desenvolvedor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch).)

## <a name="single-finger-panning"></a>Single-Finger panorâmica

Em muitos aplicativos comuns, os recursos de toque são mais úteis para navegação do que para seleção de texto. Com as APIs de toque estendido, o aplicativo de um desenvolvedor pode optar por habilitar o movimento panorâmico em vez de arrastar. Por exemplo, se você criou um aplicativo que usa gestos multitoque para usuários que executam música, pode permitir que esses usuários simplesmente deslizem um dedo para cima ou para baixo para ajustar o volume, alterar músicas ou baixar um arquivo. Nenhuma rolagem é necessária.

O Windows 7 fornece oportunidades infinitas para desenvolvedores interessados em criar aplicativos para PCs de última geração. O melhor de tudo é que o trabalho árduo de verificar barras de rolagem e implementar a semântica de panorâmica. Os aplicativos também recebem um conjunto mais rico de eventos e comentários para o controle personalizado de gestos do que nas versões anteriores do Windows. (Consulte [aprimorando a experiência de panorâmica Single-Finger](../wintouch/improving-the-single-finger-panning-experience.md).)

## <a name="raw-touch-input-data"></a>Dados de entrada de toque bruto

No Windows 7, novas experiências de toque são habilitadas por modelos de interação que acessam mensagens de entrada por toque de nível inferior e fornecem respostas personalizadas para combinações de mensagens de toque. A plataforma dá suporte ao recebimento de dados de entrada de toque bruto para cenários como aplicativos de pintura multitoque e gestos personalizados dentro de um aplicativo. Você pode usar o suporte de plataforma para toque ou criar suas próprias experiências de multitoque originais. (Consulte [a \_ mensagem de toque do WM](../wintouch/wm-touchdown.md).)

 

 