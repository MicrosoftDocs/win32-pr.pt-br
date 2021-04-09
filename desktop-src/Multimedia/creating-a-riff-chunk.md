---
title: Criando uma parte do RIFF
description: Criando uma parte do RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de arquivo multimídia, criando parte do RIFF
- e/s de arquivo, criando a parte RIFF
- entrada e saída (e/s), criando parte do RIFF
- E/s (entrada e saída), criando a parte do RIFF
- Criando parte do RIFF
- função mmioCreateChunk
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
- Parte do RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823718"
---
# <a name="creating-a-riff-chunk"></a>Criando uma parte do RIFF

O exemplo a seguir usa a função [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para criar uma parte com um identificador de parte de "riff" e um tipo de formulário de "RDIB".


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Se você estiver criando uma parte "RIFF" ou "lista", deverá especificar o tipo de formulário ou de lista no membro **fccType** da estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) . No exemplo anterior, "RDIB" é o tipo de formulário.

Se você souber o tamanho do campo de dados em uma nova parte, poderá definir o membro **cksize** da estrutura **MMCKINFO** ao criar a parte. Esse valor será gravado no campo tamanho dos dados na nova parte. Se esse valor não estiver correto quando você chamar [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) para marcar o final da parte, ele será reescrito automaticamente para refletir o tamanho correto do campo de dados.

Depois de criar uma parte usando a função [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , a posição do arquivo é definida como o campo de dados da parte (8 bytes a partir do início da parte). Se a parte for uma parte "RIFF" ou "lista", a posição do arquivo será definida como o local após o tipo de formulário ou tipo de lista (12 bytes a partir do início da parte).

 

 