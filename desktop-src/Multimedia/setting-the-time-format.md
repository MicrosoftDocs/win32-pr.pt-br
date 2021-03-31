---
title: Definindo o formato de hora
description: Definindo o formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823714"
---
# <a name="setting-the-time-format"></a>Definindo o formato de hora

Use a mensagem de comando [**\_ set do MCI**](mci-set.md) junto com a estrutura do [**MCI \_ set \_ parms**](mci-set-parms.md) para definir o formato de hora para um dispositivo aberto. Defina o membro **dwTimeFormat** como uma das constantes a seguir.



| Constante                   | Formato de hora                                          |
|----------------------------|------------------------------------------------------|
| \_bytes de formato MCI \_         | Bytes (em arquivos de formato PCM modulados por código de pulso \[ \] ) |
| \_milissegundos do formato MCI \_  | Milissegundos                                         |
| \_formato MCI \_ MSF           | Minuto/segundo/quadro                                  |
| \_exemplos de formato MCI \_       | Exemplos                                              |
| \_Formato MCI \_ SMPTE \_ 24     | SMPTE, 24 frame                                      |
| \_Formato MCI \_ SMPTE \_ 25     | SMPTE, 25 quadros                                      |
| \_Formato MCI \_ SMPTE \_ 30     | SMPTE, 30 quadros                                      |
| \_Formato MCI \_ SMPTE \_ 30DROP | SMPTE, 30 quadros drop                                 |
| \_formato MCI \_ TMSF          | Faixa/minuto/segundo/quadro                            |
| \_formato de Seq MCI \_ \_ SONGPTR  | Ponteiro de música MIDI                                    |



 

O exemplo a seguir define o formato de hora como milissegundos no dispositivo especificado pela variável wDeviceID usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


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



 

 