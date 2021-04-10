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
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294052"
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

 

 