---
description: Sobre o controle de taxa
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Sobre o controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772945"
---
# <a name="about-rate-control"></a><span data-ttu-id="3e8d8-103">Sobre o controle de taxa</span><span class="sxs-lookup"><span data-stu-id="3e8d8-103">About Rate Control</span></span>

<span data-ttu-id="3e8d8-104">No Media Foundation, a *taxa de reprodução* é expressa como a taxa da taxa de reprodução atual para a taxa de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="3e8d8-105">Por exemplo, uma taxa de 2,0 é duas vezes a velocidade normal e 0,5 é a metade da velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="3e8d8-106">Valores negativos indicam reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="3e8d8-107">Uma taxa de reprodução de-2,0 é reproduzida por meio do fluxo em duas vezes a velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="3e8d8-108">Uma taxa de zero faz com que um quadro seja renderizado; Depois disso, o relógio de apresentação não avança.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="3e8d8-109">Para obter outro quadro com a taxa de zero, o aplicativo deve procurar uma nova posição.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="3e8d8-110">Os aplicativos usam as seguintes interfaces para controlar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="3e8d8-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="3e8d8-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="3e8d8-112">Usado para descobrir as taxas de reprodução mais rápidas e mais lentas possíveis.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="3e8d8-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="3e8d8-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="3e8d8-114">Usado para alterar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-114">Used to change the playback rate.</span></span>

<span data-ttu-id="3e8d8-115">Para obter essas duas interfaces, chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="3e8d8-116">O identificador de serviço é o serviço de controle de taxa de MF \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3e8d8-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="3e8d8-117">Usando o serviço de controle de taxa, um aplicativo pode implementar a reprodução rápida e inversa.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="3e8d8-118">Finamento</span><span class="sxs-lookup"><span data-stu-id="3e8d8-118">Thinning</span></span>

<span data-ttu-id="3e8d8-119">A *fina* é qualquer processo que reduz o número de amostras em um fluxo, a fim de reduzir a taxa geral de bits.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="3e8d8-120">Para vídeo, o estreitamento geralmente é feito removendo os quadros Delta e entregando apenas os quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="3e8d8-121">Geralmente, o pipeline pode dar suporte a taxas de reprodução mais rápidas usando reprodução fina, porque a taxa de dados é menor porque os quadros Delta não são decodificados.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="3e8d8-122">A fina não altera os carimbos de data/hora ou as durações nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="3e8d8-123">Por exemplo, se a taxa nominal do fluxo de vídeo for de 25 quadros por segundo, a duração de cada quadro ainda será marcada como 40 milissegundos, mesmo que a origem da mídia esteja removendo todos os quadros Delta.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="3e8d8-124">Isso significa que haverá uma lacuna de tempo entre o final de um quadro e o início do próximo.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="3e8d8-125">Anulação</span><span class="sxs-lookup"><span data-stu-id="3e8d8-125">Scrubbing</span></span>

<span data-ttu-id="3e8d8-126">A *depuração* é o processo de busca instantânea de pontos específicos no fluxo interagindo com uma barra de rolagem, linha do tempo ou outra representação visual do tempo.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="3e8d8-127">O termo vem da era dos players de fita de rolo a rolo quando um rolo para frente e para trás para localizar uma seção era como depurar o cabeçote de reprodução com a fita.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="3e8d8-128">A depuração é implementada no Media Foundation definindo a taxa de reprodução como zero.</span><span class="sxs-lookup"><span data-stu-id="3e8d8-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="3e8d8-129">Para obter mais informações, consulte [como executar a depuração](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="3e8d8-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e8d8-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8d8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e8d8-131">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="3e8d8-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="3e8d8-132">Busca, avanço rápido e reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="3e8d8-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="3e8d8-133">Interfaces de serviço</span><span class="sxs-lookup"><span data-stu-id="3e8d8-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



