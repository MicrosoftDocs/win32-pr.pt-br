---
title: Copiar quadros individuais de uma imagem de vários quadros
description: O exemplo a seguir recupera os quadros individuais de um arquivo TIFF de vários quadros.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165469"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="3bcc6-103">Copiar quadros individuais de uma imagem de vários quadros</span><span class="sxs-lookup"><span data-stu-id="3bcc6-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="3bcc6-104">O exemplo a seguir recupera os quadros individuais de um arquivo TIFF de vários quadros.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="3bcc6-105">Quando o arquivo TIFF foi criado, os quadros individuais foram adicionados à dimensão de página (consulte [criando e salvando uma imagem de Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="3bcc6-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="3bcc6-106">O código exibe cada uma das quatro páginas e salva cada página em um arquivo de disco PNG separado.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="3bcc6-107">O código constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo TIFF de vários quadros.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="3bcc6-108">Para recuperar os quadros individuais (páginas), o código chama o método [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) desse objeto **Image** .</span><span class="sxs-lookup"><span data-stu-id="3bcc6-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="3bcc6-109">O primeiro argumento passado para o método **Image:: SelectActiveFrame** é o endereço de um GUID que especifica a dimensão na qual os quadros foram adicionados anteriormente ao arquivo TIFF de vários quadros.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="3bcc6-110">O GUID FrameDimensionPage é definido em Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="3bcc6-111">Outros GUIDs definidos nesse arquivo de cabeçalho são FrameDimensionTime e FrameDimensionResolution.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="3bcc6-112">O segundo argumento passado para o método **Image:: SelectActiveFrame** é o índice baseado em zero da página desejada.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="3bcc6-113">O código depende da função auxiliar GetEncoderClsid, que é mostrada na [recuperação do identificador de classe de um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="3bcc6-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



<span data-ttu-id="3bcc6-114">A ilustração a seguir mostra as páginas individuais, conforme exibido pelo código anterior.</span><span class="sxs-lookup"><span data-stu-id="3bcc6-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![ilustração mostrando uma forma geométrica, uma foto colorida, uma foto monocromática e uma forma geométrica diferente](images/multiframe1.png)

 

 



