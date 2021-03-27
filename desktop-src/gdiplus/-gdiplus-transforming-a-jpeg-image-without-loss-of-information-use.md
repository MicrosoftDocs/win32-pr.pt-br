---
title: Transformação sem perdas de uma imagem JPEG
description: Quando você compacta uma imagem JPEG, algumas das informações na imagem são perdidas.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967398"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="4deba-103">Transformação sem perdas de uma imagem JPEG</span><span class="sxs-lookup"><span data-stu-id="4deba-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="4deba-104">Quando você compacta uma imagem JPEG, algumas das informações na imagem são perdidas.</span><span class="sxs-lookup"><span data-stu-id="4deba-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="4deba-105">Se você abrir um arquivo JPEG, alterar a imagem e salvá-la em outro arquivo JPEG, a qualidade diminuirá.</span><span class="sxs-lookup"><span data-stu-id="4deba-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="4deba-106">Se você repetir esse processo muitas vezes, verá uma degradação substancial na qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="4deba-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="4deba-107">Como o JPEG é um dos formatos de imagem mais populares na Web, e como as pessoas frequentemente gostam de modificar imagens JPEG, a GDI+ fornece as seguintes transformações que podem ser executadas em imagens JPEG sem perda de informações:</span><span class="sxs-lookup"><span data-stu-id="4deba-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="4deba-108">Girar 90 graus</span><span class="sxs-lookup"><span data-stu-id="4deba-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="4deba-109">Girar 180 graus</span><span class="sxs-lookup"><span data-stu-id="4deba-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="4deba-110">Girar 270 graus</span><span class="sxs-lookup"><span data-stu-id="4deba-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="4deba-111">Inverter horizontalmente</span><span class="sxs-lookup"><span data-stu-id="4deba-111">Flip horizontally</span></span>
-   <span data-ttu-id="4deba-112">Inverter verticalmente</span><span class="sxs-lookup"><span data-stu-id="4deba-112">Flip vertically</span></span>

<span data-ttu-id="4deba-113">Você pode aplicar uma das transformações mostradas na lista anterior ao chamar o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de um objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4deba-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="4deba-114">Se as condições a seguir forem atendidas, a transformação continuará sem perda de informações:</span><span class="sxs-lookup"><span data-stu-id="4deba-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="4deba-115">O arquivo usado para construir o objeto de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) é um arquivo JPEG.</span><span class="sxs-lookup"><span data-stu-id="4deba-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="4deba-116">A largura e a altura da imagem são múltiplos de 16.</span><span class="sxs-lookup"><span data-stu-id="4deba-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="4deba-117">Se a largura e a altura da imagem não forem ambas múltiplas de 16, a GDI+ fará o melhor para preservar a qualidade da imagem quando você aplicar uma das transformações de rotação ou inversão mostradas na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="4deba-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="4deba-118">Para transformar uma imagem JPEG, inicialize um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) e passe o endereço desse objeto para o método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4deba-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="4deba-119">Inicialize o objeto **EncoderParameters** para que ele tenha uma matriz que consiste em um objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="4deba-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="4deba-120">Inicialize esse objeto **EncoderParameter** para que seu membro de **valor** aponte para uma variável **ULONG** que contém um dos seguintes elementos da enumeração [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="4deba-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="4deba-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="4deba-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="4deba-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="4deba-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="4deba-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="4deba-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="4deba-124">EncoderValueTransformFlipHorizontal,</span><span class="sxs-lookup"><span data-stu-id="4deba-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="4deba-125">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="4deba-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="4deba-126">Defina o membro **GUID** do objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) como EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="4deba-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="4deba-127">O aplicativo de console a seguir cria um objeto de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de um arquivo JPEG e salva a imagem em um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="4deba-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="4deba-128">Durante o processo de salvamento, a imagem é girada 90 graus.</span><span class="sxs-lookup"><span data-stu-id="4deba-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="4deba-129">Se a largura e a altura da imagem forem múltiplos de 16, o processo de girar e salvar a imagem não causará perda de informações.</span><span class="sxs-lookup"><span data-stu-id="4deba-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="4deba-130">A função main se baseia na função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="4deba-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
