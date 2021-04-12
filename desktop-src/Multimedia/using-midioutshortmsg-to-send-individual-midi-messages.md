---
title: Usando midiOutShortMsg para enviar mensagens MIDI individuais
description: Usando midiOutShortMsg para enviar mensagens MIDI individuais
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), função midiOutShortMsg
- MIDI (interface digital de instrumentos musicais), função midiOutShortMsg
- função midiOutShortMsg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454029"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a><span data-ttu-id="8a8e6-109">Usando midiOutShortMsg para enviar mensagens MIDI individuais</span><span class="sxs-lookup"><span data-stu-id="8a8e6-109">Using midiOutShortMsg to Send Individual MIDI Messages</span></span>

<span data-ttu-id="8a8e6-110">O exemplo a seguir usa a função [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) para enviar um evento MIDI especificado para um determinado dispositivo de saída de Midi:</span><span class="sxs-lookup"><span data-stu-id="8a8e6-110">The following example uses the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function to send a specified MIDI event to a given MIDI output device:</span></span>


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> <span data-ttu-id="8a8e6-111">Os drivers de saída de MIDI não são necessários para verificar os dados antes de enviá-los para uma porta de saída.</span><span class="sxs-lookup"><span data-stu-id="8a8e6-111">MIDI output drivers are not required to verify data before sending it to an output port.</span></span> <span data-ttu-id="8a8e6-112">Os aplicativos devem garantir que apenas dados válidos sejam enviados.</span><span class="sxs-lookup"><span data-stu-id="8a8e6-112">Applications must ensure that only valid data is sent.</span></span>

 

 

 