---
title: Noções básicas sobre problemas de dimensionamento de tela
description: O Windows Vista e versões posteriores do sistema operacional permitem que os usuários alterem a configuração de pontos por polegada (DPI) para que a maioria dos elementos da interface do usuário na tela pareçam maiores.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- clientes, dimensionamento de tela de automação da interface do usuário
- clientes, dimensionamento de tela
- clientes, dimensionando
- Automação da interface do usuário, dimensionamento de tela
- Automação da interface do usuário, dimensionamento
- dimensionamento de tela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366522"
---
# <a name="understanding-screen-scaling-issues"></a>Noções básicas sobre problemas de dimensionamento de tela

O Windows Vista e versões posteriores do sistema operacional permitem que os usuários alterem a configuração de pontos por polegada (DPI) para que a maioria dos elementos da interface do usuário na tela pareçam maiores. Em versões anteriores do Windows, o dimensionamento precisava ser implementado por aplicativos. No Windows Vista e posterior, o Gerenciador de Janelas da Área de Trabalho (DWM) executa o dimensionamento padrão para todos os aplicativos que não manipulam seu próprio dimensionamento. Os aplicativos cliente de automação da interface do usuário da Microsoft devem levar esse recurso em conta.

Este tópico contém as seguintes seções:

-   [Dimensionamento no Windows Vista e posterior](#scaling-in-windows-vista-and-later)
-   [Dimensionamento em clientes de automação da interface do usuário](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Dimensionamento no Windows Vista e posterior

A configuração padrão de DPI é 96, o que significa que 96 pixels ocupam uma largura ou altura de uma polegada de conceito. A medida exata de uma "polegada" depende do tamanho e da resolução física do monitor. Por exemplo, em um monitor de 12 polegadas de largura, com uma resolução horizontal de 1280 pixels, uma linha horizontal de 96 pixels se estende cerca de 9/10 de uma polegada.

Alterar a configuração de DPI não é o mesmo que alterar a resolução da tela. Com o ajuste de DPI, o número de pixels físicos na tela permanece o mesmo. No entanto, o dimensionamento é aplicado ao tamanho e ao local dos elementos da interface do usuário. Esse dimensionamento pode ser executado automaticamente pelo DWM para a área de trabalho e para aplicativos que não pedem explicitamente que não sejam dimensionados.

Em vigor, quando o usuário define o fator de escala como 120 dpi, uma polegada vertical ou horizontal na tela se torna maior em 25%. Todas as dimensões são dimensionadas de acordo. O deslocamento de uma janela de aplicativo da borda superior e da borda esquerda da tela aumenta em 25%. Se o dimensionamento de aplicativos estiver habilitado e o aplicativo não reconhecer dpi, o tamanho da janela aumentará na mesma proporção, juntamente com os deslocamentos e tamanhos de todos os elementos da interface do usuário que ele contém.

> [!Note]  
> Por padrão, o DWM não executa o dimensionamento para aplicativos que não reconhecem dpi quando o usuário define o DPI como 120, mas realiza o dimensionamento quando o DPI é definido como um valor personalizado de 144 ou superior. No entanto, o usuário pode substituir o comportamento padrão.

 

O dimensionamento de tela cria novos desafios para aplicativos que se preocupam de qualquer forma com coordenadas de tela. A tela agora contém dois sistemas de coordenadas: físico e lógico. As coordenadas físicas de um ponto são o deslocamento real em pixels do canto superior esquerdo do ponto de origem. As coordenadas lógicas são os deslocamentos como seriam se os próprios pixels fossem dimensionados.

Suponha que você projete uma caixa de diálogo com um botão nas coordenadas (100, 48). Quando essa caixa de diálogo é exibida no padrão de 96 dpi, o botão está localizado em coordenadas físicas de (100, 48). Em 120 dpi, ele está localizado em coordenadas físicas de (125, 60). Mas as coordenadas lógicas são as mesmas em qualquer configuração de DPI: (100, 48).

As coordenadas lógicas são importantes, pois tornam o comportamento do sistema operacional e dos aplicativos consistentes, independentemente da configuração de DPI. Por exemplo, normalmente, a função [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) retorna as coordenadas lógicas. Se você mover o cursor sobre um elemento em uma caixa de diálogo, as mesmas coordenadas serão retornadas, independentemente da configuração de DPI. Se você desenhar um controle em (100, 100), ele será desenhado para essas coordenadas lógicas e ocupará a mesma posição relativa em qualquer configuração de DPI.

## <a name="scaling-in-ui-automation-clients"></a>Dimensionamento em clientes de automação da interface do usuário

A API de automação da interface do usuário não usa coordenadas lógicas. Os métodos e as propriedades a seguir retornam coordenadas físicas ou tomam coordenadas físicas como parâmetros.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Por padrão, os aplicativos de automação da interface do usuário que estão sendo executados em um ambiente que não está definido como 96 DPI não obterão os resultados corretos desses métodos e propriedades. Por exemplo, como a posição do cursor está em coordenadas lógicas, o cliente não pode passar essas coordenadas para [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) para obter o elemento que está sob o cursor. Além disso, o aplicativo não será capaz de posicionar corretamente o Windows fora de sua área de cliente.

A solução tem duas partes.

Primeiro, torne o reconhecimento de DPI do aplicativo cliente. Para fazer isso, chame a função [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) na inicialização. Essa função faz com que todo o processo reconheça o DPI, o que significa que todas as janelas que pertencem ao processo não são dimensionadas.

Em segundo lugar, para obter as coordenadas do cursor, chame a função [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) .

 

 