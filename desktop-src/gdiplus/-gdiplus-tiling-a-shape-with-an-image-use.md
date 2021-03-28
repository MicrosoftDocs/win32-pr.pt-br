---
description: Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Colocação em um formato de forma lado a imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090327"
---
# <a name="tiling-a-shape-with-an-image"></a>Colocação em um formato de forma lado a imagem

Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma. Para organizar o interior de uma forma lado a lado, use um pincel de textura. Quando você constrói um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , um dos argumentos que você passa para o construtor é o endereço de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) . Quando você usa o pincel de textura para pintar o interior de uma forma, ela será preenchida com repetidas cópias dessa imagem.

A propriedade Wrap Mode do objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina como a imagem é orientada à medida que é repetida em uma grade retangular. Você pode fazer todos os blocos na grade terem a mesma orientação ou fazer com que a imagem fique invertida de uma posição de grade para a próxima. A inversão pode ser horizontal, vertical ou ambas. Os exemplos a seguir demonstram organização lado a lado com tipos diferentes de inversão.

## <a name="tiling-an-image"></a>Divisão de uma imagem

Este exemplo usa a seguinte imagem 75 × 75 para dividir um retângulo 200 × 200:

![ilustração usada como a base de outras ilustrações neste tópico: uma casa e uma árvore em segundo plano e centralizadas em um retângulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que todos os blocos têm a mesma orientação; não há nenhum inversão.

![ilustração mostrando a imagem base repetida horizontal e verticalmente em um retângulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>Invertendo uma imagem horizontalmente durante a colocação em blocos

Este exemplo usa uma imagem 75 × 75 para preencher um retângulo 200 × 200. O modo de encapsulamento é definido para inverter a imagem horizontalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente.

![ilustração mostrando a imagem base repetida horizontalmente, mas as instâncias com números iguais são revertidas horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>Invertendo uma imagem verticalmente durante a colocação em blocos

Este exemplo usa uma imagem 75 × 75 para preencher um retângulo 200 × 200. O modo de encapsulamento é definido para inverter a imagem verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que, à medida que você passa de um bloco para o próximo em uma determinada coluna, a imagem é invertida verticalmente.

![ilustração mostrando a imagem base repetida horizontal e verticalmente, mas linhas de números iguais são revertidas verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>Invertendo uma imagem horizontal e verticalmente durante a colocação em divisão

Este exemplo usa uma imagem 75 × 75 para dividir um retângulo 200 × 200. O modo de encapsulamento é definido para inverter a imagem tanto horizontalmente quanto verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado pela imagem. Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente e, ao mudar de um bloco para o próximo em uma determinada coluna, a imagem é invertida verticalmente.

![a ilustração que mostra as instâncias alternadas da imagem base em cada linha é invertida horizontalmente e as linhas alternadas são invertidas verticalmente](images/tile5.png)

 

 



