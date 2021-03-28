---
description: Uma imagem em miniatura é uma versão pequena de uma imagem. Você pode criar uma imagem em miniatura chamando o método GetThumbnailImage de um objeto Image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Criando imagens em miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556938"
---
# <a name="creating-thumbnail-images"></a>Criando imagens em miniatura

Uma imagem em miniatura é uma versão pequena de uma imagem. Você pode criar uma imagem em miniatura chamando o método **GetThumbnailImage** de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .

O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Compass.bmp. A imagem original tem uma largura de 640 pixels e uma altura de 479 pixels. O código cria uma imagem em miniatura que tem uma largura de 100 pixels e uma altura de 100 pixels.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



A ilustração a seguir mostra a imagem em miniatura.

![ilustração de um gráfico pequeno mostrando uma bússola](images/thumbnail1.png)

 

 



