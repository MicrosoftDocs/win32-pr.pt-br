---
title: Codificação de taxa de bits constante (CBR)
description: Codificação de taxa de bits constante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- SDK do Windows Media Format, codificação de CBR
- SDK do Windows Media Format, taxa de bits constante (CBR)
- codecs, codificação de CBR
- codecs, taxa de bits constante (CBR)
- taxa de bits constante (CBR)
- CBR (taxa de bits constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364349"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="842f9-109">Codificação de taxa de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="842f9-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="842f9-110">A codificação de taxa de bits constante (CBR) é o método padrão de codificação com o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="842f9-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="842f9-111">Ao usar a codificação de CBR, você especifica a taxa de bits de destino para um fluxo e o codec usa qualquer quantidade de compactação necessária para obtê-la.</span><span class="sxs-lookup"><span data-stu-id="842f9-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="842f9-112">Com a codificação CBR, a taxa de bits e o tamanho do fluxo codificado são conhecidos antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="842f9-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="842f9-113">Por exemplo, se você estiver codificando uma música de três minutos a 32.000 bits por segundo, saberá que o tamanho do arquivo será de cerca de 704 quilobytes (32.000 bps x 180 segundos/8 bits por byte/1.024).</span><span class="sxs-lookup"><span data-stu-id="842f9-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="842f9-114">Você também sabe que a largura de banda necessária para transmitir o conteúdo codificado é de cerca de 32.000 bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="842f9-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="842f9-115">A codificação de taxa de bits de variável restrita (descrita na seção a seguir) também permite que você saiba a taxa de bits antes da codificação, mas como a taxa é variável, o arquivo resultante não pode ser transmitido com eficiência como um arquivo codificado no modo CBR.</span><span class="sxs-lookup"><span data-stu-id="842f9-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="842f9-116">Com a CBR, a taxa de bits ao longo do tempo sempre permanece próxima à taxa de bits média ou de destino, e a quantidade de variação pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="842f9-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="842f9-117">A desvantagem da codificação CBR é que a qualidade do conteúdo codificado não será constante.</span><span class="sxs-lookup"><span data-stu-id="842f9-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="842f9-118">Como algum conteúdo é mais difícil de ser compactado, partes de um fluxo de CBR serão de menor qualidade do que outras.</span><span class="sxs-lookup"><span data-stu-id="842f9-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="842f9-119">Por exemplo, um filme típico tem algumas cenas que são razoavelmente estáticas e algumas cenas que estão cheias de ação.</span><span class="sxs-lookup"><span data-stu-id="842f9-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="842f9-120">Se você codificar um filme usando CBR, os bastidores estáticos e, portanto, fáceis de codificar com eficiência, serão de maior qualidade do que as cenas de ação, que são muito mais difíceis de codificar com eficiência.</span><span class="sxs-lookup"><span data-stu-id="842f9-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="842f9-121">A codificação de CBR também pode resultar em uma qualidade inconsistente de um arquivo para outro.</span><span class="sxs-lookup"><span data-stu-id="842f9-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="842f9-122">Se você usar a CBR para codificar várias músicas de diferentes gêneros na mesma taxa de bits, poderá notar alguma diferença na qualidade entre elas.</span><span class="sxs-lookup"><span data-stu-id="842f9-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="842f9-123">Em geral, as variações na qualidade de um arquivo CBR são mais pronunciadas em taxas de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="842f9-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="842f9-124">Em taxas de bits mais altas, a qualidade de um arquivo codificado em CBR ainda variará, mas os problemas de qualidade serão menos perceptíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="842f9-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="842f9-125">Ao usar a codificação de CBR, você deve definir a largura de banda tão alta quanto o cenário de entrega permitir.</span><span class="sxs-lookup"><span data-stu-id="842f9-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="842f9-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="842f9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="842f9-127">**Escolhendo um método de codificação**</span><span class="sxs-lookup"><span data-stu-id="842f9-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="842f9-128">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="842f9-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="842f9-129">**Codificação de taxa de bits variável (VBR)**</span><span class="sxs-lookup"><span data-stu-id="842f9-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




