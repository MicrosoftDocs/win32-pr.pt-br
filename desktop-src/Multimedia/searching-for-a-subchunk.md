---
title: Pesquisando uma subparte
description: Pesquisando uma subparte
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
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
ms.openlocfilehash: f9f77cc4d3b9640e0d262a113d3c8f352bb30fce625737b1bf13dde24adbe578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371134"
---
# <a name="searching-for-a-subchunk"></a>Pesquisando uma subparte

O exemplo a seguir usa a função [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para procurar a parte "fmt" na parte "riff" do exemplo anterior.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Para pesquisar uma subparte (ou seja, qualquer parte que não seja uma parte "RIFF" ou "lista"), identifique sua parte pai no parâmetro *lpckParent* da função [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .

Se você não especificar uma parte pai, a posição atual do arquivo deverá estar no início de uma parte antes de chamar a função **mmioDescend** . Se você especificar uma parte pai, a posição atual do arquivo poderá estar em qualquer lugar nessa parte.

Se a pesquisa de uma subparte falhar, a posição atual do arquivo será indefinida. Você pode usar a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) e o membro **DwDataOffset** da estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) descrevendo a parte pai para buscar de volta até o início da parte pai, como no exemplo a seguir:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Como **dwDataOffset** especifica o deslocamento para o início da parte de dados da parte, você deve procurar quatro bytes após **dwDataOffset** para definir a posição do arquivo após o tipo de formulário.

 

 