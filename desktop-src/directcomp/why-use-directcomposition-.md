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
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810620"
---
# <a name="why-use-directcomposition"></a>Por que usar o DirectComposition?

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve os recursos e os benefícios do Microsoft DirectComposition. Ele contém as seções a seguir:

-   [Criar uma interface do usuário visualmente atraente](#create-a-visually-engaging-user-interface)
-   [Habilite animações avançadas e suaves para seu aplicativo](#enable-rich-smooth-animations-for-your-application)
-   [Combinar bitmaps de uma variedade de fontes](#combine-bitmaps-from-a-variety-of-sources)
-   [Economia de memória por meio da integração com o DWM](#memory-savings-though-integration-with-dwm)
-   [Mantenha o que você já tem](#keep-what-you-already-have)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Criar uma interface do usuário visualmente atraente

O DirectComposition permite combinar e animar [*visuais*](directcomposition-glossary.md) para criar uma interface do usuário visualmente envolvente para seus aplicativos baseados no Windows. Ele pode ajudar a dar uma aparência única ao seu aplicativo, estabelecendo uma identidade que o define de forma separada de outros aplicativos.

O DirectComposition também pode ajudar a facilitar o uso de seus aplicativos. Por exemplo, você pode usar isso para criar indicações visuais e transições de tela animadas que mostram as relações entre os itens na tela.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Habilite animações avançadas e suaves para seu aplicativo

DirectComposition é um mecanismo de composição de bitmap de alto desempenho que usa gráficos acelerados por hardware para atingir altas taxas de quadros, resultando em visão panorâmica, rolagem e animações de conteúdo complexo. Como ele opera em um thread dedicado que é separado do thread usado para renderizar a interface do usuário do aplicativo, o DirectComposition nunca pode "privar" o thread da interface do usuário ou interferir na capacidade do aplicativo de desenhar seus elementos da interface do usuário.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinar bitmaps de uma variedade de fontes

Muitos aplicativos baseados no Windows têm uma interface do usuário que consiste em elementos criados por uma variedade de estruturas gráficas diferentes. Por exemplo, um aplicativo pode usar Windows Forms para criar uma barra de status, o Windows Graphics Device Interface (GDI) para criar o conteúdo da janela principal, o Microsoft DirectX para conteúdo de gráficos e assim por diante. O DirectComposition permite combinar o conteúdo de uma variedade de estruturas gráficas e fazer com que ela seja processada para a mesma janela de nível superior ou filho sem a necessidade de se preocupar com o que acontece se o conteúdo de diferentes estruturas se sobrepuser.

## <a name="memory-savings-though-integration-with-dwm"></a>Economia de memória por meio da integração com o DWM

Composições e animações criadas por DirectComposition são passadas para um componente interno do Windows chamado [Gerenciador de janelas da área de trabalho (DWM)](/windows/desktop/dwm/dwm-overview) para renderização na tela. Portanto, nenhum componente de renderização especial ou estruturas de interface do usuário são necessários no computador.

## <a name="keep-what-you-already-have"></a>Mantenha o que você já tem

O código da interface do usuário em um aplicativo existente baseado no Windows representa um investimento significativo. Para a maior parte, o DirectComposition permite compor e animar o conteúdo da interface do usuário existente. Isso significa que você pode usar o DirectComposition para fazer atualizações e aprimoramentos significativos na interface do usuário do aplicativo sem a necessidade de fazer alterações extensivas na base de código da interface do usuário existente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 