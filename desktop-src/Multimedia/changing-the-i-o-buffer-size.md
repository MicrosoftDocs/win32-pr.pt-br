---
title: Alterando o tamanho do buffer de e/s
description: Alterando o tamanho do buffer de e/s
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- e/s de arquivo multimídia, alterando o tamanho do buffer
- e/s de arquivo, alterando o tamanho do buffer
- entrada e saída (e/s), alterando o tamanho do buffer
- E/s (entrada e saída), alterando o tamanho do buffer
- alterando O tamanho do buffer de e/s
- e/s sem buffer
- e/s em buffer
- função mmioSetBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 826fabfb7e51b80bf406721b3d5e7b094f83c1c3fe2061f7edea0810a41dc639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145079"
---
# <a name="changing-the-io-buffer-size"></a>Alterando o tamanho do buffer de e/s

O exemplo a seguir abre um arquivo chamado SAMPLE.TXT para e/s não armazenada em buffer e, em seguida, habilita o e/s em buffer com um buffer interno de 16K usando a função [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 