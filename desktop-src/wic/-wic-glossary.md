---
description: Define os termos que são usados no WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossário do componente de imagem do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783698"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="6d368-103">Glossário do componente de imagem do Windows</span><span class="sxs-lookup"><span data-stu-id="6d368-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="6d368-104">B</span><span class="sxs-lookup"><span data-stu-id="6d368-104">B</span></span>

<dl> <dt>

<span data-ttu-id="6d368-105">**profundidade de bits**</span><span class="sxs-lookup"><span data-stu-id="6d368-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-106">O número de valores de cor que podem ser atribuídos a um único pixel em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="6d368-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="6d368-107">A profundidade de cor pode variar de 1 bit (preto e branco) a 32 bits (mais de 16,7 milhões cores).</span><span class="sxs-lookup"><span data-stu-id="6d368-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="6d368-108">Consulte também: profundidade de cor</span><span class="sxs-lookup"><span data-stu-id="6d368-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="6d368-109">**bits por pixel (BPP)**</span><span class="sxs-lookup"><span data-stu-id="6d368-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-110">O número de bits que representam o valor de cor de cada pixel em uma imagem digitalizada.</span><span class="sxs-lookup"><span data-stu-id="6d368-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="6d368-111">Consulte também: BPP</span><span class="sxs-lookup"><span data-stu-id="6d368-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="6d368-112">C</span><span class="sxs-lookup"><span data-stu-id="6d368-112">C</span></span>

<dl> <dt>

<span data-ttu-id="6d368-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="6d368-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-114">Um objeto IWICBitmapClipper.</span><span class="sxs-lookup"><span data-stu-id="6d368-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-115">**codec**</span><span class="sxs-lookup"><span data-stu-id="6d368-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-116">Um filtro que compacta (codifica) ou descompacta (decodifica) um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="6d368-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-117">**contexto de cor**</span><span class="sxs-lookup"><span data-stu-id="6d368-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-118">Uma abstração para um perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="6d368-118">An abstraction for a color profile.</span></span> <span data-ttu-id="6d368-119">O perfil pode ser carregado de um arquivo (por ex. "sRGB Color Space Profile. icm") ou de um buffer de memória obtido pela leitura.</span><span class="sxs-lookup"><span data-stu-id="6d368-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="6d368-120">As informações de contexto de cor são definidas pela interface IWICColorContext para o WIC e são recuperadas com o método GetColorContext.</span><span class="sxs-lookup"><span data-stu-id="6d368-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-121">**transformação de cor**</span><span class="sxs-lookup"><span data-stu-id="6d368-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-122">Mapear cores do contexto de cor de origem para o contexto de cor de destino em um determinado formato de pixel de saída.</span><span class="sxs-lookup"><span data-stu-id="6d368-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-123">**Modelo de cores CYMK**</span><span class="sxs-lookup"><span data-stu-id="6d368-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-124">O espaço de cores multidimensional que consiste nas intensidades ciano, magenta, amarelo e preto que compõem uma determinada cor.</span><span class="sxs-lookup"><span data-stu-id="6d368-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="6d368-125">D</span><span class="sxs-lookup"><span data-stu-id="6d368-125">D</span></span>

<dl> <dt>

<span data-ttu-id="6d368-126">**decodificador**</span><span class="sxs-lookup"><span data-stu-id="6d368-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-127">Consulte outro termo: codec</span><span class="sxs-lookup"><span data-stu-id="6d368-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="6d368-128">E</span><span class="sxs-lookup"><span data-stu-id="6d368-128">E</span></span>

<dl> <dt>

<span data-ttu-id="6d368-129">**fita**</span><span class="sxs-lookup"><span data-stu-id="6d368-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-130">Consulte outro termo: codec</span><span class="sxs-lookup"><span data-stu-id="6d368-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="6d368-131">L</span><span class="sxs-lookup"><span data-stu-id="6d368-131">L</span></span>

<dl> <dt>

