---
description: Windows GDI+ fornece vários estilos de traço listados na enumeração DashStyle. Se esses estilos de traço padrão não atenderem às suas necessidades, você poderá criar um padrão de traço personalizado.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Desenhando uma linha tracejada personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad7bb415ff4f7b1cbde4637ab184c9ab05e4a707e0bce8328500d39ee2b840d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115074"
---
# <a name="drawing-a-custom-dashed-line"></a>Desenhando uma linha tracejada personalizada

Windows GDI+ fornece vários estilos de traço listados na [**enumeração DashStyle.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) Se esses estilos de traço padrão não atenderem às suas necessidades, você poderá criar um padrão de traço personalizado.

Para desenhar uma linha tracejada personalizada, coloque os comprimentos dos traços e espaços em uma matriz e passe o endereço da matriz como um argumento para o método [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) de um objeto [**Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) O exemplo a seguir desenha uma linha tracejada personalizada com base na matriz {5, 2, 15, 4}. Se você multiplicar os elementos da matriz pela largura da caneta de 5, obterá {25, 10, 75, 20}. Os traços exibidos alternam de comprimento entre 25 e 75 e os espaços alternam de comprimento entre 10 e 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



A ilustração a seguir mostra a linha tracejada resultante. Observe que o traço final deve ser menor do que 25 unidades para que a linha possa terminar em (405, 5).

![ilustração mostrando uma linha tracejada; cada segmento é uma linha curta seguida por uma longa](images/pens6.png)

 

 



