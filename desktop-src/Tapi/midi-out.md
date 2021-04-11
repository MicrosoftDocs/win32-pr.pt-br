---
description: A classe de dispositivo MIDI/out consiste em seqüenciais MIDI que são usados para saída. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164246"
---
# <a name="midiout"></a><span data-ttu-id="2c4f2-104">MIDI/out</span><span class="sxs-lookup"><span data-stu-id="2c4f2-104">midi/out</span></span>

<span data-ttu-id="2c4f2-105">A classe de dispositivo MIDI/out consiste em seqüenciais MIDI que são usados para saída.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="2c4f2-106">Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).</span><span class="sxs-lookup"><span data-stu-id="2c4f2-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2c4f2-107">As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="2c4f2-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="2c4f2-108">O membro **DeviceID** é o identificador de um dispositivo MIDI fechado.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="2c4f2-109">Você usa esse identificador em uma chamada para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir o dispositivo para saída.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="2c4f2-110">Você pode usar o identificador de dispositivo resultante para reproduzir dados MIDI no dispositivo de linha ou telefone.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="2c4f2-111">Para obter mais informações sobre as funções de MIDI, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2c4f2-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
