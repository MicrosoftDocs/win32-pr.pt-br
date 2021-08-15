---
description: 'Ao criar um objeto de caneta, você pode fornecer a largura da caneta como um dos argumentos para o construtor. Você também pode alterar a largura da caneta usando o método Pen:: SetWidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Definindo a largura e o alinhamento da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2a6bd5be00fde0f27657cef558365d857775a5b55f9f108074884906916b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885007"
---
# <a name="setting-pen-width-and-alignment"></a>Definindo a largura e o alinhamento da caneta

Ao criar um objeto de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , você pode fornecer a largura da caneta como um dos argumentos para o construtor. Você também pode alterar a largura da caneta usando o método [**Pen:: SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .

Uma linha teórica tem uma largura de zero. Quando você desenha uma linha, os pixels são centralizados na linha teórica. O exemplo a seguir desenha uma linha especificada duas vezes: uma vez com uma caneta preta de largura 1 e uma vez com uma caneta verde de largura 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



A ilustração a seguir mostra a saída do código anterior. Os pixels verdes e os pixels pretos são centralizados na linha teórica.

![ilustração mostrando uma linha fina, diagonal e preta cercada por uma linha verde ](images/pens1a.png)

O exemplo a seguir desenha um retângulo especificado duas vezes: uma vez com uma caneta preta de largura 1 e uma vez com uma caneta verde de largura 10. O código passa o valor **PenAlignmentCenter** (um elemento da enumeração [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) para o método [**Pen:: setAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) para especificar que os pixels desenhados com a caneta verde estejam centralizados no limite do retângulo.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



A ilustração a seguir mostra a saída do código anterior. Os pixels verdes são centralizados no retângulo teórico, que é representado pelos pixels pretos.

![ilustração mostrando uma linha preta fina na forma de um retângulo, cercada por uma linha verde mais larga](images/pens2.png)

Você pode alterar o alinhamento da caneta verde modificando a terceira instrução no exemplo anterior, da seguinte maneira:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Agora os pixels na linha verde larga aparecem no interior do retângulo conforme mostrado na ilustração a seguir.

![ilustração mostrando uma linha preta fina na forma de um retângulo, colocando uma linha verde larga da mesma forma](images/pens3.png)

 

 



