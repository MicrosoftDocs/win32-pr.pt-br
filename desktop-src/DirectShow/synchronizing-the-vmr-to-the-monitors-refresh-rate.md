---
description: Sincronizando o VMR com a taxa de atualização do monitor
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizando o VMR com a taxa de atualização do monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171698"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="ddaaf-103">Sincronizando o VMR com a taxa de atualização do monitor</span><span class="sxs-lookup"><span data-stu-id="ddaaf-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="ddaaf-104">Em cenários raros, talvez você queira sincronizar precisamente a renderização de vídeo com a taxa de atualização do monitor para que exatamente um novo quadro seja apresentado sempre que o monitor for atualizado.</span><span class="sxs-lookup"><span data-stu-id="ddaaf-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="ddaaf-105">A maneira mais confiável de fazer isso é criar um apresentador de alocador personalizado que usa uma operação de inversão em vez de uma operação blit para gravar os bits de vídeo na superfície primária.</span><span class="sxs-lookup"><span data-stu-id="ddaaf-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="ddaaf-106">"Flip" é chamado cada vez que o monitor é atualizado, portanto, se o fluxo de vídeo não contiver carimbos de data/hora, o VMR renderizará o mais rápido possível para a superfície primária, mas a superfície bloqueará o fluxo até que a operação de inversão seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ddaaf-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="ddaaf-107">Isso significa que, desde que a CPU não seja sobrecarregada, o próximo quadro sempre estará aguardando na superfície principal cada vez que o monitor for atualizado.</span><span class="sxs-lookup"><span data-stu-id="ddaaf-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="ddaaf-108">No entanto, se algum outro processo de uso intensivo de CPU estiver em execução, poderá possivelmente ficar sem o thread de streaming do DirectShow para que ele não possa entregar quadros de vídeo rápido o suficiente para a superfície primária.</span><span class="sxs-lookup"><span data-stu-id="ddaaf-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddaaf-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddaaf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddaaf-110">Modo de reprodução do VMR (alocador personalizado-apresentadores)</span><span class="sxs-lookup"><span data-stu-id="ddaaf-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



