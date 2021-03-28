---
description: Se você passar apenas o canto superior esquerdo de uma imagem para o método DrawImage, o Windows GDI+ poderá dimensionar a imagem, o que diminuiria o desempenho.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Melhorando o desempenho, evitando o dimensionamento automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967764"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="bae92-103">Melhorando o desempenho, evitando o dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="bae92-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="bae92-104">Se você passar apenas o canto superior esquerdo de uma imagem para o método **DrawImage** , o Windows GDI+ poderá dimensionar a imagem, o que diminuiria o desempenho.</span><span class="sxs-lookup"><span data-stu-id="bae92-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="bae92-105">A chamada a seguir para o método **DrawImage** especifica um canto superior esquerdo de (50, 30), mas não especifica um retângulo de destino:</span><span class="sxs-lookup"><span data-stu-id="bae92-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="bae92-106">Embora essa seja a versão mais fácil do método **DrawImage** em termos do número de argumentos necessários, ela não é necessariamente a mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="bae92-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="bae92-107">Se o número de pontos por polegada no dispositivo de vídeo atual for diferente do número de pontos por polegada no dispositivo em que a imagem foi criada, a GDI+ dimensionará a imagem para que seu tamanho físico no dispositivo de vídeo atual seja o mais próximo possível de seu tamanho físico no dispositivo em que foi criado.</span><span class="sxs-lookup"><span data-stu-id="bae92-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="bae92-108">Se você quiser evitar esse dimensionamento, passe a largura e a altura de um retângulo de destino para o método **DrawImage** .</span><span class="sxs-lookup"><span data-stu-id="bae92-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="bae92-109">O exemplo a seguir desenha a mesma imagem duas vezes.</span><span class="sxs-lookup"><span data-stu-id="bae92-109">The following example draws the same image twice.</span></span> <span data-ttu-id="bae92-110">No primeiro caso, a largura e altura do retângulo de destino não são especificados, e a escala da imagem é ajustada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bae92-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="bae92-111">No segundo caso, a largura e altura (medidas em pixels) do retângulo de destino são especificadas como iguais à largura e altura da imagem original.</span><span class="sxs-lookup"><span data-stu-id="bae92-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="bae92-112">A ilustração a seguir mostra a imagem renderizada duas vezes.</span><span class="sxs-lookup"><span data-stu-id="bae92-112">The following illustration shows the image rendered twice.</span></span>

![captura de tela de uma janela que contém duas versões de uma imagem em escalas diferentes](images/scaledtexture1.png)

 

 



