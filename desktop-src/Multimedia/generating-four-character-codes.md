---
title: Gerando códigos Four-Character dados
description: Gerando códigos Four-Character dados
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- E/S de arquivo multimídia, códigos de quatro caracteres
- E/S de arquivo, códigos de quatro caracteres
- entrada e saída (E/S), códigos de quatro caracteres
- E/S (entrada e saída), códigos de quatro caracteres
- códigos de quatro caracteres
- Função mmioStringToCCICC
- macro mmioMINALCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96dd724876a3c4b6ac37424b49411edac5929c61d1fcf6c8c18275b1d6ae9dd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785306"
---
# <a name="generating-four-character-codes"></a>Gerando códigos Four-Character dados

Você pode usar a [**macro mmio BOOCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) ou a [**função mmioStringToMINALCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar códigos de quatro caracteres. O exemplo a seguir **usa mmio BOOCC** para gerar um código de quatro caracteres para "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



O exemplo a seguir [**usa mmioStringToCENECC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar um código de quatro caracteres para "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



O segundo parâmetro em [**mmioStringTo BOOCC especifica**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) sinalizadores para converter a cadeia de caracteres em um código de quatro caracteres. Se você especificar o sinalizador MMIO \_ TOUPPER, **mmioStringTo ALPHABETCC** converterá todos os caracteres alfabéticos na cadeia de caracteres em letras maiúsculas. Isso é útil quando você precisa especificar um código de quatro caracteres para identificar um procedimento de E/S personalizado porque códigos de quatro caracteres que identificam nomes de extensão de arquivo devem estar em letras maiúsculas.

 

 