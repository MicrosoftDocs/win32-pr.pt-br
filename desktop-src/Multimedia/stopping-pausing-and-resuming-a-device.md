---
title: Parando, pausando e retomando um dispositivo
description: Parando, pausando e retomando um dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP comando
- MCI_PAUSE comando
- MCI_RESUME comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635969"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="ebadd-106">Parando, pausando e retomando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="ebadd-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="ebadd-107">O comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) suspende a reprodução ou a gravação de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebadd-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="ebadd-108">Muitos dispositivos também dão suporte ao comando [**Pause**](pause.md) ([**\_ pausa MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="ebadd-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="ebadd-109">A diferença entre **parar** e **Pausar** depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebadd-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="ebadd-110">Geralmente, **Pause** suspende a operação, mas deixa o dispositivo pronto para retomar a reprodução ou a gravação imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ebadd-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="ebadd-111">Usando o comando [**Play**](play.md) ([**\_ reprodução MCI**](mci-play.md)) ou [**gravar**](record.md) ([**\_ registro MCI**](mci-record.md)) para reiniciar um dispositivo, redefine os locais especificados com os sinalizadores "para" (MCI \_ para) e "de" (MCI \_ de) antes de o dispositivo ser pausado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="ebadd-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="ebadd-112">Sem o sinalizador "from", esses comandos redefinem o local inicial para a posição atual.</span><span class="sxs-lookup"><span data-stu-id="ebadd-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="ebadd-113">Sem o sinalizador "to", eles redefinem o local final para o final da mídia.</span><span class="sxs-lookup"><span data-stu-id="ebadd-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="ebadd-114">Para continuar a reproduzir ou gravar sem redefinir uma posição de parada especificada anteriormente, use o sinalizador "para" do comando **Play** ou **Record** para especificar uma posição final.</span><span class="sxs-lookup"><span data-stu-id="ebadd-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="ebadd-115">Alguns dispositivos dão suporte ao comando [**resume**](resume.md) ([**\_ retomar MCI**](mci-resume.md)) para reiniciar um dispositivo em pausa.</span><span class="sxs-lookup"><span data-stu-id="ebadd-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="ebadd-116">Esse comando não altera os locais "para" e "de" especificados com o comando **Play** ou **Record** que precede o comando [**Pause**](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="ebadd-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




