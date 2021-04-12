---
title: Revertendo a reprodução
description: Revertendo a reprodução
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Macro MCIWndPlayReverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363965"
---
# <a name="reversing-playback"></a><span data-ttu-id="c445d-104">Revertendo a reprodução</span><span class="sxs-lookup"><span data-stu-id="c445d-104">Reversing Playback</span></span>

<span data-ttu-id="c445d-105">Alguns dispositivos dão suporte à reprodução na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="c445d-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="c445d-106">Você pode reproduzir o conteúdo desse dispositivo na direção inversa usando a macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="c445d-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="c445d-107">Essa macro define o escopo de reprodução da posição de reprodução atual para o início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c445d-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="c445d-108">O dispositivo de vídeo digital, MCIAVI. DRV, pode reproduzir para trás.</span><span class="sxs-lookup"><span data-stu-id="c445d-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="c445d-109">Dispositivos que não podem reproduzir, como áudio de CD, podem emitir uma mensagem de erro quando **MCIWndPlayReverse** é invocado.</span><span class="sxs-lookup"><span data-stu-id="c445d-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




