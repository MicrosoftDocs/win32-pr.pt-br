---
description: Controle de qualidade padrão
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Controle de qualidade padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009885"
---
# <a name="default-quality-control"></a><span data-ttu-id="0e940-103">Controle de qualidade padrão</span><span class="sxs-lookup"><span data-stu-id="0e940-103">Default Quality Control</span></span>

<span data-ttu-id="0e940-104">As [classes base do DirectShow](directshow-base-classes.md) implementam alguns comportamentos padrão para o controle de qualidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e940-104">The [DirectShow Base Classes](directshow-base-classes.md) implement some default behaviors for video quality control.</span></span>

<span data-ttu-id="0e940-105">As mensagens de qualidade começam no renderizador.</span><span class="sxs-lookup"><span data-stu-id="0e940-105">Quality messages start at the renderer.</span></span> <span data-ttu-id="0e940-106">A classe base para renderizadores de vídeo é [**CBaseVideoRenderer**](cbasevideorenderer.md), que tem o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="0e940-106">The base class for video renderers is [**CBaseVideoRenderer**](cbasevideorenderer.md), which has the following behavior:</span></span>

1.  <span data-ttu-id="0e940-107">Quando o renderizador de vídeo recebe um exemplo, ele compara o carimbo de data/hora no exemplo com o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="0e940-107">When the video renderer receives a sample, it compares the time stamp on the sample with the current reference time.</span></span>
2.  <span data-ttu-id="0e940-108">O processador de vídeo gera uma mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="0e940-108">The video renderer generates a quality message.</span></span> <span data-ttu-id="0e940-109">Na classe base, o membro de **proporção** da mensagem de qualidade é limitado a um intervalo de 500 (50%) a 2000 (200%).</span><span class="sxs-lookup"><span data-stu-id="0e940-109">In the base class, the **Proportion** member of the quality message is limited to a range of 500 (50%) to 2000 (200%).</span></span> <span data-ttu-id="0e940-110">Os valores fora desse intervalo podem resultar em alterações de qualidade abrupta.</span><span class="sxs-lookup"><span data-stu-id="0e940-110">Values outside this range could result in abrupt quality changes.</span></span>
3.  <span data-ttu-id="0e940-111">Por padrão, o processador de vídeo envia a mensagem de qualidade para o pino de saída upstream (o PIN conectado ao seu PIN de entrada).</span><span class="sxs-lookup"><span data-stu-id="0e940-111">By default, the video renderer sends the quality message to the upstream output pin (the pin connected to its input pin).</span></span> <span data-ttu-id="0e940-112">Os aplicativos podem substituir esse comportamento chamando o método **SetSink** .</span><span class="sxs-lookup"><span data-stu-id="0e940-112">Applications can override this behavior by calling the **SetSink** method.</span></span>

<span data-ttu-id="0e940-113">O que acontece em seguida depende do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="0e940-113">What happens next depends on the upstream filter.</span></span> <span data-ttu-id="0e940-114">Normalmente, esse é um filtro de transformação.</span><span class="sxs-lookup"><span data-stu-id="0e940-114">Typically, this is a transform filter.</span></span> <span data-ttu-id="0e940-115">A classe base para filtros de transformação é [**CTransformFilter**](ctransformfilter.md), que usa as classes [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) para implementar Pins de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="0e940-115">The base class for transform filters is [**CTransformFilter**](ctransformfilter.md), which uses the [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) classes to implement input and output pins.</span></span> <span data-ttu-id="0e940-116">Juntas, essas classes têm o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="0e940-116">Together, these classes have the following behavior:</span></span>

