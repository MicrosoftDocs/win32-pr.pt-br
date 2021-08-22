---
title: Por que usar DirectComposition
description: Este tópico descreve os recursos e os benefícios do Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Por que usar DirectComposition
- motivos para usar o DirectComposition
- Recursos e benefícios do DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9b67b17869c53b393d8a1f1ecb6230a69322d898f691c21370a5b24befda21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562086"
---
# <a name="why-use-directcomposition"></a>Por que usar o DirectComposition?

> [!NOTE]
> para aplicativos no Windows 10, é recomendável usar as APIs Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve os recursos e os benefícios do Microsoft DirectComposition. Ele contém as seções a seguir:

-   [Criar uma interface do usuário visualmente atraente](#create-a-visually-engaging-user-interface)
-   [Habilite animações avançadas e suaves para seu aplicativo](#enable-rich-smooth-animations-for-your-application)
-   [Combinar bitmaps de uma variedade de fontes](#combine-bitmaps-from-a-variety-of-sources)
-   [Economia de memória por meio da integração com o DWM](#memory-savings-though-integration-with-dwm)
-   [Mantenha o que você já tem](#keep-what-you-already-have)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Criar uma interface do usuário visualmente atraente

o DirectComposition permite combinar e animar [*visuais*](directcomposition-glossary.md) para criar uma interface do usuário visualmente envolvente para seus aplicativos baseados em Windows. Ele pode ajudar a dar uma aparência única ao seu aplicativo, estabelecendo uma identidade que o define de forma separada de outros aplicativos.

O DirectComposition também pode ajudar a facilitar o uso de seus aplicativos. Por exemplo, você pode usar isso para criar indicações visuais e transições de tela animadas que mostram as relações entre os itens na tela.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Habilite animações avançadas e suaves para seu aplicativo

DirectComposition é um mecanismo de composição de bitmap de alto desempenho que usa gráficos acelerados por hardware para atingir altas taxas de quadros, resultando em visão panorâmica, rolagem e animações de conteúdo complexo. Como ele opera em um thread dedicado que é separado do thread usado para renderizar a interface do usuário do aplicativo, o DirectComposition nunca pode "privar" o thread da interface do usuário ou interferir na capacidade do aplicativo de desenhar seus elementos da interface do usuário.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinar bitmaps de uma variedade de fontes

muitos aplicativos baseados em Windows têm uma interface do usuário que consiste em elementos criados por uma variedade de estruturas gráficas diferentes. por exemplo, um aplicativo pode usar Windows Forms para criar uma barra de status, Windows Graphics Device Interface (GDI) para criar o conteúdo da janela principal, o Microsoft DirectX para conteúdo de gráficos e assim por diante. O DirectComposition permite combinar o conteúdo de uma variedade de estruturas gráficas e fazer com que ela seja processada para a mesma janela de nível superior ou filho sem a necessidade de se preocupar com o que acontece se o conteúdo de diferentes estruturas se sobrepuser.

## <a name="memory-savings-though-integration-with-dwm"></a>Economia de memória por meio da integração com o DWM

composições e animações criadas por DirectComposition são passadas para um componente interno do Windows chamado [Gerenciador de Janelas da Área de Trabalho (DWM)](/windows/desktop/dwm/dwm-overview) para renderização na tela. Portanto, nenhum componente de renderização especial ou estruturas de interface do usuário são necessários no computador.

## <a name="keep-what-you-already-have"></a>Mantenha o que você já tem

o código da interface do usuário em um aplicativo existente baseado em Windows representa um investimento significativo. Para a maior parte, o DirectComposition permite compor e animar o conteúdo da interface do usuário existente. Isso significa que você pode usar o DirectComposition para fazer atualizações e aprimoramentos significativos na interface do usuário do aplicativo sem a necessidade de fazer alterações extensivas na base de código da interface do usuário existente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 