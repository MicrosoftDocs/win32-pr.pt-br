---
description: A finalidade do teste de clique é determinar se o cursor está sobre um determinado objeto, como um ícone ou um botão.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Teste de acerto com uma região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0673466bc368c9288765b1c7e6f460716d8d40674802a0977690a7ef79b58b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885394"
---
# <a name="hit-testing-with-a-region"></a>Teste de acerto com uma região

A finalidade do teste de clique é determinar se o cursor está sobre um determinado objeto, como um ícone ou um botão. O exemplo a seguir cria uma região em forma de a mais, formando a união de duas regiões retangulares. Suponha que o ponto **de variável** contém o local do clique mais recente. O código verifica se o **ponto está** na região em forma de a mais. Se **o** ponto estiver na região (um acerto), a região será preenchida com um pincel vermelho opaco. Caso contrário, a região será preenchida com um pincel vermelho semitransparente.


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



