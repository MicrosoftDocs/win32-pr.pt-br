---
title: Acessando um buffer de e/s de arquivo
description: Acessando um buffer de e/s de arquivo
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- e/s de arquivo multimídia, acessando buffers
- e/s de arquivo, acessando buffers
- entrada e saída (e/s), acesso a buffers
- E/s (entrada e saída), acesso a buffers
- Acessando buffers de e/s
- e/s em buffer
- função mmioSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105810308"
---
# <a name="accessing-a-file-io-buffer"></a>Acessando um buffer de e/s de arquivo

O exemplo a seguir acessa um buffer de e/s diretamente para ler dados de um arquivo de formato de onda-áudio.


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



Quando você terminar de acessar um buffer de e/s de arquivo, chame a função [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , passando um endereço da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) preenchida pela função [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) . Se você escreveu no buffer, defina o \_ sinalizador sujo MMIO no membro **dwFlags** da estrutura **MMIOINFO** antes de chamar **mmioSetInfo**. Caso contrário, o buffer não será liberado para o disco.

 

 