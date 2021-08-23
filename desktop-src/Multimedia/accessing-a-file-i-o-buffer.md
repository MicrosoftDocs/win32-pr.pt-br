---
title: Acessando um buffer de E/S de arquivo
description: Acessando um buffer de E/S de arquivo
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- E/S de arquivo multimídia, acessando buffers
- E/S de arquivo, acessando buffers
- entrada e saída (E/S), acessando buffers
- E/S (entrada e saída), acessando buffers
- acessando buffers de E/S
- E/S em buffer
- Função mmioSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4ab9533f0f121d42f859961b60d405477856faacee8d8cf36a0dfb975e2587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808636"
---
# <a name="accessing-a-file-io-buffer"></a>Acessando um buffer de E/S de arquivo

O exemplo a seguir acessa um buffer de E/S diretamente para ler dados de um arquivo waveform-audio.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



Quando você terminar de acessar um buffer de E/S de arquivo, chame a função [**mmioSetInfo,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) passando um endereço da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) preenchida pela [**função mmioGetInfo.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) Se você escreveu no buffer, defina o sinalizador MMIO DIRTY no membro \_ **dwFlags** da estrutura **MMIOINFO** antes de chamar **mmioSetInfo**. Caso contrário, o buffer não será liberado para o disco.

 

 