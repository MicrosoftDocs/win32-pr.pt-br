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
# <a name="creating-thumbnail-images"></a><span data-ttu-id="53a9a-104">Criando imagens em miniatura</span><span class="sxs-lookup"><span data-stu-id="53a9a-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="53a9a-105">Uma imagem em miniatura é uma versão pequena de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="53a9a-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="53a9a-106">Você pode criar uma imagem em miniatura chamando o método **GetThumbnailImage** de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="53a9a-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="53a9a-107">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Compass.bmp.</span><span class="sxs-lookup"><span data-stu-id="53a9a-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="53a9a-108">A imagem original tem uma largura de 640 pixels e uma altura de 479 pixels.</span><span class="sxs-lookup"><span data-stu-id="53a9a-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="53a9a-109">O código cria uma imagem em miniatura que tem uma largura de 100 pixels e uma altura de 100 pixels.</span><span class="sxs-lookup"><span data-stu-id="53a9a-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="53a9a-110">A ilustração a seguir mostra a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="53a9a-110">The following illustration shows the thumbnail image.</span></span>

![ilustração de um gráfico pequeno mostrando uma bússola](images/thumbnail1.png)

 

 



