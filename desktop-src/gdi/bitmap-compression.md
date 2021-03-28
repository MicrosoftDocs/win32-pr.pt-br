---
description: O Windows dá suporte a formatos para compactação de bitmaps que definem suas cores com 8 ou 4 bits por pixel. A compactação reduz o armazenamento de disco e memória necessário para o bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compactação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091223"
---
# <a name="bitmap-compression"></a><span data-ttu-id="8f08e-104">Compactação de bitmap</span><span class="sxs-lookup"><span data-stu-id="8f08e-104">Bitmap Compression</span></span>

<span data-ttu-id="8f08e-105">O Windows dá suporte a formatos para compactação de bitmaps que definem suas cores com 8 ou 4 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="8f08e-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="8f08e-106">A compactação reduz o armazenamento de disco e memória necessário para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="8f08e-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="8f08e-107">Quando o membro de **compactação** da estrutura de cabeçalho de informações de bitmap é bi \_ RLE8, um formato RLE (codificação de comprimento de execução) é usado para compactar um bitmap de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8f08e-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="8f08e-108">Esse formato pode ser compactado em modos codificados ou absolutos.</span><span class="sxs-lookup"><span data-stu-id="8f08e-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="8f08e-109">Ambos os modos podem ocorrer em qualquer lugar no mesmo bitmap:</span><span class="sxs-lookup"><span data-stu-id="8f08e-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="8f08e-110">O *modo codificado* consiste em dois bytes: o primeiro byte Especifica o número de pixels consecutivos a serem desenhados usando o índice de cores contido no segundo byte.</span><span class="sxs-lookup"><span data-stu-id="8f08e-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="8f08e-111">Além disso, o primeiro byte do par pode ser definido como zero para indicar um caractere de escape que denota o final de uma linha, o final de um bitmap ou um Delta, dependendo do valor do segundo byte.</span><span class="sxs-lookup"><span data-stu-id="8f08e-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="8f08e-112">A interpretação do escape depende do valor do segundo byte do par, que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f08e-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="8f08e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8f08e-113">Value</span></span> | <span data-ttu-id="8f08e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8f08e-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f08e-115">0</span><span class="sxs-lookup"><span data-stu-id="8f08e-115">0</span></span>     | <span data-ttu-id="8f08e-116">Fim da linha.</span><span class="sxs-lookup"><span data-stu-id="8f08e-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="8f08e-117">1</span><span class="sxs-lookup"><span data-stu-id="8f08e-117">1</span></span>     | <span data-ttu-id="8f08e-118">Fim do bitmap.</span><span class="sxs-lookup"><span data-stu-id="8f08e-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="8f08e-119">2</span><span class="sxs-lookup"><span data-stu-id="8f08e-119">2</span></span>     | <span data-ttu-id="8f08e-120">Trifásico.</span><span class="sxs-lookup"><span data-stu-id="8f08e-120">Delta.</span></span> <span data-ttu-id="8f08e-121">Os 2 bytes após o escape contêm valores não assinados indicando os deslocamentos horizontal e vertical do próximo pixel da posição atual.</span><span class="sxs-lookup"><span data-stu-id="8f08e-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="8f08e-122">No *modo absoluto*, o primeiro byte é zero e o segundo byte é um valor no intervalo de 03H a FFH.</span><span class="sxs-lookup"><span data-stu-id="8f08e-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="8f08e-123">O segundo byte representa o número de bytes a seguir, cada um contendo o índice de cores de um único pixel.</span><span class="sxs-lookup"><span data-stu-id="8f08e-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="8f08e-124">Quando o segundo byte é dois ou menos, o escape tem o mesmo significado que o modo codificado.</span><span class="sxs-lookup"><span data-stu-id="8f08e-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="8f08e-125">No modo absoluto, cada execução deve estar alinhada em um limite de palavra.</span><span class="sxs-lookup"><span data-stu-id="8f08e-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="8f08e-126">O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="8f08e-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="8f08e-127">O bitmap é expandido da seguinte maneira (valores de dois dígitos representam um índice de cores para um único pixel):</span><span class="sxs-lookup"><span data-stu-id="8f08e-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="8f08e-128">Quando o membro de **compactação** é bi \_ RLE4, o bitmap é compactado usando um formato de codificação de comprimento de execução para um bitmap de 4 bits, que também usa modos codificados e absolutos:</span><span class="sxs-lookup"><span data-stu-id="8f08e-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="8f08e-129">No modo codificado, o primeiro byte do par contém o número de pixels a serem desenhados usando os índices de cores no segundo byte.</span><span class="sxs-lookup"><span data-stu-id="8f08e-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="8f08e-130">O segundo byte contém dois índices de cores, um em seus quatro bits de ordem superior e outro em seus 4 bits de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="8f08e-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="8f08e-131">O primeiro dos pixels é desenhado usando a cor especificada pelos quatro bits de ordem superior, o segundo é desenhado usando a cor nos 4 bits de ordem inferior, o terceiro é desenhado usando a cor nos quatro bits de ordem superior e assim por diante, até que todos os pixels especificados pelo primeiro byte tenham sido desenhados.</span><span class="sxs-lookup"><span data-stu-id="8f08e-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="8f08e-132">No modo absoluto, o primeiro byte é zero.</span><span class="sxs-lookup"><span data-stu-id="8f08e-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="8f08e-133">O segundo byte contém o número de índices de cores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f08e-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="8f08e-134">Os bytes subsequentes contêm índices de cores em seus 4 bits de ordem alta e baixa, um índice de cor para cada pixel.</span><span class="sxs-lookup"><span data-stu-id="8f08e-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="8f08e-135">No modo absoluto, cada execução deve estar alinhada em um limite de palavra.</span><span class="sxs-lookup"><span data-stu-id="8f08e-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="8f08e-136">Os escapes de fim de linha, fim de bitmap e Delta descritos para BI \_ RLE8 também se aplicam à \_ compactação de bi RLE4.</span><span class="sxs-lookup"><span data-stu-id="8f08e-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="8f08e-137">O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 4 bits:</span><span class="sxs-lookup"><span data-stu-id="8f08e-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="8f08e-138">O bitmap é expandido da seguinte maneira (valores de dígito único representam um índice de cor para um único pixel):</span><span class="sxs-lookup"><span data-stu-id="8f08e-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



