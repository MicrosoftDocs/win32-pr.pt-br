---
description: Segmentos de envelope
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmentos de envelope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500446"
---
# <a name="envelope-segments"></a><span data-ttu-id="2199f-103">Segmentos de envelope</span><span class="sxs-lookup"><span data-stu-id="2199f-103">Envelope Segments</span></span>

<span data-ttu-id="2199f-104">Uma curva de parâmetro consiste em um ou mais segmentos de envelope, definidos usando a estrutura de [**\_ \_ segmento de envelope MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) .</span><span class="sxs-lookup"><span data-stu-id="2199f-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="2199f-105">Essa estrutura contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="2199f-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="2199f-106">Os horários de início e término.</span><span class="sxs-lookup"><span data-stu-id="2199f-106">The start and end times.</span></span>
-   <span data-ttu-id="2199f-107">Os valores inicial e final.</span><span class="sxs-lookup"><span data-stu-id="2199f-107">The starting and ending values.</span></span>
-   <span data-ttu-id="2199f-108">O tipo de curva (linear, quadrado e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="2199f-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="2199f-109">Sinalizadores opcionais, descritos em breve.</span><span class="sxs-lookup"><span data-stu-id="2199f-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="2199f-110">O cliente adiciona segmentos de envelope a um parâmetro chamando o método [**IMediaParams:: addenvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) e passando uma matriz de estruturas **de \_ \_ segmento de envelope MP** .</span><span class="sxs-lookup"><span data-stu-id="2199f-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="2199f-111">O cliente deve classificar os segmentos em ordem de tempo crescente antes de chamar o método.</span><span class="sxs-lookup"><span data-stu-id="2199f-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="2199f-112">À medida que o DMO processa dados, você pode imaginar o parâmetro viajando em cada segmento de envelope, como um carro conduzindo uma série de Hills.</span><span class="sxs-lookup"><span data-stu-id="2199f-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="2199f-113">O método [**IMediaParams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) retorna o valor mais recente.</span><span class="sxs-lookup"><span data-stu-id="2199f-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="2199f-114">Dois segmentos adjacentes podem ter uma lacuna entre eles.</span><span class="sxs-lookup"><span data-stu-id="2199f-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="2199f-115">Durante as lacunas, o parâmetro retém seu valor anterior, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2199f-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="2199f-116">Antes do primeiro segmento, o valor é o valor neutro.</span><span class="sxs-lookup"><span data-stu-id="2199f-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="2199f-117">Entre segmentos, o valor é o valor final do segmento anterior.</span><span class="sxs-lookup"><span data-stu-id="2199f-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="2199f-118">Após o último segmento, o valor permanece no valor final desse segmento.</span><span class="sxs-lookup"><span data-stu-id="2199f-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="2199f-119">Se o cliente liberar o DMO, o valor será revertido para o valor neutro.</span><span class="sxs-lookup"><span data-stu-id="2199f-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="2199f-120">Você pode alterar um segmento definindo qualquer um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="2199f-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="2199f-121">ENVLP do MPF \_ \_ begin \_ CURRENTVAL.</span><span class="sxs-lookup"><span data-stu-id="2199f-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="2199f-122">O DMO usa o valor mais recente do parâmetro como o valor inicial para o segmento.</span><span class="sxs-lookup"><span data-stu-id="2199f-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="2199f-123">Esse pode ser o valor neutro ou o valor final do segmento anterior.</span><span class="sxs-lookup"><span data-stu-id="2199f-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="2199f-124">O DMO ignora o membro **valStart** da estrutura do **\_ \_ segmento de envelope do MP** .</span><span class="sxs-lookup"><span data-stu-id="2199f-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="2199f-125">ENVLP do MPF \_ \_ begin \_ NEUTRALVAL.</span><span class="sxs-lookup"><span data-stu-id="2199f-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="2199f-126">O DMO usa o valor neutro do parâmetro como o valor inicial para o segmento.</span><span class="sxs-lookup"><span data-stu-id="2199f-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="2199f-127">Ele ignora **valStart**.</span><span class="sxs-lookup"><span data-stu-id="2199f-127">It ignores **valStart**.</span></span>

<span data-ttu-id="2199f-128">Você pode considerar esses sinalizadores como captar o ponto inicial do segmento e movê-lo para cima ou para baixo, enquanto o valor final permanece fixo.</span><span class="sxs-lookup"><span data-stu-id="2199f-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="2199f-129">O segmento será "alongar" de acordo.</span><span class="sxs-lookup"><span data-stu-id="2199f-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2199f-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2199f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2199f-131">Parâmetros de mídia</span><span class="sxs-lookup"><span data-stu-id="2199f-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



