---
description: Com determinados formatos de arquivo, você pode salvar várias imagens (quadros) em um único arquivo.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Criar e salvar uma imagem de vários quadros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091474"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Criar e salvar uma imagem de vários quadros

Com determinados formatos de arquivo, você pode salvar várias imagens (quadros) em um único arquivo. Por exemplo, você pode salvar várias páginas em um único arquivo TIFF. Para salvar a primeira página, chame o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Para salvar as páginas subsequentes, chame o método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) da classe **Image** .

> [!Note]  
> Não é possível usar [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) para adicionar quadros a um arquivo GIF animado.

 

O aplicativo de console a seguir cria um arquivo TIFF com quatro páginas. As imagens que se tornam as páginas do arquivo TIFF são provenientes de quatro arquivos de disco: Shapes.bmp, Cereal.gif, Iron.jpg e House.png. Primeiro, o Code constrói quatro objetos [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **multi**, **página2**, **page3** e **page4**. A princípio, **multi** contém apenas a imagem de Shapes.bmp, mas, eventualmente, contém todas as quatro imagens. Como as páginas individuais são adicionadas ao objeto de **várias**  **imagens** , elas também são adicionadas ao arquivo de disco vários frame. tif.

Observe que o código chama [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (não [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) para salvar a primeira página. O primeiro argumento passado para o método Save é o nome do arquivo de disco que eventualmente conterá vários quadros. O segundo argumento passado para o método Save especifica o codificador que será usado para converter os dados no objeto de **várias**  [**imagens**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) no formato (neste caso, TIFF) exigido pelo arquivo de disco. Esse mesmo codificador é usado automaticamente por todas as chamadas subsequentes para o método SaveAdd do objeto **multi**  **Image** .

O terceiro argumento passado para o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) é o endereço de um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) . O objeto **EncoderParameters** tem uma matriz que contém um único objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . O membro **GUID** desse objeto **EncoderParameter** é definido como EncoderSaveFlag. O membro **Value** do objeto **EncoderParameter** aponta para um **ULONG** que contém o valor EncoderValueMultiFrame.

O código salva a segunda, terceira e quarta páginas chamando o método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) do objeto **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . O primeiro argumento passado para o método SaveAdd é o endereço de um objeto **Image** . A imagem nesse objeto de **imagem** é adicionada ao objeto de **várias**  **imagens** e também é adicionada ao arquivo de disco de vários quadros. tif. O segundo argumento passado para o método SaveAdd é o endereço do mesmo objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que foi usado pelo método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) . A diferença é que o **ULONG** apontado pelo membro de **valor** agora contém o valor EncoderValueFrameDimensionPage.

A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
