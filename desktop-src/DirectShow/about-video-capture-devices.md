---
description: Sobre dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Sobre dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645868"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="faa55-103">Sobre dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="faa55-103">About Video Capture Devices</span></span>

<span data-ttu-id="faa55-104">A maioria dos novos dispositivos de captura de vídeo usam drivers de Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="faa55-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="faa55-105">Na arquitetura WDM, a Microsoft fornece um conjunto de drivers independentes de hardware, chamados de drivers de classe, e o fornecedor de hardware fornece minidrivers específicas de hardware.</span><span class="sxs-lookup"><span data-stu-id="faa55-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="faa55-106">Um minidriver implementa qualquer função que seja específica para o dispositivo; para a maioria das funções, o minidriver chama o Microsoft Class Driver.</span><span class="sxs-lookup"><span data-stu-id="faa55-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="faa55-107">Em um grafo de filtro do DirectShow, qualquer dispositivo de captura WDM aparece como o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="faa55-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="faa55-108">O filtro de captura de vídeo WDM se configura com base nas características do driver.</span><span class="sxs-lookup"><span data-stu-id="faa55-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="faa55-109">Ele aparece sob um nome fornecido pelo driver — você não verá um filtro chamado "filtro de captura de vídeo WDM" em qualquer lugar no grafo.</span><span class="sxs-lookup"><span data-stu-id="faa55-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="faa55-110">Alguns dispositivos de captura mais antigos ainda usam drivers de vídeo para Windows (VFW).</span><span class="sxs-lookup"><span data-stu-id="faa55-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="faa55-111">Embora esses drivers agora sejam obsoletos, eles têm suporte no DirectShow por meio do filtro de [captura VFW](vfw-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="faa55-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faa55-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="faa55-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa55-113">Sobre a captura de vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="faa55-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



