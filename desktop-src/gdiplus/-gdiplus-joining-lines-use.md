---
description: Uma junção de linha é a área comum que é formada por duas linhas cujas extremidades se encontram ou se sobrepõem.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unindo linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066970"
---
# <a name="joining-lines"></a>Unindo linhas

Uma junção de linha é a área comum que é formada por duas linhas cujas extremidades se encontram ou se sobrepõem. Windows GDI+ fornece quatro estilos de junção de linha: miter, bevel, round e miter recortado. O estilo de junção de linha é uma propriedade da [**classe Caneta.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Quando você especifica um estilo de junção de linha para uma caneta e, em seguida, usa essa caneta para desenhar um caminho, o estilo de junção especificado é aplicado a todas as linhas conectadas no caminho.

Você pode especificar o estilo de junção de linha usando o [**método Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) da [**classe Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) O exemplo a seguir demonstra uma junção de linha em bevel entre uma linha horizontal e uma linha vertical:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



A ilustração a seguir mostra a junção de linha em beveled resultante.

![ilustração que mostra duas linhas se encontrando em um ângulo direito, com uma junção em bevelled](images/pens5.png)

No exemplo anterior, o valor (**LineJoinBevel**) passado para o método [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) é um elemento da [**enumeração LineJoin.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)

 

 



