---
title: Acessibilidade Ativa e Windows de tela do Vista
description: Windows O Vista permite que os usuários alterem a configuração dpi (pontos por polegada) para que a maioria dos elementos da interface do usuário na tela pareça maior.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acf9c1ff6755507541c08b34e183dd751e0941fc646a1f691e4488884e572c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327056"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Acessibilidade Ativa e Windows de tela do Vista

Windows O Vista permite que os usuários alterem a configuração dpi (pontos por polegada) para que a maioria dos elementos da interface do usuário na tela pareça maior. Embora esse recurso tenha sido disponibilizado há muito tempo no Microsoft Windows, nas versões anteriores, o dimensionamento precisava ser implementado por aplicativos. No Windows Vista, o Gerenciador de Janelas da Área de Trabalho executa o dimensionamento padrão para todos os aplicativos que não lidam com seu próprio dimensionamento. Microsoft Active Accessibility aplicativos cliente devem levar esse recurso em conta.

## <a name="scaling-in-windows-vista"></a>Dimensionamento no Windows Vista

A configuração de dpi padrão é 96, o que significa que 96 pixels ocupam uma largura ou altura de uma polegada noções básicas. A medida exata de uma "polegada" depende do tamanho e da resolução física do monitor. Por exemplo, em um monitor de 12 polegadas de largura, em uma resolução horizontal de 1280 pixels, uma linha horizontal de 96 pixels estende cerca de 9/10 de polegada.

Alterar a configuração de dpi não é o mesmo que alterar a resolução da tela. Com o dimensionamento de dpi, o número de pixels físicos na tela permanece o mesmo. No entanto, o dimensionamento é aplicado ao tamanho e ao local dos elementos da interface do usuário. Esse dimensionamento pode ser executado automaticamente pelo DWM (Gerenciador de Janelas da Área de Trabalho) para a área de trabalho e para aplicativos que não solicitam explicitamente que não sejam dimensionados.

Na verdade, quando o usuário define o fator de escala como 120 dpi, uma polegada vertical ou horizontal na tela fica maior em 25%. Todas as dimensões são dimensionados de acordo. O deslocamento de uma janela das bordas superior e esquerda da tela aumenta em 25%. O tamanho da janela aumenta na mesma proporção, juntamente com os deslocamentos e tamanhos de todos os elementos de interface do usuário que ela contém.

Por padrão, o DWM não executa o dimensionamento para aplicativos sem conhecimento de dpi quando o usuário define o dpi como 120, mas o executa quando o dpi é definido como um valor personalizado de 144 ou superior. No entanto, o usuário pode substituir o comportamento padrão.

O dimensionamento de tela cria novos desafios para aplicativos que se preocupam de qualquer forma com as coordenadas de tela. A tela agora contém dois sistemas de coordenadas: físico e lógico. As coordenadas físicas de um ponto são o deslocamento real em pixels da parte superior esquerda da origem. As coordenadas lógicas são os deslocamentos como seriam se os próprios pixels fossem dimensionados.

Suponha que você projete uma caixa de diálogo com um botão nas coordenadas (100, 48). Quando essa caixa de diálogo é exibida no padrão de 96 dpi, o botão está localizado em coordenadas físicas de (100, 48). Em 120 dpi, ele está localizado em coordenadas físicas de (125, 60). Mas as coordenadas lógicas são as mesmas em qualquer configuração de dpi: (100, 48).

As coordenadas lógicas são importantes, pois elas fazem com que o comportamento do sistema operacional e dos aplicativos seja consistente, independentemente da configuração de dpi. Por exemplo, **System.Windows. Forms.Cursor.Position** normalmente retorna as coordenadas lógicas. Se você mover o cursor sobre um elemento em uma caixa de diálogo, as mesmas coordenadas serão retornadas independentemente da configuração de dpi. Se você desenhar um controle em (100, 100), ele será desenhado para essas coordenadas lógicas e ocupará a mesma posição relativa em qualquer configuração de dpi.

## <a name="scaling-in-active-accessibility-clients"></a>Dimensionamento em Acessibilidade Ativa Clientes

Microsoft Active Accessibility não usa coordenadas lógicas. Os métodos e funções a seguir retornam coordenadas físicas ou as levam como parâmetros.

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Por padrão, um Microsoft Active Accessibility aplicativo cliente em execução em um ambiente diferente de 96 dpi não poderá obter os resultados corretos dessas chamadas. Por exemplo, como a posição do cursor está em coordenadas lógicas, o cliente não pode simplesmente passar essas coordenadas para [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) para obter o elemento que está sob o cursor.

Além disso, um aplicativo que cria uma janela fora de sua área de cliente, como um aplicativo de acessibilidade que realça elementos de interface do usuário focados, não criará a janela no local correto da tela, pois a janela será colocada nas coordenadas lógicas, não nas coordenadas físicas retornadas por [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

A solução está em duas partes:

-   Tornar o aplicativo cliente "com conhecimento de dpi". Para fazer isso, chame a [**função SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) na inicialização. Essa função torna todo o processo ciente de dpi, o que significa que todas as janelas que pertencem ao processo são descalçadas.
-   Use funções com conhecimento de dpi. Por exemplo, para obter coordenadas de cursor, chame a [**função GetPhysicalCursorPos.**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) Não use [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); seu comportamento em aplicativos com conhecimento de dpi é indefinido.

Se seu aplicativo executar comunicação direta entre processos com aplicativos sem conhecimento de dpi, você poderá converter entre coordenadas lógicas e físicas usando as funções [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) e [**LogicalToPhysicalPoint.**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint)

 

 