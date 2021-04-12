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
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454053"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="fe9e0-113">Abrindo um arquivo com mmioOpen</span><span class="sxs-lookup"><span data-stu-id="fe9e0-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="fe9e0-114">Para abrir um arquivo para operações de e/s básica, defina o parâmetro *lpmmioinfo* da função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe9e0-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="fe9e0-115">O exemplo a seguir abre um arquivo chamado "C: \\ samples \\SAMPLE1.TXT" para leitura e verifica o valor de retorno em busca de erro.</span><span class="sxs-lookup"><span data-stu-id="fe9e0-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="fe9e0-116">Use o parâmetro *dwFlags* de **mmioOpen** para especificar sinalizadores para abrir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe9e0-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 