---
description: A classe de dispositivo MIDI/in consiste em seqüenciais MIDI que são usados para entrada. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646659"
---
# <a name="midiin"></a><span data-ttu-id="6b6aa-104">MIDI/in</span><span class="sxs-lookup"><span data-stu-id="6b6aa-104">midi/in</span></span>

<span data-ttu-id="6b6aa-105">A classe de dispositivo MIDI/in consiste em seqüenciais MIDI que são usados para entrada.</span><span class="sxs-lookup"><span data-stu-id="6b6aa-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="6b6aa-106">Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).</span><span class="sxs-lookup"><span data-stu-id="6b6aa-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="6b6aa-107">As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="6b6aa-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="6b6aa-108">O membro **DeviceID** é o identificador de um dispositivo MIDI fechado.</span><span class="sxs-lookup"><span data-stu-id="6b6aa-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="6b6aa-109">Você usa esse identificador em uma chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir o dispositivo para entrada.</span><span class="sxs-lookup"><span data-stu-id="6b6aa-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="6b6aa-110">Você pode usar o identificador de dispositivo resultante para registrar dados MIDI do dispositivo de linha ou telefone.</span><span class="sxs-lookup"><span data-stu-id="6b6aa-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="6b6aa-111">Para obter mais informações sobre as funções de MIDI, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6b6aa-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
