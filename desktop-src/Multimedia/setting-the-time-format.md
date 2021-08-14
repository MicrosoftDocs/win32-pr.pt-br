---
title: Definindo o formato de hora
description: Definindo o formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370884"
---
# <a name="setting-the-time-format"></a>Definindo o formato de hora

Use a [**mensagem de comando MCI \_ SET**](mci-set.md) junto com a estrutura [**MCI SET \_ \_ PARMS**](mci-set-parms.md) para definir o formato de hora para um dispositivo aberto. De definir **o membro dwTimeFormat** como uma das constantes a seguir.



| Constante                   | Formato de hora                                          |
|----------------------------|------------------------------------------------------|
| BYTES DE FORMATO \_ MCI \_         | Bytes (em arquivos de formato PCM com pulse code \[ \] modular) |
| FORMATO MCI \_ \_ MILISSEGUNDOS  | Milissegundos                                         |
| \_MSF DE \_ FORMATO MCI           | Minuto/segundo/quadro                                  |
| EXEMPLOS DE FORMATO MCI \_ \_       | Exemplos                                              |
| FORMATO MCI \_ \_ SMPTE \_ 24     | SMPTE, 24 quadros                                      |
| FORMATO MCI \_ \_ SMPTE \_ 25     | SMPTE, 25 quadros                                      |
| FORMATO MCI \_ \_ SMPTE \_ 30     | SMPTE, 30 quadros                                      |
| MCI \_ FORMAT \_ SMPTE \_ 30DROP | SMPTE, queda de 30 quadros                                 |
| TMSF DE \_ \_ FORMATO MCI          | Track/minute/second/frame                            |
| MCI \_ SEQ \_ FORMAT \_ SONGPTR  | Ponteiro de música MIDI                                    |



 

O exemplo a seguir define o formato de tempo como milissegundos no dispositivo especificado pela variável wDeviceID usando a [**função mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 