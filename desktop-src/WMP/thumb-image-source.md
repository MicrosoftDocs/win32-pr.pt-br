---
title: Origem da imagem em miniatura
description: Origem da imagem em miniatura
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, origem da imagem
- trackbars em capas, origem do Thumb Image
- origem da imagem para capas, trackbars
- Thumb, origem da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005180"
---
# <a name="thumb-image-source"></a><span data-ttu-id="76542-110">Origem da imagem em miniatura</span><span class="sxs-lookup"><span data-stu-id="76542-110">Thumb Image Source</span></span>

<span data-ttu-id="76542-111">Você deve definir o nome do arquivo que contém a imagem do Thumb.</span><span class="sxs-lookup"><span data-stu-id="76542-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="76542-112">Ele deve ser um nome de arquivo válido com a extensão. bmp,. gif,. jpg ou. png.</span><span class="sxs-lookup"><span data-stu-id="76542-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="76542-113">O arquivo deve conter três imagens lado a lado de tamanho idêntico.</span><span class="sxs-lookup"><span data-stu-id="76542-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="76542-114">Eles devem ser adjacentes entre si sem nenhum espaço entre eles.</span><span class="sxs-lookup"><span data-stu-id="76542-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="76542-115">A posição superior esquerda da imagem esquerda deve estar no canto superior esquerdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="76542-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="76542-116">A imagem no lado esquerdo é a imagem normal da imagem em miniatura, e a imagem no meio mostra o estado enviado e a imagem à direita representa o estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="76542-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="76542-117">Talvez você queira tornar as áreas do Thumb Image transparentes.</span><span class="sxs-lookup"><span data-stu-id="76542-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="76542-118">Isso permitirá que você crie imagens thumbs em formas diferentes de retangulares.</span><span class="sxs-lookup"><span data-stu-id="76542-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="76542-119">Qualquer região da imagem do Thumb que você preencher com a cor especificada pelo valor RGB 255, 0, 255 aparecerá transparente em sua capa.</span><span class="sxs-lookup"><span data-stu-id="76542-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76542-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76542-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76542-121">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="76542-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




