---
title: Acessibilidade Ativa e Windows o dimensionamento de tela Vista
description: Windows O Vista permite que os usuários alterem a configuração de pontos por polegada (DPI) para que a maioria dos elementos da interface do usuário na tela pareçam maiores.
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
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Acessibilidade Ativa e Windows o dimensionamento de tela Vista

Windows O Vista permite que os usuários alterem a configuração de pontos por polegada (DPI) para que a maioria dos elementos da interface do usuário na tela pareçam maiores. embora esse recurso tenha sido muito disponível no Microsoft Windows, nas versões anteriores, o dimensionamento precisava ser implementado por aplicativos. no Windows Vista, o Gerenciador de Janelas da Área de Trabalho executa o dimensionamento padrão para todos os aplicativos que não manipulam seu próprio dimensionamento. Os aplicativos cliente Microsoft Acessibilidade Ativa devem levar esse recurso em conta.

## <a name="scaling-in-windows-vista"></a>dimensionamento no Windows Vista

A configuração padrão de DPI é 96, o que significa que 96 pixels ocupam uma largura ou altura de uma polegada de conceito. A medida exata de uma "polegada" depende do tamanho e da resolução física do monitor. Por exemplo, em um monitor de 12 polegadas de largura, com uma resolução horizontal de 1280 pixels, uma linha horizontal de 96 pixels se estende cerca de 9/10 de uma polegada.

Alterar a configuração de DPI não é o mesmo que alterar a resolução da tela. Com o ajuste de DPI, o número de pixels físicos na tela permanece o mesmo. No entanto, o dimensionamento é aplicado ao tamanho e ao local dos elementos da interface do usuário. Esse dimensionamento pode ser executado automaticamente pelo Gerenciador de Janelas da Área de Trabalho (DWM) para a área de trabalho e para aplicativos que não pedem explicitamente que não sejam dimensionados.

Em vigor, quando o usuário define o fator de escala como 120 dpi, uma polegada vertical ou horizontal na tela se torna maior em 25%. Todas as dimensões são dimensionadas de acordo. O deslocamento de uma janela das bordas superior e esquerda da tela aumenta em 25%. O tamanho da janela aumenta na mesma proporção, juntamente com os deslocamentos e tamanhos de todos os elementos da interface do usuário que ele contém.

Por padrão, o DWM não executa o dimensionamento para aplicativos que não reconhecem dpi quando o usuário define o DPI como 120, mas o executa quando o DPI é definido como um valor personalizado de 144 ou superior. No entanto, o usuário pode substituir o comportamento padrão.

O dimensionamento de tela cria novos desafios para aplicativos que se preocupam de qualquer forma com coordenadas de tela. A tela agora contém dois sistemas de coordenadas: físico e lógico. As coordenadas físicas de um ponto são o deslocamento real em pixels da parte superior esquerda da origem. As coordenadas lógicas são os deslocamentos como seriam se os próprios pixels fossem dimensionados.

Suponha que você projete uma caixa de diálogo com um botão nas coordenadas (100, 48). Quando essa caixa de diálogo é exibida no padrão de 96 dpi, o botão está localizado em coordenadas físicas de (100, 48). Em 120 dpi, ele está localizado em coordenadas físicas de (125, 60). Mas as coordenadas lógicas são as mesmas em qualquer configuração de DPI: (100, 48).

As coordenadas lógicas são importantes, pois tornam o comportamento do sistema operacional e dos aplicativos consistentes, independentemente da configuração de DPI. Por exemplo, **System. Windows. Forms. cursor. Position** normalmente retorna as coordenadas lógicas. Se você mover o cursor sobre um elemento em uma caixa de diálogo, as mesmas coordenadas serão retornadas independentemente da configuração de DPI. Se você desenhar um controle em (100, 100), ele será desenhado para essas coordenadas lógicas e ocupará a mesma posição relativa em qualquer configuração de DPI.

## <a name="scaling-in-active-accessibility-clients"></a>Dimensionamento em clientes Acessibilidade Ativa

O Microsoft Acessibilidade Ativa não usa coordenadas lógicas. Os métodos e as funções a seguir retornam coordenadas físicas ou as levam como parâmetros.

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Por padrão, um aplicativo cliente do Microsoft Acessibilidade Ativa em execução em um ambiente diferente de 96 DPI não poderá obter os resultados corretos dessas chamadas. Por exemplo, como a posição do cursor está em coordenadas lógicas, o cliente não pode simplesmente passar essas coordenadas para [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) para obter o elemento que está sob o cursor.

Além disso, um aplicativo que cria uma janela fora de sua área de cliente, como um aplicativo de acessibilidade que realça elementos de interface do usuário focados, não criará a janela no local correto da tela, pois a janela será colocada nas coordenadas lógicas, não nas coordenadas físicas retornadas por [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

A solução está em duas partes:

-   Tornar o aplicativo cliente "com reconhecimento de dpi". Para fazer isso, chame a função [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) na inicialização. Essa função faz com que todo o processo reconheça o DPI, o que significa que todas as janelas que pertencem ao processo não são dimensionadas.
-   Use funções com reconhecimento de DPI. Por exemplo, para obter coordenadas de cursor, chame a função [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) . Não use [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); seu comportamento em aplicativos com reconhecimento de DPI é indefinido.

Se seu aplicativo executa comunicação direta entre processos com aplicativos que não reconhecem dpi, você pode ter convertido entre coordenadas lógicas e físicas usando as funções [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) e [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) .

 

 