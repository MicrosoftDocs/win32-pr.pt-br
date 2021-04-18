---
description: Top-Down vs.
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down x Bottom-Up DIBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756948"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="1ead6-103">Top-Down x Bottom-Up DIBs</span><span class="sxs-lookup"><span data-stu-id="1ead6-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="1ead6-104">Se você for novo na programação de gráficos, poderá esperar que um bitmap seja organizado na memória para que a linha superior da imagem apareça no início do buffer, seguida pela próxima linha e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1ead6-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="1ead6-105">No entanto, isso não é necessariamente o caso.</span><span class="sxs-lookup"><span data-stu-id="1ead6-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="1ead6-106">No Windows, os bitmaps independentes de dispositivo (DIBs) podem ser colocados na memória em duas orientações diferentes, de baixo para cima e de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="1ead6-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="1ead6-107">Em um DIB de baixo para cima, o buffer de imagem começa com a linha inferior de pixels, seguida pela próxima linha e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1ead6-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="1ead6-108">A linha superior da imagem é a última linha no buffer.</span><span class="sxs-lookup"><span data-stu-id="1ead6-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="1ead6-109">Portanto, o primeiro byte na memória é o pixel inferior esquerdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="1ead6-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="1ead6-110">No GDI, todos os DIBs são de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="1ead6-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="1ead6-111">O diagrama a seguir mostra o layout físico de um DIB de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="1ead6-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![DIB de baixo para cima](images/pixel-layout-bottomup.png)

<span data-ttu-id="1ead6-113">Em um DIB de cima para baixo, a ordem das linhas é invertida.</span><span class="sxs-lookup"><span data-stu-id="1ead6-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="1ead6-114">A linha superior da imagem é a primeira linha na memória, seguida pela próxima linha abaixo.</span><span class="sxs-lookup"><span data-stu-id="1ead6-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="1ead6-115">A linha inferior da imagem é a última linha no buffer.</span><span class="sxs-lookup"><span data-stu-id="1ead6-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="1ead6-116">Com um DIB de cima para baixo, o primeiro byte na memória é o pixel superior esquerdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="1ead6-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="1ead6-117">O DirectDraw usa DIBs de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="1ead6-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="1ead6-118">O diagrama a seguir mostra o layout físico de um DIB de cima para baixo:</span><span class="sxs-lookup"><span data-stu-id="1ead6-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![DIB de cima para baixo](images/pixel-layout-topdown.png)

<span data-ttu-id="1ead6-120">Para o DIBs RGB, a orientação da imagem é indicada pelo membro de **doheight** da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="1ead6-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="1ead6-121">Se a **interheight** for positiva, a imagem será de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="1ead6-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="1ead6-122">Se a **interheight** for negativa, a imagem será de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="1ead6-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="1ead6-123">Os DIBs em formatos YUV são sempre de cima para baixo, e o sinal do membro de **monoheight** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="1ead6-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="1ead6-124">Os decodificadores devem oferecer formatos YUV com uma **altura** positiva, mas também devem aceitar formatos YUV com uma **biHeight** negativa e ignorar o sinal.</span><span class="sxs-lookup"><span data-stu-id="1ead6-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="1ead6-125">Além disso, qualquer tipo de DIB que usa um **FOURCC** no membro da **bicompressão** deve expressar sua **altura** como um número positivo, independentemente do que é sua orientação, pois o próprio **FOURCC** identifica um esquema de compactação cuja orientação de imagem deve ser compreendida por qualquer filtro compatível.</span><span class="sxs-lookup"><span data-stu-id="1ead6-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ead6-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ead6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ead6-127">Trabalhando com quadros de vídeo</span><span class="sxs-lookup"><span data-stu-id="1ead6-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



