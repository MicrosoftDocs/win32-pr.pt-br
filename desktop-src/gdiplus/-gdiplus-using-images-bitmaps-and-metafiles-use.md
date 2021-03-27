---
description: O Windows GDI+ fornece a classe de imagem para trabalhar com imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Usando imagens, bitmaps e metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010860"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="51a50-103">Usando imagens, bitmaps e metaarquivos</span><span class="sxs-lookup"><span data-stu-id="51a50-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="51a50-104">O Windows GDI+ fornece a classe de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para trabalhar com imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).</span><span class="sxs-lookup"><span data-stu-id="51a50-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="51a50-105">A classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e a classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) herdam da classe **Image** .</span><span class="sxs-lookup"><span data-stu-id="51a50-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="51a50-106">A classe **bitmap** expande os recursos da classe **Image** fornecendo métodos adicionais para carregar, salvar e manipular imagens rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="51a50-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="51a50-107">A classe **Metafile** expande os recursos da classe **Image** fornecendo métodos adicionais para gravar e examinar imagens vetoriais.</span><span class="sxs-lookup"><span data-stu-id="51a50-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="51a50-108">Os tópicos a seguir abordam as classes de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="51a50-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="51a50-109">Carregando e exibindo bitmaps</span><span class="sxs-lookup"><span data-stu-id="51a50-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="51a50-110">Carregando e exibindo metaarquivos</span><span class="sxs-lookup"><span data-stu-id="51a50-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="51a50-111">Gravando metaarquivos</span><span class="sxs-lookup"><span data-stu-id="51a50-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="51a50-112">Cortando e dimensionando imagens</span><span class="sxs-lookup"><span data-stu-id="51a50-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="51a50-113">Girando, refletindo e distorcendo imagens</span><span class="sxs-lookup"><span data-stu-id="51a50-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="51a50-114">Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento</span><span class="sxs-lookup"><span data-stu-id="51a50-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="51a50-115">Criando imagens em miniatura</span><span class="sxs-lookup"><span data-stu-id="51a50-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="51a50-116">Usando um bitmap armazenado em cache para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="51a50-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="51a50-117">Melhorando o desempenho, evitando o dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="51a50-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="51a50-118">Lendo e gravando metadados</span><span class="sxs-lookup"><span data-stu-id="51a50-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



