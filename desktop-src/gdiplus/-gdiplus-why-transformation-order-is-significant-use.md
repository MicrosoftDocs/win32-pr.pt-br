---
description: Um único objeto matriz pode armazenar uma única transformação ou uma sequência de transformações.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Por que a ordem das transformações é importante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967394"
---
# <a name="why-transformation-order-is-significant"></a>Por que a ordem das transformações é importante

Um único objeto [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) pode armazenar uma única transformação ou uma sequência de transformações. O último é chamado de *transformação* composta.   A matriz de uma transformação composta é obtida multiplicando-se as matrizes das transformações individuais.

Em uma transformação composta, a ordem das transformações individuais é importante. Por exemplo, girar, ajustar a escala e mover terá um resultado diferente de mover, girar e ajustar a escala. No Windows GDI+, as transformações de composição são criadas da esquerda para a direita. Se S, R e T forem matrizes de escala, rotação e translação, respectivamente, o produto SRT (nesta ordem) será a matriz da transformação composta que primeiro ajusta a escala, em seguida girará e finalmente fará a translação. A matriz produzida pelo produto SRT será diferente da matriz produzida pelo produto TRS.

Um motivo de a ordem ser importante é que transformações, como rotação e colocação em escala, são feitas em relação a origem do sistema de coordenadas. O dimensionamento de um objeto que é centralizado na origem produz um resultado diferente do dimensionamento de um objeto que foi movido para fora da origem. Da mesma forma, girar um objeto centralizado na origem produz um resultado diferente de girar um objeto movido para fora da origem.

O exemplo a seguir combina colocação em escala, rotação e translação (nessa ordem) para formar uma transformação composta. O argumento [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * passado para o método [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) especifica que a rotação seguirá o dimensionamento. Da mesma forma, o argumento [* * * * MatrixOrderAppend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passado para o método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) especifica que a conversão irá seguir a rotação.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



O exemplo a seguir faz as mesmas chamadas de método que o exemplo anterior, mas a ordem das chamadas é revertida. A ordem resultante das operações é primeiro traduzir, depois girar e dimensionar, o que produz um resultado muito diferente do que a primeira escala, em seguida, girar e depois converter:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Uma maneira de inverter a ordem das transformações individuais em uma transformação composta é inverter a ordem de uma sequência de chamadas de método. Outra maneira de controlar a ordem das operações é alterar o argumento de ordem de matriz. O exemplo a seguir é o mesmo que o exemplo anterior, exceto que [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * foi alterado para [* * * * MatrixOrderPrepend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* *. A multiplicação de matriz é feita na ordem SRT, em que S, R e T são matrizes para ajustar escala, girar e mover, respectivamente. A ordem da transformação composta é ajustar escala, girar e mover.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



O resultado do exemplo anterior é o mesmo resultado que obtivemos no primeiro exemplo desta seção. Isso ocorre porque invertemos a ordem das chamadas de método e a ordem de multiplicação da matriz.

 

 