<span data-ttu-id="6d368-132">**Compact**</span><span class="sxs-lookup"><span data-stu-id="6d368-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-133">Um tipo de compactação que garante que os dados originais possam ser recuperados exatamente, sem perda na qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="6d368-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-134">**com perdas**</span><span class="sxs-lookup"><span data-stu-id="6d368-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-135">Um processo para compactação de dados em que as informações consideradas desnecessárias é removido e não pode ser recuperado após a descompactação.</span><span class="sxs-lookup"><span data-stu-id="6d368-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="6d368-136">Normalmente usado com áudio e dados visuais em que uma pequena degradação da qualidade é aceitável.</span><span class="sxs-lookup"><span data-stu-id="6d368-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="6d368-137">M</span><span class="sxs-lookup"><span data-stu-id="6d368-137">M</span></span>

<dl> <dt>

<span data-ttu-id="6d368-138">**apartamento multithread (MTA)**</span><span class="sxs-lookup"><span data-stu-id="6d368-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-139">Uma forma de multithreading com suporte do COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="6d368-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="6d368-140">Em um modelo de apartamento multi-threaded, todos os threads no processo que foram inicializados como de thread livre residem em um único apartamento.</span><span class="sxs-lookup"><span data-stu-id="6d368-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="6d368-141">N</span><span class="sxs-lookup"><span data-stu-id="6d368-141">N</span></span>

<dl> <dt>

<span data-ttu-id="6d368-142">**formato de pixel nativo**</span><span class="sxs-lookup"><span data-stu-id="6d368-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-143">Um dos formatos de pixel fornecidos pelo WIC, no qual o layout de memória de cada pixel em um bitmap é descrito.</span><span class="sxs-lookup"><span data-stu-id="6d368-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="6d368-144">P</span><span class="sxs-lookup"><span data-stu-id="6d368-144">P</span></span>

<dl> <dt>

<span data-ttu-id="6d368-145">**Palette**</span><span class="sxs-lookup"><span data-stu-id="6d368-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-146">Conjunto de cores usado por um objeto ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d368-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-147">**política de metadados de foto**</span><span class="sxs-lookup"><span data-stu-id="6d368-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-148">A política do Windows para leitura, gravação e remoção de metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="6d368-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-149">**formato de pixel**</span><span class="sxs-lookup"><span data-stu-id="6d368-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-150">Tamanho e organização de componentes de cor de pixel na memória.</span><span class="sxs-lookup"><span data-stu-id="6d368-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="6d368-151">Ele é especificado pelo número total de bits usados por pixel e pelo número de bits usados para armazenar os componentes vermelho, verde, azul e alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="6d368-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="6d368-152">Por exemplo, o formato de pixel RGB24 usa 24 bits para armazenar uma cor de pixel, com oito bits cada para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="6d368-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="6d368-153">O formato de pixel ARGB32 usa 32 bits, com 24 bits de informações de cores e 8 bits de informações de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="6d368-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="6d368-154">**decodificação progressiva**</span><span class="sxs-lookup"><span data-stu-id="6d368-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-155">O processo de decodificação de imagens que foram codificadas com informações sobre os diferentes níveis de decodificação.</span><span class="sxs-lookup"><span data-stu-id="6d368-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="6d368-156">S</span><span class="sxs-lookup"><span data-stu-id="6d368-156">S</span></span>

<dl> <dt>

<span data-ttu-id="6d368-157">**fluxo**</span><span class="sxs-lookup"><span data-stu-id="6d368-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-158">Refere-se a uma interface COM de IStream que pode ser usada para ler ou gravar dados em arquivos, memória ou locais de rede em sequência.</span><span class="sxs-lookup"><span data-stu-id="6d368-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="6d368-159">T</span><span class="sxs-lookup"><span data-stu-id="6d368-159">T</span></span>

<dl> <dt>

<span data-ttu-id="6d368-160">**curva de Tom**</span><span class="sxs-lookup"><span data-stu-id="6d368-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-161">Um grafo usado em fotos digitais que exibe o intervalo de tons da imagem.</span><span class="sxs-lookup"><span data-stu-id="6d368-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="6d368-162">W</span><span class="sxs-lookup"><span data-stu-id="6d368-162">W</span></span>

<dl> <dt>

<span data-ttu-id="6d368-163">**Windows Imaging Component (WIC)**</span><span class="sxs-lookup"><span data-stu-id="6d368-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="6d368-164">Uma plataforma extensível que fornece uma API de nível baixo para imagens digitais.</span><span class="sxs-lookup"><span data-stu-id="6d368-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



