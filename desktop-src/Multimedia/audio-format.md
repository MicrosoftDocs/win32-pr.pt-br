---
title: Formato de áudio
description: Formato de áudio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT mensagem
- macro capGetAudioFormat
- macro capGetAudioFormatSize
- WM_CAP_SET_AUDIOFORMAT mensagem
- macro capSetAudioFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823694"
---
# <a name="audio-format"></a><span data-ttu-id="7ee3a-108">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="7ee3a-108">Audio Format</span></span>

<span data-ttu-id="7ee3a-109">Você pode recuperar o formato de captura atual para dados de áudio ou o tamanho da estrutura de formato de áudio enviando a mensagem do [**WM \_ Cap \_ Get \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (ou as macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7ee3a-109">You can retrieve the current capture format for audio data or the size of the audio format structure by sending the [**WM\_CAP\_GET\_AUDIOFORMAT**](wm-cap-get-audioformat.md) message (or the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros) to a capture window.</span></span> <span data-ttu-id="7ee3a-110">O formato de captura de áudio padrão é mono, 8 bits, 11 kHz PCM (modulação de código de pulso).</span><span class="sxs-lookup"><span data-stu-id="7ee3a-110">The default audio capture format is mono, 8-bit, 11 kHz PCM (Pulse Code Modulation).</span></span> <span data-ttu-id="7ee3a-111">Quando você recupera o formato usando o WM \_ Cap \_ Get \_ AUDIOFORMAT, sempre use a estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="7ee3a-111">When you retrieve the format by using WM\_CAP\_GET\_AUDIOFORMAT, always use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure.</span></span>

<span data-ttu-id="7ee3a-112">Você pode definir o formato de captura para dados de áudio enviando a mensagem do [**AUDIOFORMAT do WM \_ Cap \_ set \_**](wm-cap-set-audioformat.md) (ou a macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7ee3a-112">You can set the capture format for audio data by sending the [**WM\_CAP\_SET\_AUDIOFORMAT**](wm-cap-set-audioformat.md) message (or the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro) to a capture window.</span></span> <span data-ttu-id="7ee3a-113">Ao definir o formato de áudio, você pode passar um ponteiro para uma estrutura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX** ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , dependendo do formato de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="7ee3a-113">When setting the audio format, you can pass a pointer to a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX**, or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure, depending on the specified audio format.</span></span>

 

 