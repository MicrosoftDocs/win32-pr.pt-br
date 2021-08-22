---
description: A transformação do mundo é uma propriedade da classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Usando a transformação global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6288b5640e330a827e96b632541dac44e9463b87c566c16a94797810c4c92c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977236"
---
# <a name="using-the-world-transformation"></a>Usando a transformação global

A transformação do mundo é uma propriedade da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Os números que especificam a transformação do mundo são armazenados em um objeto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , que representa uma matriz 3 × 3. As classes **Matrix** e **Graphics** têm vários métodos para definir os números na matriz de transformação mundial. Os exemplos nesta seção manipulam retângulos porque os retângulos são fáceis de desenhar e é fácil ver os efeitos das transformações em retângulos.

Começamos criando um retângulo de 50 por 50 e localizando-o na origem (0, 0). A origem está localizada no canto superior esquerdo da área de cliente.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



O código a seguir aplica uma transformação de escala que expande o retângulo por um fator de 1,75 na direção x e encolhe o retângulo por um fator de 0,5 na direção y:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



O resultado é um retângulo que é maior na direção x e menor na direção y que o original.

Para girar o retângulo em vez de dimensioná-lo, use o código a seguir em vez do código anterior:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Para converter o retângulo, use o seguinte código:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



