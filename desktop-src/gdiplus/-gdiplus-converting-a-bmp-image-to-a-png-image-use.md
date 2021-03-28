---
description: Para salvar uma imagem em um arquivo de disco, chame o método Save da classe Image.
ms.assetid: a95fa3ea-2013-45d5-bdec-61eddcefc2fa
title: Convertendo uma imagem BMP em uma imagem PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d165809bb4cfa7f37685b8b130e2b895b35c0ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988886"
---
# <a name="converting-a-bmp-image-to-a-png-image"></a>Convertendo uma imagem BMP em uma imagem PNG

Para salvar uma imagem em um arquivo de disco, chame o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . O aplicativo de console a seguir carrega uma imagem BMP de um arquivo de disco, converte a imagem no formato PNG e salva a imagem convertida em um novo arquivo de disco. A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID   encoderClsid;
   Status  stat;
   Image*   image = new Image(L"Bird.bmp");

   // Get the CLSID of the PNG encoder.
   GetEncoderClsid(L"image/png", &encoderClsid);

   stat = image->Save(L"Bird.png", &encoderClsid, NULL);

   if(stat == Ok)
      printf("Bird.png was saved successfully\n");
   else
      printf("Failure: stat = %d\n", stat); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 



