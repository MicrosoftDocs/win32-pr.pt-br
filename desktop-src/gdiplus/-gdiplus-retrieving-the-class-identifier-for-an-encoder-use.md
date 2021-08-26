---
description: A função GetEncoderClsid no exemplo a seguir recebe o tipo MIME de um codificador e retorna o CLSID (identificador de classe) desse codificador.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Recuperando o identificador de classe para um codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a40c31c7ad997ed3e7525ff247019f6a41c681b9523dc523105bd5ba6c7ca6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014706"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Recuperando o identificador de classe para um codificador

A função GetEncoderClsid no exemplo a seguir recebe o tipo MIME de um codificador e retorna o **CLSID**(identificador de classe) desse codificador. Os tipos MIME dos codificadores integrados Windows GDI+ são os seguinte:

-   image/bmp
-   image/jpeg
-   image/gif
-   imagem/tiff
-   image/png

A função chama [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) para obter uma matriz de [**objetos ImageCodecInfo.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) Se um dos objetos **ImageCodecInfo** nessa matriz representar o codificador solicitado, a função retornará o índice do objeto **ImageCodecInfo** e copia o **CLSID** para a variável apontada por **pClsid**. Se a função falhar, ela retornará -1.


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



O aplicativo de console a seguir chama a função GetEncoderClsid para determinar a **CLSID** do codificador PNG:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Ao executar o aplicativo de console anterior, você obterá uma saída semelhante à seguinte:


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
