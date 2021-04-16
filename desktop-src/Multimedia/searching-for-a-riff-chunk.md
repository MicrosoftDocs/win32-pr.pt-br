---
title: Pesquisando uma parte do RIFF
description: Pesquisando uma parte do RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- e/s de arquivo multimídia, pesquisando a parte do RIFF
- e/s de arquivo, pesquisando a parte do RIFF
- entrada e saída (e/s), pesquisando a parte do RIFF
- E/s (entrada e saída), pesquisando a parte do RIFF
- pesquisando a parte do RIFF
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
- Parte do RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366018"
---
# <a name="searching-for-a-riff-chunk"></a><span data-ttu-id="05302-112">Pesquisando uma parte do RIFF</span><span class="sxs-lookup"><span data-stu-id="05302-112">Searching for a RIFF Chunk</span></span>

<span data-ttu-id="05302-113">O exemplo a seguir usa a função [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para pesquisar uma parte "riff" com um tipo de formulário de "onda" para verificar se o arquivo que acabou de ser aberto é um arquivo de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="05302-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for a "RIFF" chunk with a form type of "WAVE" to verify that the file that has just been opened is a waveform-audio file.</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 