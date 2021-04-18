---
title: Armazenando conteúdo em buffer
description: Armazenando conteúdo em buffer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- SDK do Windows Media Format, armazenar em buffer o conteúdo
- armazenando conteúdo em buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814087"
---
# <a name="buffering-content"></a><span data-ttu-id="4416d-105">Armazenando conteúdo em buffer</span><span class="sxs-lookup"><span data-stu-id="4416d-105">Buffering Content</span></span>

<span data-ttu-id="4416d-106">Quando o objeto do leitor abre um arquivo de streaming, ele determina o tamanho do buffer com base nas configurações no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4416d-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="4416d-107">Você pode considerar o buffer como um Bucket com um orifício na parte inferior que vaza em uma taxa constante.</span><span class="sxs-lookup"><span data-stu-id="4416d-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="4416d-108">Desde que a taxa na qual o Bucket é preenchido não seja, em média, maior do que a taxa na qual ele está vazando, o Bucket nunca será estourado.</span><span class="sxs-lookup"><span data-stu-id="4416d-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="4416d-109">A taxa na qual os vazamentos de Bucket imaginários é a taxa de bits do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4416d-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="4416d-110">A taxa na qual o Bucket é preenchido é a taxa de bits de streaming real.</span><span class="sxs-lookup"><span data-stu-id="4416d-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="4416d-111">Os dados em um fluxo compactado variam de acordo com o tamanho de amostra para amostra, dependendo da quantidade de compactação obtida.</span><span class="sxs-lookup"><span data-stu-id="4416d-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="4416d-112">Portanto, embora a taxa de bits do fluxo seja definida no perfil, ela representa a taxa média de bits, não uma constante.</span><span class="sxs-lookup"><span data-stu-id="4416d-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="4416d-113">A outra configuração de fluxo importante para o processo de buffer é a janela buffer.</span><span class="sxs-lookup"><span data-stu-id="4416d-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="4416d-114">A janela buffer é medida em tempo e especifica a quantidade de conteúdo que pode ser armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="4416d-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="4416d-115">A capacidade do Bucket imaginário pode ser encontrada usando a janela buffer.</span><span class="sxs-lookup"><span data-stu-id="4416d-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="4416d-116">Por exemplo, se você tiver um fluxo com uma taxa de bits de 32 kbps e uma janela de buffer de 3 segundos, o buffer será dimensionado para conter 3 segundos de conteúdo de 32 kbps ou 12.000 bytes (32.000 bits por segundo x 3 segundos/8 bits por byte).</span><span class="sxs-lookup"><span data-stu-id="4416d-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="4416d-117">O codec limita a variação entre a taxa de bits de streaming real de amostras codificadas para que, em um período de tempo igual à janela de buffer, a taxa de bits média não seja maior do que a taxa de bits do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4416d-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="4416d-118">Normalmente, você define a taxa de bits e a janela de buffer para um fluxo em um perfil, e o gravador lida com o restante.</span><span class="sxs-lookup"><span data-stu-id="4416d-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="4416d-119">No entanto, ao passar amostras compactadas para o leitor, você deve garantir que os valores corretos sejam transferidos para o novo arquivo, definindo a taxa de bits e a janela de buffer para o fluxo no perfil de destino para os valores do fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="4416d-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4416d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4416d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4416d-121">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="4416d-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="4416d-122">**Amostras de mídia**</span><span class="sxs-lookup"><span data-stu-id="4416d-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="4416d-123">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="4416d-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




