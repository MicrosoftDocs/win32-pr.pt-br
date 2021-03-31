---
title: Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários
description: Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- fluxos, taxas de bits
- codecs, calculando taxas de bits para fluxos arbitrários
- taxas de bits, calculando para fluxos arbitrários
- fluxos, calculando taxas de bits para fluxos arbitrários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004944"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="cfae2-107">Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários</span><span class="sxs-lookup"><span data-stu-id="cfae2-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="cfae2-108">Calcular a taxa de bits e a janela de buffer adequadas para um tipo de fluxo arbitrário não é uma ciência exata.</span><span class="sxs-lookup"><span data-stu-id="cfae2-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="cfae2-109">Uma abordagem simples é definir a taxa de bits para corresponder ao tamanho do fluxo dividido por seu comprimento, em segundos.</span><span class="sxs-lookup"><span data-stu-id="cfae2-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="cfae2-110">Por exemplo, um fluxo contendo um total de 68000 bits com duração de 20 segundos pode ter uma taxa de bits de 3400 bits por segundo (68000 bits/20 segundos = 3400 bits por segundo).</span><span class="sxs-lookup"><span data-stu-id="cfae2-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="cfae2-111">O problema com essa técnica simples de atribuição de taxa de bits é que ela não leva em conta a distribuição de dados dentro do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfae2-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="cfae2-112">Muitos fluxos arbitrários contêm grandes quantidades de dados em intervalos ao longo da linha do tempo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cfae2-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="cfae2-113">Fluxos de imagem, por exemplo, têm amostras que são muito grandes, mas geralmente têm um espaçamento de vários segundos de distância.</span><span class="sxs-lookup"><span data-stu-id="cfae2-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="cfae2-114">A janela buffer deve ser definida para garantir que o buffer não irá exceder.</span><span class="sxs-lookup"><span data-stu-id="cfae2-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="cfae2-115">Para verificar a janela de buffer, multiplique a taxa de bits (bits por segundo) pela janela de buffer (em segundos) e divida por 1000 para obter o tamanho, em bits, do buffer para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfae2-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="cfae2-116">Em seguida, certifique-se de que o tamanho do buffer seja grande o suficiente para conter qualquer combinação de amostras no fluxo que seja menor do que a janela de buffer, além do tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="cfae2-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="cfae2-117">Em caso de dúvida, defina os dois valores um pouco mais alto do que você imagina que precisa deles.</span><span class="sxs-lookup"><span data-stu-id="cfae2-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfae2-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cfae2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfae2-119">**Armazenando conteúdo em buffer**</span><span class="sxs-lookup"><span data-stu-id="cfae2-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="cfae2-120">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="cfae2-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




