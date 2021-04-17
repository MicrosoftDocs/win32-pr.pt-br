---
description: Trabalhando com RGB de 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Trabalhando com RGB de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812969"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="8a941-103">Trabalhando com RGB de 16 bits</span><span class="sxs-lookup"><span data-stu-id="8a941-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="8a941-104">Dois formatos são definidos para RGB não compactado de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="8a941-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="8a941-105">MEDIASUBTYPE \_ 555 usa cinco bits cada para os componentes vermelho, verde e azul em um pixel.</span><span class="sxs-lookup"><span data-stu-id="8a941-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="8a941-106">O bit mais significativo na **palavra** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8a941-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="8a941-107">MEDIASUBTYPE \_ 565 usa cinco bits para os componentes vermelho e azul e seis bits para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="8a941-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="8a941-108">Esse formato reflete o fato de que a visão humana é mais sensível às partes verdes do espectro visível.</span><span class="sxs-lookup"><span data-stu-id="8a941-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="8a941-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="8a941-109">**RGB 565**</span></span>

<span data-ttu-id="8a941-110">Para extrair os componentes de cor de uma imagem RGB 565, trate cada pixel como um tipo de **palavra** e use as seguintes máscaras de bits:</span><span class="sxs-lookup"><span data-stu-id="8a941-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="8a941-111">Obtenha os componentes de cor de um pixel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8a941-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="8a941-112">Lembre-se de que os canais vermelho e azul são de 5 bits e o canal verde é de 6 bits.</span><span class="sxs-lookup"><span data-stu-id="8a941-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="8a941-113">Para converter esses valores em componentes de 8 bits (para RGB de 24 ou 32 bits), você deve mover o número apropriado de bits para a esquerda:</span><span class="sxs-lookup"><span data-stu-id="8a941-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="8a941-114">Inverta esse processo para criar um pixel RGB 565.</span><span class="sxs-lookup"><span data-stu-id="8a941-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="8a941-115">Supondo que os valores de cor foram truncados para o número correto de bits:</span><span class="sxs-lookup"><span data-stu-id="8a941-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="8a941-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="8a941-116">**RGB 555**</span></span>

<span data-ttu-id="8a941-117">Trabalhar com RGB 555 é essencialmente o mesmo que o RGB 565, exceto que as máscaras de bits e as operações de deslocamento de bits são diferentes.</span><span class="sxs-lookup"><span data-stu-id="8a941-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="8a941-118">Para obter os componentes de cor de um pixel RGB 555, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a941-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="8a941-119">Para empacotar os valores de cor vermelho, verde e azul em um pixel RGB 555, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a941-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="8a941-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a941-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a941-121">Subtipos de vídeo RGB não compactados</span><span class="sxs-lookup"><span data-stu-id="8a941-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



