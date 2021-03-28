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
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Usando um bitmap armazenado em cache para melhorar o desempenho

Objetos de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) armazenam imagens em um formato independente de dispositivo. Um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) armazena uma imagem no formato do dispositivo de vídeo atual. A renderização de uma imagem armazenada em um objeto **CachedBitmap** é rápida porque nenhum tempo de processamento é gasto convertendo a imagem para o formato exigido pelo dispositivo de vídeo.

O exemplo a seguir cria um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) do arquivo Texture.jpg. O **bitmap** e o **CachedBitmap** são cada um desenhado em 30.000 vezes. Se você executar o código, verá que as imagens **CachedBitmap** são desenhadas significativamente mais rápido do que as imagens de **bitmap** .


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
> Um objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) corresponde ao formato do dispositivo de exibição no momento em que o objeto **CachedBitmap** foi construído. Se o usuário do seu programa alterar as configurações de exibição, seu código deverá construir um novo objeto **CachedBitmap** . O método **DrawImage** falhará se você passar um objeto **CachedBitmap** criado antes de uma alteração no formato de exibição.

 

 

 



