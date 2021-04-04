---
title: Escolhendo a abordagem certa para o Windows Touch
description: Esta seção explica as diferentes abordagens para o Windows Touch que você pode usar.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Touch, abordagens diferentes
- Windows Touch, escolhendo abordagens
- Windows Touch, aprimorando aplicativos
- Windows Touch, suporte a zoom
- Windows Touch, suporte herdado
- Windows Touch, plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007924"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Escolhendo a abordagem certa para o Windows Touch

Esta seção explica as diferentes abordagens para o Windows Touch que você pode usar.

Você pode aprimorar os aplicativos usando os recursos do Windows Touch de várias maneiras. Antes de adotar um método, você deve considerar o que deseja fazer com seu aplicativo. Os cenários a seguir são típicos para o Windows Touch:

-   Você quer que seu aplicativo se comporte da mesma forma que nas versões herdadas do Windows, mas quer que as mensagens do Windows Touch se comportem de forma consistente.
-   Você deseja rotação de objetos personalizados, tradução, panorâmica ou suporte a zoom em seu aplicativo.
-   Você quer que seu aplicativo tenha uma interpretação refinada dos gestos de toque do Windows ou para interpretar vários toques em um aplicativo que é especificamente otimizado para entrada de toque do Windows.
-   Você tem um aplicativo que usa o objeto [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) e deseja aprimorá-lo com os recursos de toque do Windows.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Você quer que seu aplicativo se comporte como fazia em versões herdadas do Windows

No Windows 7, os aplicativos, por padrão, geram mensagens que habilitam a funcionalidade de toque do Windows. Por exemplo, gestos de Pan disparam \_ \* mensagens de rolagem do WM. Além do suporte a Pan, o manipulador de \_ gestos padrão do WM no Windows 7 dá suporte a comentários de limite, zoom e pressionar e tocar. Os comentários de limite também são habilitados por meio do suporte herdado. Consulte a [visão geral dos gestos de toque do Windows](windows-touch-gestures-overview.md) para obter mais informações sobre como os gestos são mapeados para mensagens. Os desenvolvedores que desejam apenas essa funcionalidade básica não precisam trabalhar diretamente com a API de toque do Windows.

> [!Note]  
> Os manipuladores de barra de rolagem personalizada devem dar suporte à solicitação **SM \_ THUMBPOSITION** para mensagens do **WM \_ VSCROLL** e devem dar suporte à solicitação **\_ LINELEFT SB** e solicitação de **\_ LINERIGHT SB** para mensagens do **WM \_ HSCROLL** .

 

-   A seção [suporte herdado para movimento panorâmico com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) explica como garantir que seu aplicativo se comporta conforme os usuários esperam no Windows 7.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Você deseja rotação de objetos personalizados, tradução, panorâmica ou suporte a zoom

Se você quiser suporte limitado para toque, mas o comportamento padrão oferecido pelo Windows 7 não for adequado para seu aplicativo, você poderá usar gestos para aprimorar seu aplicativo. Usando gestos, você pode interpretar os comandos de gestos manipulando a mensagem de [**\_ gesto do WM**](wm-gesture.md) . Mais informações sobre gestos podem ser encontradas na seção [gestos do Windows Touch](guide-multi-touch-gestures.md). Se seu aplicativo precisar de suporte apenas para rotações de alta granularidade, suporte aprimorado de zoom ou movimento panorâmico de um único dedo, gestos é a melhor abordagem a ser tomada para o desenvolvimento de toque do Windows. Além de interpretar a mensagem de gesto, você pode optar por ter suporte para comentários de limite. Para obter mais informações sobre comentários de limite, consulte a seção de [comentários sobre limites](boundary-feedback.md) da referência de [programação do Windows Touch](windows-touch-programming-reference.md). No Windows 7, o prompt de comando e o Internet Explorer aproveitam os comentários e os gestos de limites.

-   A seção [melhorando a experiência de panorâmica de dedo único](improving-the-single-finger-panning-experience.md) explica como personalizar a experiência de panorâmica manipulando a mensagem de [**\_ gesto do WM**](wm-gesture.md) .

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Você deseja uma interpretação de gesto refinada ou manipulação personalizada de vários pontos de toque

Se você quiser ter um controle ainda mais específico de gestos do que é oferecido pela mensagem de [**\_ gesto do WM**](wm-gesture.md) ou se desejar interpretar vários gestos em vários objetos, deverá usar o processador de manipulação. Essencialmente, o processador de manipulação é um superconjunto de gestos. Usar o processador de manipulação exige que você implemente um coletor de eventos para manipulações para as quais você alimenta dados brutos de toque.

Se você quiser uma física de objeto simples, além de interpretar os gestos, deverá usar um processador inércia em conjunto com o processador de manipulação. O processador inércia trabalha com o processador de manipulação, tomando os valores de velocidade do processador de manipulação após a conclusão da manipulação.

Se você quiser interpretar vários pontos de toque em seu aplicativo, deverá criar um manipulador de mensagens para a mensagem do [**WM \_ Touch**](wm-touchdown.md) .

-   A seção de [entrada por toque do Windows](guide-multi-touch-input.md) explica como você pode interpretar a mensagem de [**\_ toque do WM**](wm-touchdown.md) .
-   A seção [detectando e acompanhando vários pontos de toque](detecting-and-tracking-multiple-touch-points.md) demonstra como criar um aplicativo simples que interpreta várias entradas.
-   A seção [manipulações e inércia](manipulation-and-inertia.md) explica como habilitar a abordagem mais flexível para o Windows Touch.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Você deseja habilitar a entrada por toque do Windows para um aplicativo que usa o RealTimeStylus

Se você quiser habilitar a entrada para vários contatos na plataforma do Tablet PC, deverá implementar um plug-in do RealTimeStylus personalizado que interprete os dados de toque do Windows. A Microsoft introduziu as interfaces [**ITablet3**](/windows/desktop/tablet/itablet3) e [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) para habilitar a entrada de vários contatos no plug-in do RealTimeStylus. Essas interfaces simplificam a extensão de plug-ins RealTimeStylus para dar suporte a vários pontos de contato.

Para verificar se o suporte a vários contatos está habilitado, chame [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch). Para verificar o número de contatos com suporte, chame [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors). Para habilitar ou desabilitar o suporte a vários contatos, chame [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled).

> [!Note]  
> Se você não habilitar vários pontos de contato no RealTimeStylus, receberá mensagens de gesto como panorâmica e zoom.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 