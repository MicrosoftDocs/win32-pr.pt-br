---
description: Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e assim por diante) que podem ser manipulados e desenhados como uma única unidade. Um caminho pode ser dividido em figuras que são abertas ou fechadas. Uma figura pode conter vários primitivos.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Construindo e desenhando demarcadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988889"
---
# <a name="constructing-and-drawing-paths"></a>Construindo e desenhando demarcadores

Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e assim por diante) que podem ser manipulados e desenhados como uma única unidade. Um caminho pode ser dividido em *figuras* que são abertas ou fechadas. Uma figura pode conter vários primitivos.

Você pode desenhar um caminho chamando o método [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e pode preencher um caminho chamando o método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) da classe **Graphics** .

Os tópicos a seguir abrangem caminhos com mais detalhes:

-   [Criar figuras usando linhas, curvas e formas](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Preenchendo figuras abertas](-gdiplus-filling-open-figures-use.md)

 

 



