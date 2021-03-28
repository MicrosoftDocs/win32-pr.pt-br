---
description: Para exibir uma imagem rasterizada (bitmap) na tela, você precisa de um objeto Image e de um objeto Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Carregando e exibindo bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104968764"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="b3048-103">Carregando e exibindo bitmaps</span><span class="sxs-lookup"><span data-stu-id="b3048-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="b3048-104">Consulte também o [aplicativo de exemplo do WIC Viewer GDI+](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="b3048-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="b3048-105">Para exibir uma imagem rasterizada (bitmap) na tela, você precisa de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b3048-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="b3048-106">Passe o nome de um arquivo (ou um ponteiro para um fluxo) para um construtor de **imagem** .</span><span class="sxs-lookup"><span data-stu-id="b3048-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="b3048-107">Depois de criar um objeto **Image** , passe o endereço desse objeto **Image** para o método **DrawImage** de um objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b3048-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="b3048-108">O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) de um arquivo JPEG e, em seguida, desenha a imagem com seu canto superior esquerdo em (60, 10):</span><span class="sxs-lookup"><span data-stu-id="b3048-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="b3048-109">A ilustração a seguir mostra a imagem desenhada no local especificado.</span><span class="sxs-lookup"><span data-stu-id="b3048-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="b3048-110">captura de tela de uma janela que contém uma imagem, com um texto explicativo para o ponto de origem</span><span class="sxs-lookup"><span data-stu-id="b3048-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="b3048-111">A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais.</span><span class="sxs-lookup"><span data-stu-id="b3048-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="b3048-112">A classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , que herda da classe **Image** , fornece métodos mais especializados para carregar, exibir e manipular imagens rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="b3048-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="b3048-113">Por exemplo, você pode construir um objeto de **bitmap** a partir de um identificador de ícone (HICON).</span><span class="sxs-lookup"><span data-stu-id="b3048-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="b3048-114">O exemplo a seguir obtém um identificador para um ícone e, em seguida, usa esse identificador para construir um objeto de [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="b3048-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="b3048-115">O código exibe o ícone passando o endereço do objeto de **bitmap** para o método **DrawImage** de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b3048-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="b3048-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3048-116">See also</span></span>

[<span data-ttu-id="b3048-117">Aplicativo de exemplo do Visualizador de WIC GDI+</span><span class="sxs-lookup"><span data-stu-id="b3048-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
