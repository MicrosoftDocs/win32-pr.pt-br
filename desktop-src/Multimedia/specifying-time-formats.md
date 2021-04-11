---
title: Especificando formatos de hora
description: Especificando formatos de hora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Macro MCIWndGetTimeFormat
- Macro MCIWndSetTimeFormat
- Macro MCIWndUseTime
- Macro MCIWndUseFrames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292204"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="3fe9d-107">Especificando formatos de hora</span><span class="sxs-lookup"><span data-stu-id="3fe9d-107">Specifying Time Formats</span></span>

<span data-ttu-id="3fe9d-108">Os tipos de dados de multimídia normalmente podem usar o tempo para identificar posições significativas em seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="3fe9d-109">Formatos de tempo comuns são milissegundos, faixas e quadros; outros formatos de tempo menos comuns, como SMPTE (sociedade de imagem de movimento e engenheiros de televisão) 24, também existem.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="3fe9d-110">A hora é o formato e o sistema de referência para a forma de onda-áudio, MIDI e dados de áudio de CD.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="3fe9d-111">O vídeo dá suporte ao tempo, embora seja registrado como uma sequência de quadros (fluxo) que normalmente é reproduzido em uma velocidade específica.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="3fe9d-112">Várias macros estão disponíveis para o formato de hora de design.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="3fe9d-113">Você pode recuperar o formato de hora atual para um arquivo ou dispositivo usando a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3fe9d-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="3fe9d-114">Você pode alterar o formato de hora atual para qualquer outro formato de hora com suporte de um dispositivo usando a macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3fe9d-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="3fe9d-115">Ou você pode definir o formato de hora como milissegundos ou quadros usando as macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) ou [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .</span><span class="sxs-lookup"><span data-stu-id="3fe9d-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="3fe9d-116">Formatos não contínuos, como trilhas e SMPTE, podem fazer com que a barra de ferramentas se comporte incorretamente.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="3fe9d-117">Para esses formatos de tempo, talvez você queira desativar a barra de ferramentas especificando o \_ estilo de janela MCIWNDF NOPLAYBAR ao criar uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




