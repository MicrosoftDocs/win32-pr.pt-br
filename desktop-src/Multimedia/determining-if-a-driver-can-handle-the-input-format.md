---
title: Determinando se um driver pode manipular o formato de entrada
description: Determinando se um driver pode manipular o formato de entrada
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- VCM (gerenciador de compactação de vídeo), formato de entrada
- VCM (gerenciador de compactação de vídeo), formato de entrada
- Macro ICDrawQuery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497286"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Determinando se um driver pode manipular o formato de entrada

O exemplo a seguir mostra como verificar o formato de entrada com a macro [**ICDrawQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery)


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




