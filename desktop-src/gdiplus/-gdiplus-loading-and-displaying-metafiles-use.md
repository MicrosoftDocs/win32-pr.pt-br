---
description: A classe Image fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais. A classe Metafile, que herda da classe Image, fornece métodos mais especializados para gravar, exibir e examinar imagens vetoriais.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Carregando e exibindo metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010474"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="89ce9-104">Carregando e exibindo metaarquivos</span><span class="sxs-lookup"><span data-stu-id="89ce9-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="89ce9-105">A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais.</span><span class="sxs-lookup"><span data-stu-id="89ce9-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="89ce9-106">A classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que herda da classe **Image** , fornece métodos mais especializados para gravar, exibir e examinar imagens vetoriais.</span><span class="sxs-lookup"><span data-stu-id="89ce9-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="89ce9-107">Para exibir uma imagem de vetor (metarquivo) na tela, você precisa de um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e um objeto de [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="89ce9-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="89ce9-108">Passe o nome de um arquivo (ou um ponteiro para um fluxo) para um construtor de **imagem** .</span><span class="sxs-lookup"><span data-stu-id="89ce9-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="89ce9-109">Depois de criar um objeto **Image** , passe o endereço desse objeto **Image** para o método **DrawImage** de um objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="89ce9-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="89ce9-110">O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) de um arquivo EMF (metarquivo avançado) e, em seguida, desenha a imagem com seu canto superior esquerdo em (60, 10):</span><span class="sxs-lookup"><span data-stu-id="89ce9-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="89ce9-111">A ilustração a seguir mostra a imagem desenhada no local especificado.</span><span class="sxs-lookup"><span data-stu-id="89ce9-111">The following illustration shows the image drawn at the specified location.</span></span>

![captura de tela de uma janela que contém uma imagem e especifica o ponto de origem](images/imageposition2.png)

 

 



