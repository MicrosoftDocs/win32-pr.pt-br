---
title: Abrindo um arquivo com mmioOpen
description: Abrindo um arquivo com mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- e/s de arquivo multimídia, abrindo arquivos
- e/s de arquivo, abrindo arquivos
- entrada e saída (e/s), abertura de arquivos
- E/s (entrada e saída), abertura de arquivos
- e/s de arquivo multimídia, função mmioOpen
- e/s de arquivo, função mmioOpen
- entrada e saída (e/s), função mmioOpen
- E/s (entrada e saída), função mmioOpen
- função mmioOpen
- Abrindo arquivos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd323e888b181b0166572d11687d3dde66e83f0ce73541555b1f49083564ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893186"
---
# <a name="opening-a-file-with-mmioopen"></a>Abrindo um arquivo com mmioOpen

Para abrir um arquivo para operações de e/s básica, defina o parâmetro *lpmmioinfo* da função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) como **NULL**. O exemplo a seguir abre um arquivo chamado "C: \\ samples \\SAMPLE1.TXT" para leitura e verifica o valor de retorno em busca de erro.


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



Use o parâmetro *dwFlags* de **mmioOpen** para especificar sinalizadores para abrir um arquivo.

 

 