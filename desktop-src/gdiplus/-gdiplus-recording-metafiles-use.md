---
description: A classe Metafile, que herda da classe Image, permite que você grave uma sequência de comandos de desenho.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Gravando metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967402"
---
# <a name="recording-metafiles"></a><span data-ttu-id="f11b1-103">Gravando metaarquivos</span><span class="sxs-lookup"><span data-stu-id="f11b1-103">Recording Metafiles</span></span>

<span data-ttu-id="f11b1-104">A classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que herda da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , permite que você grave uma sequência de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="f11b1-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="f11b1-105">Os comandos gravados podem ser armazenados na memória, salvos em um arquivo ou salvos em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="f11b1-106">Os metaarquivos podem conter gráficos vetoriais, imagens rasterizadas e texto.</span><span class="sxs-lookup"><span data-stu-id="f11b1-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="f11b1-107">O exemplo a seguir cria um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="f11b1-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="f11b1-108">O código usa o objeto **Metafile** para gravar uma sequência de comandos gráficos e, em seguida, salva os comandos gravados em um arquivo chamado SampleMetafile. EMF.</span><span class="sxs-lookup"><span data-stu-id="f11b1-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="f11b1-109">Observe que o construtor de **metarquivo** recebe um identificador de contexto de dispositivo e o construtor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recebe o endereço do objeto de **metarquivo** .</span><span class="sxs-lookup"><span data-stu-id="f11b1-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="f11b1-110">A gravação é interrompida (e os comandos gravados são salvos no arquivo) quando o objeto de **gráficos** sai do escopo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="f11b1-111">As duas últimas linhas de código exibem o metarquivo, criando um novo objeto de **gráfico** e passando o endereço do objeto de **metarquivo** para o método **DrawImage** desse objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="f11b1-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="f11b1-112">Observe que o código usa o mesmo objeto de **metarquivo** para gravar e exibir (reproduzir) o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> <span data-ttu-id="f11b1-113">Para gravar um metarquivo, você deve construir um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="f11b1-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="f11b1-114">A gravação do metarquivo termina quando esse objeto **gráfico** é excluído ou sai do escopo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="f11b1-115">Um metarquivo contém seu próprio estado de gráfico, que é definido pelo objeto de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usado para gravar o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="f11b1-116">Todas as propriedades do objeto **gráfico** (região do clipe, transformação do mundo, modo de suavização e similares) que você definir durante a gravação do metarquivo serão armazenadas no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="f11b1-117">Quando você exibir o metarquivo, o desenho será feito de acordo com as propriedades armazenadas.</span><span class="sxs-lookup"><span data-stu-id="f11b1-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="f11b1-118">No exemplo a seguir, suponha que o modo de suavização foi definido como SmoothingModeNormal durante a gravação do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f11b1-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="f11b1-119">Embora o modo de suavização do objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usado para reprodução seja definido como SmoothingModeHighQuality, o metarquivo será reproduzido de acordo com a configuração SmoothingModeNormal.</span><span class="sxs-lookup"><span data-stu-id="f11b1-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="f11b1-120">É o modo de suavização definido durante a gravação que é importante, não o modo de suavização definido antes da reprodução.</span><span class="sxs-lookup"><span data-stu-id="f11b1-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



