---
description: 'Você pode preencher um caminho passando o endereço de um objeto GraphicsPath para o método Graphics:: FillPath.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Preenchendo figuras abertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198a1a9e3a3cffa6aa5c0f3627c1415a54c8842c9f90a2ebdd6ebc2a9e0f3fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977536"
---
# <a name="filling-open-figures"></a>Preenchendo figuras abertas

Você pode preencher um caminho passando o endereço de um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) para o método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) . O método **Graphics:: FillPath** preenche o caminho de acordo com o modo de preenchimento (alternativo ou de vento) definido atualmente para o caminho. Se o caminho tiver figuras abertas, ele será preenchido como se essas figuras que foram fechadas. GDI+ fecha uma figura desenhando uma linha reta de seu ponto final para o ponto de partida.

O exemplo a seguir cria um caminho que tem uma figura aberta (um arco) e uma figura fechada (uma elipse). O método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) preenche o caminho de acordo com o modo de preenchimento padrão, que é FillModeAlternate.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



A ilustração a seguir mostra a saída do código anterior. Observe que o caminho é preenchido (de acordo com FillModeAlternate) como se a figura aberta fosse fechada por uma linha reta de seu ponto final até seu ponto de partida.

![ilustração mostrando uma elipse alta que sobrepõe a metade inferior de uma elipse larga; a União está preenchida, mas a interseção está vazia](images/fillopenpath.png)

 

 



