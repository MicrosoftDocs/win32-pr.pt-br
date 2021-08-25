---
title: Pesquisando uma parte DE HASH
description: Pesquisando uma parte DE HASH
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- E/S de arquivo multimídia, pesquisando a parte DEIS
- E/S de arquivo, pesquisando a parte DEIS
- entrada e saída (E/S), pesquisando por parte de HASH
- E/S (entrada e saída), pesquisando por parte de HASH
- pesquisando a parte DEIS
- formato de arquivo de intercâmbio de recursos (PDF)
- CHANG (formato de arquivo de intercâmbio de recursos)
- E/S DO BLUES
- Parte DE HASH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbb09c7777cf675ceb0f11ae84fb50a3b9deaa73910ca9e15280c3fb88c42cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782086"
---
# <a name="searching-for-a-riff-chunk"></a>Pesquisando uma parte DE HASH

O exemplo a seguir usa a [**função mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para pesquisar uma parte "DIGIT" com um tipo de formulário "WAVE" para verificar se o arquivo que acabou de ser aberto é um arquivo waveform-audio.


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



 

 