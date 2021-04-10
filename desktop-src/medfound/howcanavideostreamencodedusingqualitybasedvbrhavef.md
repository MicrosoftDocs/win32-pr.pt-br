---
description: Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165450"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="68dad-103">Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?</span><span class="sxs-lookup"><span data-stu-id="68dad-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="68dad-104">A contagem de quadros de um fluxo codificado pode ser menor do que a contagem de quadros do original por um destes dois motivos: quadros duplicados e quadros ignorados.</span><span class="sxs-lookup"><span data-stu-id="68dad-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="68dad-105">Normalmente, o codificador não produz quadros que são duplicatas exatas do quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="68dad-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="68dad-106">Se você precisar ter um exemplo para cada quadro (isso é exigido por alguns contêineres, por exemplo), poderá configurar o codificador para produzir quadros "fictícios" definindo a propriedade [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="68dad-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="68dad-107">O codificador descarta os quadros quando não é possível codificar todos os quadros sem estourar o buffer.</span><span class="sxs-lookup"><span data-stu-id="68dad-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="68dad-108">Os quadros descartados afetam a qualidade do fluxo, não há quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="68dad-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="68dad-109">Você pode obter estatísticas de quadro do codificador para determinar se os quadros foram descartados.</span><span class="sxs-lookup"><span data-stu-id="68dad-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="68dad-110">Para obter mais informações, consulte [obtendo estatísticas de codificação](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="68dad-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="68dad-111">Normalmente, os fluxos de VBR com base em qualidade terão menos quadros do que o original se houver quadros duplicados (porque a taxa de bits não é restrita).</span><span class="sxs-lookup"><span data-stu-id="68dad-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68dad-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68dad-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68dad-113">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="68dad-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



