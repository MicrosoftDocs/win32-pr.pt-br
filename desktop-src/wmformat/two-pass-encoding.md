---
title: Codificação de Two-Pass
description: Codificação de Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codificação em duas passagens
- SDK de formato de mídia do Windows, codificação de 2 passagens
- codecs, codificação em duas passagens
- codecs, codificação de 2 passagens
- codificação de dois passos, sobre
- 2-passar codificação, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005278"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="5bc3a-109">Codificação de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="5bc3a-109">Two-Pass Encoding</span></span>

<span data-ttu-id="5bc3a-110">Codificação de duas passagens é um método de codificação disponível com alguns codecs, como o codec do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="5bc3a-111">Quando você usa codificação de duas passagens, o codec processa todos os exemplos para o fluxo duas vezes.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="5bc3a-112">Na primeira passagem, o codec reúne informações sobre o conteúdo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="5bc3a-113">Na segunda passagem, o codec usa as informações coletadas na primeira passagem para otimizar o processo de codificação para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="5bc3a-114">No modo de codificação de taxa de bits constante, os arquivos codificados em duas passagens geralmente são mais eficientes do que os arquivos codificados em uma única passagem.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="5bc3a-115">A taxa de bits baseada em qualidade, que é uma passagem, produz uma qualidade mais consistente do que a VBR baseada em taxa de bits, que é de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="5bc3a-116">Não é possível usar codificação de duas passagens em transmissões ao vivo.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bc3a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bc3a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc3a-118">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="5bc3a-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="5bc3a-119">**Usando a codificação Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="5bc3a-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




