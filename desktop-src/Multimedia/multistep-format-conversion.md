---
title: Conversão de formato de várias etapas
description: Conversão de formato de várias etapas
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gerenciador de compactação de áudio (ACM), convertendo dados
- ACM (Gerenciador de compactação de áudio), convertendo dados
- Exemplos do ACM, convertendo dados
- convertendo dados
- função acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916328"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="2d522-108">Conversão de formato de várias etapas</span><span class="sxs-lookup"><span data-stu-id="2d522-108">Multistep Format Conversion</span></span>

<span data-ttu-id="2d522-109">Às vezes, o ACM não pode converter dados de um formato para outro em uma única etapa.</span><span class="sxs-lookup"><span data-stu-id="2d522-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="2d522-110">Por exemplo, um aplicativo pode precisar converter dados estéreo de 16 bits 44-kHz para a ADPCM do mono de 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="2d522-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="2d522-111">Se o compressor ou o descompactador não puder fazer essa conversão diretamente, o aplicativo poderá tentar em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="2d522-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="2d522-112">Isso geralmente significa fazer uma conversão entre dois formatos PCM e, em seguida, outra conversão para o tipo de formato final.</span><span class="sxs-lookup"><span data-stu-id="2d522-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="2d522-113">Para converter em duas etapas, use a função [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) para encontrar um formato PCM que corresponda ao formato ADPCM.</span><span class="sxs-lookup"><span data-stu-id="2d522-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="2d522-114">Em seguida, use dois fluxos de conversão para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="2d522-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="2d522-115">Por exemplo, execute uma conversão de PCM estéreo de 16 bits, 44-kHz para mono de 16 bits, 11-kHz e, em seguida, converta de mono de 16 bits, de 11 kHz a 11-kHz mono ADPCM.</span><span class="sxs-lookup"><span data-stu-id="2d522-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="2d522-116">A conversão em várias etapas também ocorre quando o formato de origem ou destino não é PCM.</span><span class="sxs-lookup"><span data-stu-id="2d522-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="2d522-117">Se o formato de origem não for PCM, ele deverá ser alterado para um formato PCM antes da conversão.</span><span class="sxs-lookup"><span data-stu-id="2d522-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="2d522-118">Se o formato de destino não for PCM, a origem deverá ser convertida em um formato PCM intermediário e, em seguida, convertida no formato de destino final.</span><span class="sxs-lookup"><span data-stu-id="2d522-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="2d522-119">As conversões mais diretas ocorrem quando os formatos de origem e destino são ambos formatos PCM.</span><span class="sxs-lookup"><span data-stu-id="2d522-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="2d522-120">Quando o formato de origem ou destino não é PCM, a conversão pode exigir uma etapa adicional.</span><span class="sxs-lookup"><span data-stu-id="2d522-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="2d522-121">Se os formatos de origem e destino não forem PCM, a conversão geralmente exigirá mais de uma etapa e, em alguns casos, a conversão poderá não ser possível.</span><span class="sxs-lookup"><span data-stu-id="2d522-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




