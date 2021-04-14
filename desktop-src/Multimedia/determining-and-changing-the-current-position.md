---
title: Determinando e alterando a posição atual
description: Determinando e alterando a posição atual
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Macro MCIWndGetStart
- Macro MCIWndGetEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453635"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="2ebaf-105">Determinando e alterando a posição atual</span><span class="sxs-lookup"><span data-stu-id="2ebaf-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="2ebaf-106">Quando um arquivo ou dispositivo está associado a uma janela MCIWnd, a posição de reprodução é inicialmente definida no início do conteúdo, independentemente do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="2ebaf-107">Durante a reprodução, a posição da reprodução se move linearmente por meio do conteúdo e, se a reprodução não for interrompida, chegará eventualmente ao final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="2ebaf-108">Se ocorrer uma interrupção, a posição de reprodução atual será o local em que a reprodução foi interrompida ou pausada.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="2ebaf-109">Você pode recuperar os locais para o início e o fim do conteúdo usando as macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="2ebaf-110">Você pode determinar o comprimento do conteúdo subtraindo o valor retornado por **MCIWndGetStart** do valor retornado por **MCIWndGetEnd** ou usando a macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="2ebaf-111">Você pode recuperar a posição de reprodução atual usando a macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou pode recuperar a posição de reprodução como uma cadeia de caracteres terminada em nulo usando a macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="2ebaf-112">Para alterar a posição de reprodução atual, use as macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)e [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="2ebaf-113">Você pode mover a posição de reprodução para o início do conteúdo usando **MCIWndHome** ou para o final do conteúdo usando **MCIWndEnd**.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="2ebaf-114">Use **MCIWndSeek** para mover a posição de reprodução para qualquer local no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="2ebaf-115">Você também pode percorrer o conteúdo usando a macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="2ebaf-116">A partir da posição de reprodução atual, essa macro move a posição de reprodução para frente ou para trás por um incremento especificado.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="2ebaf-117">As unidades usadas para especificar a posição variam entre os diferentes tipos de mídia e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="2ebaf-118">Por exemplo, a posição de reprodução para arquivos AVI usados pelo dispositivo MCIAVI é medida em quadros; a posição de reprodução para áudio de CD, wave-áudio e arquivos MIDI é medida em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="2ebaf-119">Dispositivos para outros tipos de mídia e dispositivos de terceiros podem usar outras unidades.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="2ebaf-120">Para obter informações sobre como determinar essas unidades, consulte [aprimoramentos de reprodução](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="2ebaf-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




