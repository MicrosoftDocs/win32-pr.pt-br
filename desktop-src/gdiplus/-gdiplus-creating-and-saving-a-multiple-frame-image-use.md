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
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="e716d-103">Criar e salvar uma imagem de vários quadros</span><span class="sxs-lookup"><span data-stu-id="e716d-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="e716d-104">Com determinados formatos de arquivo, você pode salvar várias imagens (quadros) em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="e716d-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="e716d-105">Por exemplo, você pode salvar várias páginas em um único arquivo TIFF.</span><span class="sxs-lookup"><span data-stu-id="e716d-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="e716d-106">Para salvar a primeira página, chame o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="e716d-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="e716d-107">Para salvar as páginas subsequentes, chame o método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) da classe **Image** .</span><span class="sxs-lookup"><span data-stu-id="e716d-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="e716d-108">Não é possível usar [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) para adicionar quadros a um arquivo GIF animado.</span><span class="sxs-lookup"><span data-stu-id="e716d-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="e716d-109">O aplicativo de console a seguir cria um arquivo TIFF com quatro páginas.</span><span class="sxs-lookup"><span data-stu-id="e716d-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="e716d-110">As imagens que se tornam as páginas do arquivo TIFF são provenientes de quatro arquivos de disco: Shapes.bmp, Cereal.gif, Iron.jpg e House.png.</span><span class="sxs-lookup"><span data-stu-id="e716d-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="e716d-111">Primeiro, o Code constrói quatro objetos [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **multi**, **página2**, **page3** e **page4**.</span><span class="sxs-lookup"><span data-stu-id="e716d-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="e716d-112">A princípio, **multi** contém apenas a imagem de Shapes.bmp, mas, eventualmente, contém todas as quatro imagens.</span><span class="sxs-lookup"><span data-stu-id="e716d-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="e716d-113">Como as páginas individuais são adicionadas ao objeto de **várias**  **imagens** , elas também são adicionadas ao arquivo de disco vários frame. tif.</span><span class="sxs-lookup"><span data-stu-id="e716d-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="e716d-114">Observe que o código chama [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (não [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) para salvar a primeira página.</span><span class="sxs-lookup"><span data-stu-id="e716d-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="e716d-115">O primeiro argumento passado para o método Save é o nome do arquivo de disco que eventualmente conterá vários quadros.</span><span class="sxs-lookup"><span data-stu-id="e716d-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="e716d-116">O segundo argumento passado para o método Save especifica o codificador que será usado para converter os dados no objeto de **várias**  [**imagens**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) no formato (neste caso, TIFF) exigido pelo arquivo de disco.</span><span class="sxs-lookup"><span data-stu-id="e716d-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="e716d-117">Esse mesmo codificador é usado automaticamente por todas as chamadas subsequentes para o método SaveAdd do objeto **multi**  **Image** .</span><span class="sxs-lookup"><span data-stu-id="e716d-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="e716d-118">O terceiro argumento passado para o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) é o endereço de um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) .</span><span class="sxs-lookup"><span data-stu-id="e716d-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="e716d-119">O objeto **EncoderParameters** tem uma matriz que contém um único objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="e716d-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="e716d-120">O membro **GUID** desse objeto **EncoderParameter** é definido como EncoderSaveFlag.</span><span class="sxs-lookup"><span data-stu-id="e716d-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="e716d-121">O membro **Value** do objeto **EncoderParameter** aponta para um **ULONG** que contém o valor EncoderValueMultiFrame.</span><span class="sxs-lookup"><span data-stu-id="e716d-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="e716d-122">O código salva a segunda, terceira e quarta páginas chamando o método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) do objeto **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="e716d-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="e716d-123">O primeiro argumento passado para o método SaveAdd é o endereço de um objeto **Image** .</span><span class="sxs-lookup"><span data-stu-id="e716d-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="e716d-124">A imagem nesse objeto de **imagem** é adicionada ao objeto de **várias**  **imagens** e também é adicionada ao arquivo de disco de vários quadros. tif.</span><span class="sxs-lookup"><span data-stu-id="e716d-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="e716d-125">O segundo argumento passado para o método SaveAdd é o endereço do mesmo objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que foi usado pelo método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) .</span><span class="sxs-lookup"><span data-stu-id="e716d-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="e716d-126">A diferença é que o **ULONG** apontado pelo membro de **valor** agora contém o valor EncoderValueFrameDimensionPage.</span><span class="sxs-lookup"><span data-stu-id="e716d-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="e716d-127">A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="e716d-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