1.  <span data-ttu-id="0e940-117">O método [**CTransformOutputPin:: Notify**](ctransformoutputpin-notify.md) chama [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md), um método particular na classe base de filtro.</span><span class="sxs-lookup"><span data-stu-id="0e940-117">The [**CTransformOutputPin::Notify**](ctransformoutputpin-notify.md) method calls [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md), a private method on the filter base class.</span></span>
2.  <span data-ttu-id="0e940-118">Os filtros derivados podem substituir **AlterQuality** para manipular a mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="0e940-118">Derived filters can override **AlterQuality** to handle the quality message.</span></span> <span data-ttu-id="0e940-119">Por padrão, o **AlterQuality** ignora a mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="0e940-119">By default, **AlterQuality** ignores the quality message.</span></span>
3.  <span data-ttu-id="0e940-120">Se **AlterQuality** não tratar a mensagem de qualidade, o pino de saída chamará [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md), um método particular no PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="0e940-120">If **AlterQuality** does not handle the quality message, the output pin calls [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md), a private method on the filter's input pin.</span></span>
4.  <span data-ttu-id="0e940-121">**PassNotify** passa a mensagem de qualidade para o local apropriado — o próximo pino de saída upstream ou um Gerenciador de qualidade personalizado.</span><span class="sxs-lookup"><span data-stu-id="0e940-121">**PassNotify** passes the quality message to the appropriate place—the next upstream output pin, or a custom quality manager.</span></span>

<span data-ttu-id="0e940-122">Supondo que nenhum filtro de transformação manipule a mensagem de qualidade, a mensagem eventualmente atinge o pino de saída no filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="0e940-122">Assuming that no transform filter handles the quality message, the message eventually reaches the output pin on the source filter.</span></span> <span data-ttu-id="0e940-123">Nas classes base, [**CBasePin:: Notify**](cbasepin-notify.md) retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="0e940-123">In the base classes, [**CBasePin::Notify**](cbasepin-notify.md) returns E\_NOTIMPL.</span></span> <span data-ttu-id="0e940-124">Como um filtro de origem específico manipula as mensagens de qualidade depende da natureza da origem.</span><span class="sxs-lookup"><span data-stu-id="0e940-124">How a particular source filter handles quality messages depends on the nature of the source.</span></span> <span data-ttu-id="0e940-125">Algumas fontes, como a captura de vídeo ao vivo, não podem executar um controle de qualidade significativo.</span><span class="sxs-lookup"><span data-stu-id="0e940-125">Some sources, such as live video capture, cannot perform meaningful quality control.</span></span> <span data-ttu-id="0e940-126">Outras fontes podem ajustar a taxa na qual elas fornecem exemplos.</span><span class="sxs-lookup"><span data-stu-id="0e940-126">Other sources can adjust the rate at which they deliver samples.</span></span>

<span data-ttu-id="0e940-127">O diagrama a seguir ilustra o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="0e940-127">The following diagram illustrates the default behavior.</span></span>

![controle de qualidade nas classes base](images/quality-control.png)

<span data-ttu-id="0e940-129">O processador de vídeo base implementa **IQualityControl:: Notify**, o que significa que você pode passar mensagens de qualidade para o próprio processador.</span><span class="sxs-lookup"><span data-stu-id="0e940-129">The base video renderer implements **IQualityControl::Notify**, which means you can pass quality messages to the renderer itself.</span></span> <span data-ttu-id="0e940-130">Se você definir o membro de **proporção** como um valor menor que 1000, o processador de vídeo inserirá um período de espera entre cada quadro que ele renderiza, na lentidão do processador.</span><span class="sxs-lookup"><span data-stu-id="0e940-130">If you set the **Proportion** member to a value less than 1000, the video renderer inserts a wait period between each frame that it renders, in effect slowing down the renderer.</span></span> <span data-ttu-id="0e940-131">(Você pode fazer isso para reduzir o uso do sistema, por exemplo.) Para obter mais informações, consulte [**CBaseVideoRenderer:: ThrottleWait**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="0e940-131">(You might do this to reduce system usage, for example.) For more information, see [**CBaseVideoRenderer::ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span> <span data-ttu-id="0e940-132">Definir o membro de **proporção** como um valor maior que 1000 não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="0e940-132">Setting the **Proportion** member to a value greater than 1000 has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e940-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e940-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e940-134">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="0e940-134">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 



