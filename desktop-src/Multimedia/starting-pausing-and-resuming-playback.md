---
title: Iniciando, pausando e retomando a reprodução
description: Iniciando, pausando e retomando a reprodução
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Macro MCIWndPlay
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160441"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="2baad-106">Iniciando, pausando e retomando a reprodução</span><span class="sxs-lookup"><span data-stu-id="2baad-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="2baad-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) é a macro de reprodução mais geral.</span><span class="sxs-lookup"><span data-stu-id="2baad-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="2baad-108">Essa macro permite que você reproduza um arquivo ou dispositivo da posição de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="2baad-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="2baad-109">A reprodução continua até o final do conteúdo, a menos que seja interrompida.</span><span class="sxs-lookup"><span data-stu-id="2baad-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="2baad-110">Você pode interromper temporariamente um dispositivo que está sendo executado usando a macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="2baad-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="2baad-111">Para retomar a reprodução da posição pausada, use a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="2baad-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="2baad-112">Alguns dispositivos não dão suporte aos comandos Pause e resume.</span><span class="sxs-lookup"><span data-stu-id="2baad-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="2baad-113">Esses dispositivos geralmente mapeiam **MCIWndPause** para a macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , que interrompe a reprodução ou a gravação.</span><span class="sxs-lookup"><span data-stu-id="2baad-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="2baad-114">Você pode reiniciar um dispositivo que não dá suporte a Pause ou resume usando **MCIWndPlay**, que inicia a reprodução a partir da posição de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="2baad-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




