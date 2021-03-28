---
description: Você pode preencher uma forma fechada com uma textura usando a classe Image e a classe TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Preenchendo uma forma com uma textura de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091467"
---
# <a name="filling-a-shape-with-an-image-texture"></a>Preenchendo uma forma com uma textura de imagem

Você pode preencher uma forma fechada com uma textura usando a classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e a classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .

O exemplo a seguir preenche uma elipse com uma imagem. O código constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e, em seguida, passa o endereço desse objeto **Image** como um argumento para um construtor [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) . A terceira instrução de código dimensiona a imagem e a quarta instrução preenche a elipse com cópias repetidas da imagem dimensionada:


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



No exemplo de código anterior, o método [**TextureBrush:: SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) define a transformação que é aplicada à imagem antes de ser desenhada. Suponha que a imagem original possui uma largura de 640 pixels e uma altura de 480 pixels. A transformação reduz a imagem para 75 × 75, definindo os valores de dimensionamento horizontal e vertical.

> [!Note]  
> No exemplo anterior, o tamanho da imagem é 75 × 75 e o tamanho da elipse é 150 × 250. Como a imagem é menor do que a elipse que ela está preenchendo, a elipse é organizada lado a lado com a imagem. Lado a lado significa que a imagem é repetida horizontal e verticalmente até o limite da forma ser atingido. Para obter mais informações sobre a colocação em blocos, consulte [organizar uma forma em um formato com uma imagem](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



