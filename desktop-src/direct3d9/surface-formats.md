---
description: No Direct3D, todas as imagens bidimensionais (2D) são representadas por um intervalo linear de memória chamado superfície.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formatos de superfície (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087703"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="b0143-103">Formatos de superfície (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0143-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="b0143-104">No Direct3D, todas as imagens bidimensionais (2D) são representadas por um intervalo linear de memória chamado superfície.</span><span class="sxs-lookup"><span data-stu-id="b0143-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="b0143-105">Uma superfície pode ser considerada como uma matriz 2D, em que cada elemento contém um valor de cor representando uma pequena seção da imagem, chamada pixel.</span><span class="sxs-lookup"><span data-stu-id="b0143-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="b0143-106">O nível de detalhe de uma imagem é definido pelo número de pixels necessários para representar a imagem e o número de bits necessários para o espectro de cores da imagem.</span><span class="sxs-lookup"><span data-stu-id="b0143-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="b0143-107">Por exemplo, uma imagem com 800 pixels de largura por 600 pixels de altura com 32 bits de cor para cada pixel (escrito como 800x600x32) será mais detalhada do que uma imagem com 640 pixels de largura por 480 pixels de altura com 16 bits de cor para cada pixel (escrito como 640x480x16).</span><span class="sxs-lookup"><span data-stu-id="b0143-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="b0143-108">Da mesma forma, a imagem mais detalhada exigirá uma superfície maior para armazenar os dados.</span><span class="sxs-lookup"><span data-stu-id="b0143-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="b0143-109">Para uma imagem 800x600x32, as dimensões da matriz da superfície serão 800x600 e cada elemento conterá um valor de 32 bits para representar sua cor.</span><span class="sxs-lookup"><span data-stu-id="b0143-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="b0143-110">Todas as superfícies têm um tamanho e armazenam um número específico de bits que representam cores.</span><span class="sxs-lookup"><span data-stu-id="b0143-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="b0143-111">Os bits que representam a cor são separados em elementos de cor individuais: vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="b0143-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="b0143-112">No Direct3D, todos os elementos de cor são definidos pelo tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="b0143-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="b0143-113">Um formato de cor do Direct3D é dividido no número de bytes reservados para cada cor.</span><span class="sxs-lookup"><span data-stu-id="b0143-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="b0143-114">Por exemplo, um formato de cor de 16 bits no Direct3D é definido como D3DFMT \_ R5G6B5, em que 5 bits são reservados para vermelho (R), 6 bits para verde (G) e 5 bits para azul (B).</span><span class="sxs-lookup"><span data-stu-id="b0143-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0143-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0143-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0143-116">Superfícies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b0143-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



