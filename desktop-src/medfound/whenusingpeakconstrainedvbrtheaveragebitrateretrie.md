---
description: Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico. Como isso é possível?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296617"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="ef31d-104">Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="ef31d-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="ef31d-105">Como isso é possível?</span><span class="sxs-lookup"><span data-stu-id="ef31d-105">How is that possible?</span></span>

<span data-ttu-id="ef31d-106">A relação entre a taxa média de bits e a taxa de bits de pico geralmente é mal compreendida.</span><span class="sxs-lookup"><span data-stu-id="ef31d-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="ef31d-107">A taxa de bits de pico descreve uma restrição de buffer ao longo de um período de tempo especificado pela janela de pico do buffer.</span><span class="sxs-lookup"><span data-stu-id="ef31d-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="ef31d-108">A taxa média de bits para a VBR de duas passagens (irrestrito ou com restrição de pico) é a média de bits por segundo durante a duração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ef31d-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="ef31d-109">Conforme descrito no [modelo de buffer de Bucket vazado](the-leaky-bucket-buffer-model.md), a taxa de bits real usada em um período de tempo igual à janela de buffer pode aproximar duas vezes a taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="ef31d-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="ef31d-110">Isso ocorre porque o buffer, definido como um número de bits igual à taxa de bits, o tempo da janela de buffer (em segundos), está sendo esvaziado a uma taxa constante.</span><span class="sxs-lookup"><span data-stu-id="ef31d-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="ef31d-111">Por exemplo, em um segundo de um fluxo de 56 Kbps, o codificador cria amostras que totalizam 59 KB.</span><span class="sxs-lookup"><span data-stu-id="ef31d-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="ef31d-112">Portanto, 56 KB de dados é removido do buffer nesse segundo, deixando 3 KB no buffer.</span><span class="sxs-lookup"><span data-stu-id="ef31d-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="ef31d-113">Se o fluxo tiver uma janela de buffer de três segundos e, portanto, um tamanho de buffer total de 168 KB, levaria quase 40 segundos para preencher o buffer.</span><span class="sxs-lookup"><span data-stu-id="ef31d-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="ef31d-114">A taxa média de bits para o fluxo (se sua duração for menor do que o tempo necessário para preencher o buffer) for de 59 Kbps, mesmo que a taxa de bits seja definida como 56 Kbps.</span><span class="sxs-lookup"><span data-stu-id="ef31d-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="ef31d-115">O mesmo fenômeno se aplica a restrições de taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="ef31d-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="ef31d-116">Para conteúdo curto, a taxa média de bits computada pelo objeto codec após a codificação ser concluída pode ser maior que a taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="ef31d-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef31d-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef31d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef31d-118">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="ef31d-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



