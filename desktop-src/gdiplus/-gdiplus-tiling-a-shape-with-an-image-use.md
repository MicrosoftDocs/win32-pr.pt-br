---
description: Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Lado a lado de uma forma com uma imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fc04439db21191ddc110859ae628e975d50bf617db3da63189859070766b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943766"
---
# <a name="tiling-a-shape-with-an-image"></a>Lado a lado de uma forma com uma imagem

Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma. Para organizar o interior de uma forma lado a lado, use um pincel de textura. Quando você constrói [**um objeto TextureBrush,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) um dos argumentos que você passa para o construtor é o endereço de um [**objeto Image.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Quando você usa o pincel de textura para pintar o interior de uma forma, ela será preenchida com repetidas cópias dessa imagem.

A propriedade de modo de wrap do [**objeto TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina como a imagem é orientada à medida que ela é repetida em uma grade retangular. Você pode fazer todos os blocos na grade terem a mesma orientação ou fazer com que a imagem fique invertida de uma posição de grade para a próxima. A inversão pode ser horizontal, vertical ou ambas. Os exemplos a seguir demonstram organização lado a lado com tipos diferentes de inversão.

## <a name="tiling-an-image"></a>Lado a lado de uma imagem

Este exemplo usa a seguinte imagem de 75 ×75 para lado um retângulo de 200 ×200:

![ilustração usada como base de outras ilustrações neste tópico: uma casa e uma árvore em segundo plano e centralizadas em um retângulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que todos os blocos têm a mesma orientação; não há nenhum inversão.

![ilustração mostrando a imagem base repetida horizontal e verticalmente em um retângulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling&quot;></a>Invertendo uma imagem horizontalmente ao lado do lado

Este exemplo usa uma imagem de 75 ×75 para preencher um retângulo de 200 ×200. O modo de encapsulamento é definido para inverter a imagem horizontalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente.

![ilustração mostrando a imagem base repetida horizontalmente, mas instâncias numeradas até mesmo são revertidas horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling&quot;></a>Invertendo uma imagem verticalmente ao lado do lado

Este exemplo usa uma imagem de 75 ×75 para preencher um retângulo de 200 ×200. O modo de encapsulamento é definido para inverter a imagem verticalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem. Observe que, conforme você move de um lado para o próximo em uma determinada coluna, a imagem é invertida verticalmente.

![ilustração mostrando a imagem base repetida horizontal e verticalmente, mas linhas numeradas até mesmo são revertidas verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling&quot;></a>Invertendo uma imagem horizontal e verticalmente enquanto lado a lado

Este exemplo usa uma imagem de 75 ×75 para lado um retângulo de 200 ×200. O modo de encapsulamento é definido para inverter a imagem tanto horizontalmente quanto verticalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



A ilustração a seguir mostra como o retângulo é organizado lado a lado pela imagem. Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente e, ao mudar de um bloco para o próximo em uma determinada coluna, a imagem é invertida verticalmente.

![ilustração que mostra instâncias alternadas da imagem base em cada linha são invertida horizontalmente e as linhas alternadas são invertida verticalmente](images/tile5.png)

 

 



