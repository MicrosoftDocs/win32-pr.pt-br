---
description: Objetos de imagem e bitmap armazenam imagens em um formato independente de dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Usando um bitmap armazenado em cache para melhorar o desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988856"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="416fd-103">Usando um bitmap armazenado em cache para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="416fd-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="416fd-104">Objetos de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) armazenam imagens em um formato independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="416fd-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="416fd-105">Um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) armazena uma imagem no formato do dispositivo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="416fd-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="416fd-106">A renderização de uma imagem armazenada em um objeto **CachedBitmap** é rápida porque nenhum tempo de processamento é gasto convertendo a imagem para o formato exigido pelo dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="416fd-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="416fd-107">O exemplo a seguir cria um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) do arquivo Texture.jpg.</span><span class="sxs-lookup"><span data-stu-id="416fd-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="416fd-108">O **bitmap** e o **CachedBitmap** são cada um desenhado em 30.000 vezes.</span><span class="sxs-lookup"><span data-stu-id="416fd-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="416fd-109">Se você executar o código, verá que as imagens **CachedBitmap** são desenhadas significativamente mais rápido do que as imagens de **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="416fd-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> <span data-ttu-id="416fd-110">Um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) corresponde ao formato do dispositivo de exibição no momento em que o objeto **CachedBitmap** foi construído.</span><span class="sxs-lookup"><span data-stu-id="416fd-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="416fd-111">Se o usuário do seu programa alterar as configurações de exibição, seu código deverá construir um novo objeto **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="416fd-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="416fd-112">O método **DrawImage** falhará se você passar um objeto **CachedBitmap** criado antes de uma alteração no formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="416fd-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



