---
title: Verificando o dispositivo de saída
description: Verificando o dispositivo de saída
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- MCI_ comando de STATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916388"
---
# <a name="verifying-the-output-device"></a><span data-ttu-id="780c2-104">Verificando o dispositivo de saída</span><span class="sxs-lookup"><span data-stu-id="780c2-104">Verifying the Output Device</span></span>

<span data-ttu-id="780c2-105">Depois de abrir o Sequencer, você deve verificar se o mapeador de MIDI estava disponível e selecionado como o dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="780c2-105">After opening the sequencer, you should check whether the MIDI mapper was available and selected as the output device.</span></span> <span data-ttu-id="780c2-106">O exemplo a seguir usa o comando de [**\_ status MCI**](mci-status.md) para verificar se o mapeador de Midi é o dispositivo de saída para o sequenciador MCI.</span><span class="sxs-lookup"><span data-stu-id="780c2-106">The following example uses the [**MCI\_ STATUS**](mci-status.md) command to verify that the MIDI mapper is the output device for the MCI sequencer.</span></span>


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




