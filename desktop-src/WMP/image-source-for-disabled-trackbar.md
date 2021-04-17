---
title: Origem da imagem para TrackBar desabilitada
description: Origem da imagem para TrackBar desabilitada
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, origem da imagem
- origem da imagem para capas, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780223"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="b230c-108">Origem da imagem para TrackBar desabilitada</span><span class="sxs-lookup"><span data-stu-id="b230c-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="b230c-109">Você deve definir a origem da imagem que deseja exibir quando um TrackBar é desabilitado, usando o tipo de bitmap do qual você deseja desenhar a imagem.</span><span class="sxs-lookup"><span data-stu-id="b230c-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="b230c-110">A imagem exibida geralmente estará dentro do super arquivo ou se você estiver criando uma capa para o Windows Media Player 10 Mobile, a imagem estaria dentro do arquivo SeekThumb.</span><span class="sxs-lookup"><span data-stu-id="b230c-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="b230c-111">Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="b230c-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="b230c-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.</span><span class="sxs-lookup"><span data-stu-id="b230c-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="b230c-113">Por exemplo, para usar uma imagem do bitmap SeekThumb que tem uma posição superior e esquerda de 50, 60 pixels, digite:</span><span class="sxs-lookup"><span data-stu-id="b230c-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="b230c-114">Você deve definir um local de imagem para uma imagem TrackBar desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b230c-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="b230c-115">Se você não quiser exibir uma nova imagem, poderá definir a imagem de plano de fundo como sua imagem desabilitada com um deslocamento de 0, 0:</span><span class="sxs-lookup"><span data-stu-id="b230c-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="b230c-116">No exemplo anterior, 50, 60 representa o local do botão com o qual você está trabalhando no arquivo SeekThumb (nesse caso, o mesmo local que o botão no bitmap em segundo plano).</span><span class="sxs-lookup"><span data-stu-id="b230c-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="b230c-117">No entanto, é altamente recomendável que você exiba uma imagem desabilitada para todos os trackbars para dar ao usuário uma indicação visual, pois o trackbars não será utilizável em determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="b230c-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="b230c-118">Por exemplo, Seek trackbars pode ser desabilitado quando a playlist atual estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="b230c-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b230c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b230c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b230c-120">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="b230c-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




