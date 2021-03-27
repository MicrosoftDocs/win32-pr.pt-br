---
description: A finalidade do teste de clique é determinar se o cursor está sobre um determinado objeto, como um ícone ou um botão.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Teste de clique com uma região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24913d8d890e3e1ded87eb48e2d52f1726663a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988867"
---
# <a name="hit-testing-with-a-region"></a>Teste de clique com uma região

A finalidade do teste de clique é determinar se o cursor está sobre um determinado objeto, como um ícone ou um botão. O exemplo a seguir cria uma região com formato de mais, formando a União de duas regiões retangulares. Suponha que o **ponto** da variável contenha o local do clique mais recente. O código verifica se o **ponto** está na região com formato de mais. Se o **ponto** estiver na região (um pressionamento), a região será preenchida com um pincel vermelho opaco. Caso contrário, a região será preenchida com um pincel vermelho semitransparente.


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



 

 



