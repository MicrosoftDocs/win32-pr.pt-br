---
title: Noções básicas sobre problemas de dimensionamento de tela
description: Windows O Vista e versões posteriores do sistema operacional permitem que os usuários alterem a configuração de dpi (pontos por polegada) para que a maioria dos elementos da interface do usuário na tela pareça maior.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- clientes, Automação da Interface do Usuário de tela
- clientes, dimensionamento de tela
- clientes, dimensionamento
- Automação da Interface do Usuário, dimensionamento de tela
- Automação da Interface do Usuário,dimensionamento
- dimensionamento de tela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dcdc8d586b4320e4da04dfdd7e0264f36074cc59fa53f42333ec5a6c3dd135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614286"
---
# <a name="understanding-screen-scaling-issues"></a>Noções básicas sobre problemas de dimensionamento de tela

Windows O Vista e versões posteriores do sistema operacional permitem que os usuários alterem a configuração de dpi (pontos por polegada) para que a maioria dos elementos da interface do usuário na tela pareça maior. Em versões anteriores do Windows, o dimensionamento precisava ser implementado por aplicativos. No Windows Vista e posterior, o DWM (Gerenciador de Janelas da Área de Trabalho) executa o dimensionamento padrão para todos os aplicativos que não lidam com seu próprio dimensionamento. Os aplicativos Automação da Interface do Usuário cliente da Microsoft devem levar esse recurso em conta.

Este tópico contém as seguintes seções:

-   [Dimensionamento no Windows Vista e posterior](#scaling-in-windows-vista-and-later)
-   [Dimensionamento em Automação da Interface do Usuário Clientes](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Dimensionamento no Windows Vista e posterior

A configuração de dpi padrão é 96, o que significa que 96 pixels ocupam uma largura ou altura de uma polegada noções básicas. A medida exata de uma "polegada" depende do tamanho e da resolução física do monitor. Por exemplo, em um monitor de 12 polegadas de largura, em uma resolução horizontal de 1280 pixels, uma linha horizontal de 96 pixels estende cerca de 9/10 de polegada.

Alterar a configuração de dpi não é o mesmo que alterar a resolução da tela. Com o dimensionamento de dpi, o número de pixels físicos na tela permanece o mesmo. No entanto, o dimensionamento é aplicado ao tamanho e ao local dos elementos da interface do usuário. Esse dimensionamento pode ser executado automaticamente pelo DWM para a área de trabalho e para aplicativos que não solicitam explicitamente que não sejam dimensionados.

Na verdade, quando o usuário define o fator de escala como 120 dpi, uma polegada vertical ou horizontal na tela fica maior em 25%. Todas as dimensões são dimensionados de acordo. O deslocamento de uma janela de aplicativo da borda superior e esquerda da tela aumenta em 25%. Se o dimensionamento de aplicativos estiver habilitado e o aplicativo não tiver conhecimento de dpi, o tamanho da janela aumentará na mesma proporção, juntamente com os deslocamentos e tamanhos de todos os elementos de interface do usuário que ele contém.

> [!Note]  
> Por padrão, o DWM não executa o dimensionamento para aplicativos sem conhecimento de dpi quando o usuário define o dpi como 120, mas executa o dimensionamento quando o dpi é definido como um valor personalizado de 144 ou superior. No entanto, o usuário pode substituir o comportamento padrão.

 

O dimensionamento de tela cria novos desafios para aplicativos que se preocupam de qualquer forma com as coordenadas de tela. A tela agora contém dois sistemas de coordenadas: físico e lógico. As coordenadas físicas de um ponto são o deslocamento real em pixels do canto superior esquerdo do ponto de origem. As coordenadas lógicas são os deslocamentos como seriam se os próprios pixels fossem dimensionados.

Suponha que você projete uma caixa de diálogo com um botão nas coordenadas (100, 48). Quando essa caixa de diálogo é exibida no padrão de 96 dpi, o botão está localizado em coordenadas físicas de (100, 48). Em 120 dpi, ele está localizado em coordenadas físicas de (125, 60). Mas as coordenadas lógicas são as mesmas em qualquer configuração de dpi: (100, 48).

As coordenadas lógicas são importantes, pois fazem com que o comportamento do sistema operacional e dos aplicativos seja consistente, independentemente da configuração de dpi. Por exemplo, normalmente, a [**função GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) retorna as coordenadas lógicas. Se você mover o cursor sobre um elemento em uma caixa de diálogo, as mesmas coordenadas serão retornadas, independentemente da configuração de dpi. Se você desenhar um controle em (100, 100), ele será desenhado para essas coordenadas lógicas e ocupará a mesma posição relativa em qualquer configuração de dpi.

## <a name="scaling-in-ui-automation-clients"></a>Dimensionamento em Automação da Interface do Usuário clientes

A API Automação da Interface do Usuário não usa coordenadas lógicas. Os métodos e propriedades a seguir retornam coordenadas físicas ou levam coordenadas físicas como parâmetros.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Por padrão, Automação da Interface do Usuário aplicativos em execução em um ambiente que não está definido como 96 dpi não obterão os resultados corretos desses métodos e propriedades. Por exemplo, como a posição do cursor está em coordenadas lógicas, o cliente não pode passar essas coordenadas para [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) para obter o elemento que está sob o cursor. Além disso, o aplicativo não poderá colocar corretamente as janelas fora de sua área de cliente.

A solução tem duas partes.

Primeiro, faça com que o aplicativo cliente esteja ciente de dpi. Para fazer isso, chame a [**função SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) na inicialização. Essa função torna todo o processo ciente de dpi, o que significa que todas as janelas que pertencem ao processo são descalçadas.

Em segundo lugar, para obter coordenadas de cursor, chame a [**função GetPhysicalCursorPos.**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos)

 

 