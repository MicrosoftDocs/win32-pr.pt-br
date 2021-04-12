---
title: Recebendo Time-Stamped mensagens MIDI
description: Recebendo Time-Stamped mensagens MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (interface digital de instrumento musical), mensagens com carimbo de data/hora
- MIDI (interface digital de instrumentos musicais), mensagens com carimbo de data/hora
- gravando áudio MIDI, mensagens com carimbo de data/hora
- mensagens de MIDI com carimbo de data/hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293969"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="50658-107">Recebendo Time-Stamped mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="50658-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="50658-108">Devido ao atraso entre o momento em que o driver de dispositivo recebe uma mensagem MIDI e a hora em que o aplicativo recebe a mensagem, os drivers de dispositivo de entrada MIDI carimbam a mensagem MIDI com a hora em que a mensagem foi recebida.</span><span class="sxs-lookup"><span data-stu-id="50658-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="50658-109">Os carimbos de data/hora MIDI, que são definidos como a hora em que o primeiro byte da mensagem foi recebido, são especificados em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="50658-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="50658-110">A função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) redefine os carimbos de data/hora de um dispositivo para zero.</span><span class="sxs-lookup"><span data-stu-id="50658-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="50658-111">Conforme mencionado anteriormente, para receber carimbos de data/hora com entrada MIDI, você deve usar uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="50658-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="50658-112">O parâmetro *dwParam2* da função de retorno de chamada especifica o carimbo de data/hora dos dados associados aos [**\_ dados do mim**](mim-data.md) e às mensagens do [**mim \_ LONGDATA**](mim-longdata.md) .</span><span class="sxs-lookup"><span data-stu-id="50658-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50658-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50658-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50658-114">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="50658-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 