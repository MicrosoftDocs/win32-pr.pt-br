---
description: Para criar um caminho e selecioná-lo em um controlador de domínio, primeiro é necessário definir os pontos que o descrevem.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Criação de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165061"
---
# <a name="path-creation"></a>Criação de caminho

Para criar um caminho e selecioná-lo em um controlador de domínio, primeiro é necessário definir os pontos que o descrevem. Isso é feito chamando a função [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , especificando as funções de desenho apropriadas e, em seguida, chamando a função [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Essa combinação de funções (**BeginPath**, funções de desenho e **EndPath**) constitui um *colchete de caminho*. A seguir está a lista de funções de desenho que podem ser usadas.

-   [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Pizza**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**PolyBezierSegment**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**Polibézierto**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Metaempate**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Múltipla**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**Polilineto**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**Polipolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Nele**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**Texto**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quando um aplicativo chama [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), o sistema seleciona o caminho associado no controlador de domínio especificado. (Se outro caminho tiver sido selecionado anteriormente no controlador de domínio, o sistema excluirá esse caminho sem salvá-lo.) Depois que o sistema seleciona o caminho no controlador de domínio, um aplicativo pode operar no caminho de uma das seguintes maneiras:

-   Desenhe o contorno do caminho (usando a caneta atual).
-   Pinte o interior do caminho (usando o pincel atual).
-   Desenhe a estrutura de tópicos e preencha o interior do caminho.
-   Modifique o caminho (convertendo curvas em segmentos de linha).
-   Converta o caminho em um caminho de clipe.
-   Converta o caminho em uma região.
-   Nivelar o caminho convertendo cada curva no caminho em uma série de segmentos de linha.
-   Recupere as coordenadas das linhas e das curvas que compõem um caminho.

 

 



