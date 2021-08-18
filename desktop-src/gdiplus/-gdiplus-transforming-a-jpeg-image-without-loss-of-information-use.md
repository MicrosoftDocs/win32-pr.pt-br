---
title: Transformação sem perdas de uma imagem JPEG
description: Quando você compacta uma imagem JPEG, algumas das informações na imagem são perdidas.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977286"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Transformação sem perdas de uma imagem JPEG

Quando você compacta uma imagem JPEG, algumas das informações na imagem são perdidas. Se você abrir um arquivo JPEG, alterar a imagem e salvá-la em outro arquivo JPEG, a qualidade diminuirá. Se você repetir esse processo muitas vezes, verá uma degradação significativa na qualidade da imagem.

Como JPEG é um dos formatos de imagem mais populares na Web e como as pessoas geralmente gostam de modificar imagens JPEG, o GDI+ fornece as seguintes transformações que podem ser executadas em imagens JPEG sem perda de informações:

-   Girar 90 graus
-   Girar 180 graus graus
-   Girar 270 graus graus
-   Inverter horizontalmente
-   Inverter verticalmente

Você pode aplicar uma das transformações mostradas na lista anterior ao chamar o [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de um [**objeto Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Se as seguintes condições são atendidas, a transformação prosseguirá sem perda de informações:

-   O arquivo usado para construir o [**objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) é um arquivo JPEG.
-   A largura e a altura da imagem são múltiplos de 16.

Se a largura e a altura da imagem não são múltiplos de 16, o GDI+ fará o melhor para preservar a qualidade da imagem quando você aplicar uma das transformações de rotação ou invertida mostradas na lista anterior.

Para transformar uma imagem JPEG, inicialize um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) e passe o endereço desse objeto para o [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da [**classe Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Inicialize o **objeto EncoderParameters** para que ele tenha uma matriz que consiste em um [**objeto EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Inicialize esse objeto **EncoderParameter** para que seu membro **Value** aponta para uma variável **ULONG** que contém um dos seguintes elementos da enumeração [**EncoderValue:**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue)

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

De definir **o membro** Guid do objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) como EncoderTransformation.

O aplicativo de console a seguir cria um [**objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) de um arquivo JPEG e salva a imagem em um novo arquivo. Durante o processo de salvar, a imagem é girada em 90 graus. Se a largura e a altura da imagem são múltiplos de 16, o processo de girar e salvar a imagem não causará perda de informações.

A função principal se baseia na função auxiliar GetEncoderClsid, que é mostrada em Recuperando o Identificador de Classe para [um Codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
