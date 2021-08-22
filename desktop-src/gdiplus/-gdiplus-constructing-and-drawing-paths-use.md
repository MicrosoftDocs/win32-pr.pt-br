---
description: Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e outros) que podem ser manipulados e desenhados como uma única unidade. Um caminho pode ser dividido em figuras abertas ou fechadas. Uma figura pode conter vários primitivos.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Construindo e desenhando demarcadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83608dfacbd75bcbe916c9b5528f4bed7be4ed65713927a65f3823670c93311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612496"
---
# <a name="constructing-and-drawing-paths"></a>Construindo e desenhando demarcadores

Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e outros) que podem ser manipulados e desenhados como uma única unidade. Um caminho pode ser dividido em *figuras* abertas ou fechadas. Uma figura pode conter vários primitivos.

Você pode desenhar um caminho chamando o método [**Graphics::D rawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e preencher um caminho chamando o método [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) da classe **Graphics.**

Os tópicos a seguir abrangem caminhos mais detalhadamente:

-   [Criar figuras usando linhas, curvas e formas](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Preenchendo figuras abertas](-gdiplus-filling-open-figures-use.md)

 

 



