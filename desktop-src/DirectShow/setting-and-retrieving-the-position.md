---
description: Configurando e recuperando a posição
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Configurando e recuperando a posição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645627"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="8cb98-103">Configurando e recuperando a posição</span><span class="sxs-lookup"><span data-stu-id="8cb98-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="8cb98-104">O grafo de filtro mantém dois valores de posição, posição atual e posição de parada.</span><span class="sxs-lookup"><span data-stu-id="8cb98-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="8cb98-105">Eles são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8cb98-105">These are defined as follows:</span></span>

-   <span data-ttu-id="8cb98-106">Quando o grafo está em execução, a posição atual é a posição de reprodução atual, relativa ao início da origem.</span><span class="sxs-lookup"><span data-stu-id="8cb98-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="8cb98-107">Quando o grafo é interrompido ou pausado, a posição atual é o ponto em que o streaming começará no próximo comando de execução.</span><span class="sxs-lookup"><span data-stu-id="8cb98-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="8cb98-108">A posição de parada é o ponto em que o fluxo será encerrado.</span><span class="sxs-lookup"><span data-stu-id="8cb98-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="8cb98-109">Quando o grafo atinge a posição de parada, nenhum dado é transmitido e o Gerenciador de gráfico de filtro posta um evento de [**\_ conclusão de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb98-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="8cb98-110">(No entanto, o grafo não muda automaticamente para um estado parado.</span><span class="sxs-lookup"><span data-stu-id="8cb98-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="8cb98-111">Para obter mais informações, consulte [respondendo a eventos](responding-to-events.md).)</span><span class="sxs-lookup"><span data-stu-id="8cb98-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="8cb98-112">Para recuperar esses valores, chame o método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="8cb98-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="8cb98-113">Os valores retornados são sempre relativos à origem da mídia original.</span><span class="sxs-lookup"><span data-stu-id="8cb98-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="8cb98-114">Por padrão, os valores estão em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="8cb98-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="8cb98-115">Em alguns casos, você pode alterar as unidades de tempo; para obter mais informações, consulte [formatos de hora para comandos de busca](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="8cb98-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="8cb98-116">Para buscar uma nova posição ou definir uma nova posição de parada, chame o método [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="8cb98-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="8cb98-117">Um segundo é de 10 milhões unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="8cb98-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="8cb98-118">Para sua conveniência, o exemplo define esse valor como um \_ segundo.</span><span class="sxs-lookup"><span data-stu-id="8cb98-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="8cb98-119">Se você estiver usando a biblioteca de classe base do DirectShow, as unidades de constante têm o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="8cb98-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="8cb98-120">O parâmetro *rtNow* especifica a nova posição atual.</span><span class="sxs-lookup"><span data-stu-id="8cb98-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="8cb98-121">O segundo parâmetro é um sinalizador que define como interpretar *rtNow*.</span><span class="sxs-lookup"><span data-stu-id="8cb98-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="8cb98-122">Neste exemplo, o sinalizador AM \_ buscando \_ AbsolutePositioning indica que *rtNow* especifica uma posição absoluta na origem.</span><span class="sxs-lookup"><span data-stu-id="8cb98-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="8cb98-123">Portanto, o grafo de filtro vai procurar uma posição de dois segundos desde o início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="8cb98-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="8cb98-124">O parâmetro *rtStop* fornece a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="8cb98-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="8cb98-125">O último parâmetro especifica que *rtStop* também é uma posição absoluta.</span><span class="sxs-lookup"><span data-stu-id="8cb98-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="8cb98-126">Para especificar uma posição relativa ao valor da posição anterior, use o \_ sinalizador am buscando \_ RelativePositioning.</span><span class="sxs-lookup"><span data-stu-id="8cb98-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="8cb98-127">Para deixar um dos valores de posição inalterados, use o \_ sinalizador am buscando sem \_ posicionamento.</span><span class="sxs-lookup"><span data-stu-id="8cb98-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="8cb98-128">O parâmetro time correspondente pode ser **nulo** nesse caso.</span><span class="sxs-lookup"><span data-stu-id="8cb98-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="8cb98-129">O exemplo a seguir busca avançar por 10 segundos, mas deixa a posição de parada inalterada:</span><span class="sxs-lookup"><span data-stu-id="8cb98-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="8cb98-130">Se o grafo de filtro for interrompido, o processador de vídeo não atualizará a imagem após uma operação de busca.</span><span class="sxs-lookup"><span data-stu-id="8cb98-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="8cb98-131">Para o usuário, ele aparecerá como se a busca não tivesse acontecido.</span><span class="sxs-lookup"><span data-stu-id="8cb98-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="8cb98-132">Para atualizar a imagem, pause o grafo após a operação de busca.</span><span class="sxs-lookup"><span data-stu-id="8cb98-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="8cb98-133">Pausar o grafo aponta um novo quadro de vídeo para o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cb98-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="8cb98-134">Você pode usar o método [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , que pausa o grafo e o interrompe.</span><span class="sxs-lookup"><span data-stu-id="8cb98-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



