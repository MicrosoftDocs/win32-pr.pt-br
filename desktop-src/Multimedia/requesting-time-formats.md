---
title: Solicitando formatos de hora
description: Solicitando formatos de hora
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (interface digital de instrumento musical), formatos de hora
- MIDI (interface digital de instrumentos musicais), formatos de hora
- Serviços de MIDI, formatos de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640476"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="7fb23-106">Solicitando formatos de hora</span><span class="sxs-lookup"><span data-stu-id="7fb23-106">Requesting Time Formats</span></span>

<span data-ttu-id="7fb23-107">O Windows usa a estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar o tempo em um ou mais formatos diferentes, incluindo formatos de ponteiro de música de milissegundos, exemplos, SMPTE e MIDI.</span><span class="sxs-lookup"><span data-stu-id="7fb23-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="7fb23-108">O membro **wType** especifica o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="7fb23-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="7fb23-109">A função [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa a estrutura **MMTIME** .</span><span class="sxs-lookup"><span data-stu-id="7fb23-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="7fb23-110">Antes de chamar essa função, você deve definir o membro **wType** para indicar o formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="7fb23-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="7fb23-111">Para ver se o formato de hora solicitado tem suporte, verifique **wType** após a chamada.</span><span class="sxs-lookup"><span data-stu-id="7fb23-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="7fb23-112">Se o formato de hora solicitado não tiver suporte, a hora será especificada em um formato de hora alternativo selecionado pelo driver de dispositivo e o membro **wType** será alterado para indicar o formato de hora selecionado.</span><span class="sxs-lookup"><span data-stu-id="7fb23-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="7fb23-113">Para obter mais informações sobre a estrutura **MMTIME** , consulte [timers de multimídia](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="7fb23-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fb23-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fb23-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb23-115">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="7fb23-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 