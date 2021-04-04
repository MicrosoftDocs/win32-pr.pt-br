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
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007555"
---
# <a name="changing-the-io-buffer-size"></a><span data-ttu-id="52399-111">Alterando o tamanho do buffer de e/s</span><span class="sxs-lookup"><span data-stu-id="52399-111">Changing the I/O Buffer Size</span></span>

<span data-ttu-id="52399-112">O exemplo a seguir abre um arquivo chamado SAMPLE.TXT para e/s não armazenada em buffer e, em seguida, habilita o e/s em buffer com um buffer interno de 16K usando a função [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="52399-112">The following example opens a file named SAMPLE.TXT for unbuffered I/O, and then enables buffered I/O with an internal 16K buffer using the [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) function.</span></span>


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



 

 