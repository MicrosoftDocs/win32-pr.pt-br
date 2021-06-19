---
description: Saiba mais sobre como usar imagens, bitmaps e metaarquivos. O Windows GDI+ fornece a classe de imagem para trabalhar com imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Usando imagens, bitmaps e metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395531"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="69c36-104">Usando imagens, bitmaps e metaarquivos</span><span class="sxs-lookup"><span data-stu-id="69c36-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="69c36-105">O Windows GDI+ fornece a classe de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para trabalhar com imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).</span><span class="sxs-lookup"><span data-stu-id="69c36-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="69c36-106">A classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e a classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) herdam da classe **Image** .</span><span class="sxs-lookup"><span data-stu-id="69c36-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="69c36-107">A classe **bitmap** expande os recursos da classe **Image** fornecendo métodos adicionais para carregar, salvar e manipular imagens rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="69c36-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="69c36-108">A classe **Metafile** expande os recursos da classe **Image** fornecendo métodos adicionais para gravar e examinar imagens vetoriais.</span><span class="sxs-lookup"><span data-stu-id="69c36-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="69c36-109">Os tópicos a seguir abordam as classes de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="69c36-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="69c36-110">Carregando e exibindo bitmaps</span><span class="sxs-lookup"><span data-stu-id="69c36-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="69c36-111">Carregando e exibindo metaarquivos</span><span class="sxs-lookup"><span data-stu-id="69c36-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="69c36-112">Gravando metaarquivos</span><span class="sxs-lookup"><span data-stu-id="69c36-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="69c36-113">Cortando e dimensionando imagens</span><span class="sxs-lookup"><span data-stu-id="69c36-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="69c36-114">Girando, refletindo e distorcendo imagens</span><span class="sxs-lookup"><span data-stu-id="69c36-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="69c36-115">Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento</span><span class="sxs-lookup"><span data-stu-id="69c36-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="69c36-116">Criando imagens em miniatura</span><span class="sxs-lookup"><span data-stu-id="69c36-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="69c36-117">Usando um bitmap armazenado em cache para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="69c36-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="69c36-118">Melhorando o desempenho, evitando o dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="69c36-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="69c36-119">Lendo e gravando metadados</span><span class="sxs-lookup"><span data-stu-id="69c36-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



