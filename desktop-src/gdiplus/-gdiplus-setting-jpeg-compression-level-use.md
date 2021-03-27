---
description: Para especificar o nível de compactação ao salvar uma imagem JPEG, inicialize um objeto EncoderParameters e passe o endereço desse objeto para o método Save da classe Image.
ms.assetid: b8365c00-2223-4aff-9fb2-422976af4c31
title: Definindo o nível de compactação JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d2e82dfb21e121609d5e09e5c31e2242ec652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647101"
---
# <a name="setting-jpeg-compression-level"></a>Definindo o nível de compactação JPEG

Para especificar o nível de compactação ao salvar uma imagem JPEG, inicialize um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) e passe o endereço desse objeto para o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Inicialize o objeto **EncoderParameters** para que ele tenha uma matriz que consista em um objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Inicialize esse objeto **EncoderParameter** para que seu membro de **valor** aponte para um valor **ULONG** de 0 a 100. Defina o membro **GUID** do objeto **EncoderParameter** como EncoderQuality.

O aplicativo de console a seguir salva três imagens JPEG, cada uma com um nível de qualidade diferente. Um nível de qualidade de 0 corresponde a uma compactação maior e um nível de qualidade de 100 corresponde a uma compactação menor.

A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md):


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

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             quality;
   Status            stat;

   // Get an image from the disk.
   Image* image = new Image(L"Shapes.bmp");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will let this value vary from 0 to 100.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderQuality;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Save the image as a JPEG with quality level 0.
   quality = 0;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes001.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes001.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes001.jpg");

   // Save the image as a JPEG with quality level 50.
   quality = 50;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes050.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes050.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes050.jpg");

      // Save the image as a JPEG with quality level 100.
   quality = 100;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes100.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes100.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes100.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
