---
description: 'O GDI+ dá suporte a vários tipos de curvas: reticências, arcos, Cardeal Cardinals e B&\# 233; ziers de linha.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Construindo e desenhando curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988890"
---
# <a name="constructing-and-drawing-curves"></a>Construindo e desenhando curvas

O GDI+ dá suporte a vários tipos de curvas: elipses, arcos, polilinhas cardeal e linhas de Bézier. Uma elipse é definida por seu retângulo delimitador; um arco é uma parte de uma elipse definida por um ângulo inicial e um ângulo de flecha. Um spline cardinal é definido por uma matriz de pontos e um parâmetro de tensão – a curva passa suavemente por cada ponto na matriz e o parâmetro de tensão influencia a maneira como a curva se dobra. Uma spline de Bézier é definida por dois pontos de extremidade e dois pontos de controle — a curva não passa pelos pontos de controle, mas os pontos de controle influenciam a direção e a curva à medida que ela passa de um ponto de extremidade para o outro.

Os tópicos a seguir abordam as polilinhas cardeal e as linhas de Bézier em mais detalhes:

-   [Desenhando as linhas Cardeal](-gdiplus-drawing-cardinal-splines-use.md)
-   [Desenhando splines de Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



