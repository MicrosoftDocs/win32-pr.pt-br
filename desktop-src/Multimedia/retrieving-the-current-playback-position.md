---
title: Recuperando a posição de reprodução atual
description: Recuperando a posição de reprodução atual
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- áudio de onda, posição de reprodução atual
- Wave-interface de áudio, posição de reprodução atual
- executando a onda-arquivos de áudio, posição de reprodução atual
- função waveOutGetPosition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293906"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="56140-107">Recuperando a posição de reprodução atual</span><span class="sxs-lookup"><span data-stu-id="56140-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="56140-108">Você pode monitorar a posição de reprodução atual dentro do arquivo enquanto o áudio de formato de onda é reproduzido usando a função [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .</span><span class="sxs-lookup"><span data-stu-id="56140-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="56140-109">Para dispositivos de forma de onda-áudio, exemplos são o formato de hora preferencial no qual representar a posição atual.</span><span class="sxs-lookup"><span data-stu-id="56140-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="56140-110">Assim, a posição atual de um dispositivo de wave-áudio é especificada como o número de amostras de um canal desde o início do arquivo de áudio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="56140-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="56140-111">Para consultar a posição atual de um dispositivo de wave-áudio, defina o membro **wType** da estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para amostras de tempo \_ e passe essa estrutura para **waveOutGetPosition**.</span><span class="sxs-lookup"><span data-stu-id="56140-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="56140-112">A estrutura **MMTIME** pode representar o tempo em um ou mais formatos diferentes, incluindo milissegundos, exemplos, SMPTE (sociedade de imagem de movimento e engenheiros de televisão) e formatos de ponteiro de música MIDI.</span><span class="sxs-lookup"><span data-stu-id="56140-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="56140-113">O membro **wType** especifica o formato usado para representar o tempo.</span><span class="sxs-lookup"><span data-stu-id="56140-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="56140-114">Antes de chamar uma função que usa a estrutura **MMTIME** , você deve definir **wType** para indicar o formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="56140-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="56140-115">Certifique-se de verificar **wType** após a chamada para ver se há suporte para o formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="56140-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="56140-116">Se não houver suporte para o formato de hora solicitado, o driver de dispositivo especificará a hora em um formato de hora alternativo e alterará o membro **wType** para o formato de hora selecionado.</span><span class="sxs-lookup"><span data-stu-id="56140-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="56140-117">Para obter mais informações sobre a estrutura **MMTIME** , consulte [timers de multimídia](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="56140-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 