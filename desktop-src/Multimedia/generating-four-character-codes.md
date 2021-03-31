---
title: Gerando códigos de Four-Character
description: Gerando códigos de Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- e/s de arquivo multimídia, códigos de quatro caracteres
- e/s de arquivo, códigos de quatro caracteres
- código de entrada e saída (e/s), códigos de quatro caracteres
- E/s (entrada e saída), códigos de quatro caracteres
- códigos de quatro caracteres
- função mmioStringToFOURCC
- macro mmioFOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640555"
---
# <a name="generating-four-character-codes"></a>Gerando códigos de Four-Character

Você pode usar a macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) ou a função [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar códigos de quatro caracteres. O exemplo a seguir usa **mmioFOURCC** para gerar um código de quatro caracteres para "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



O exemplo a seguir usa [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar um código de quatro caracteres para "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



O segundo parâmetro em [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) especifica sinalizadores para converter a cadeia de caracteres em um código de quatro caracteres. Se você especificar o \_ sinalizador MMIO TOUPPER, **mmioStringToFOURCC** converterá todos os caracteres alfabéticos na cadeia de caracteres em letras maiúsculas. Isso é útil quando você precisa especificar um código de quatro caracteres para identificar um procedimento de e/s personalizado porque códigos de quatro caracteres identificando nomes de extensão de arquivo devem estar em letras maiúsculas.

 

 